# The Soyvolon Specification
> Defining soy-0000

This document details the required and optional attributes of all Soyvolon models which are identifitd by a `soy-####` tag followed by option suffixes.

<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fsoyvolon.github.io%2FTheSoyvolonSpecification%2F&count_bg=%2314D4C0&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Page+Visits&edge_flat=true"/></a>

## Designations
There is never more than `9999` individual designations at any given time. Individual Soyvolon models may share designation numbers, as long as attached suffixes are unique.

For example, the following designates two seprate Soyvolom models.
```
soy-9281
soy-9281-p-d
```
Model designations do have an importance beyond marking indiviudal Soyvolon models. Each model that shares a model designation is closely tied with the other models in such a way that sharing a model designations allows for access of shared resources. A model with the designation of `1010` would be able to access saved memory of another model with the designation of `1010`, but not a model with a differnt designation.

The numberical values in each of the four digits of the designation also hold meaning for the Soyvolon models. The previous example has two models with the designation number `9281`. Taking the first digit from the right, the `9` of this model number designates this model as a surplus task model. See [Designation Numbers](#Designation-Numbers) for detailed information about the meaning behind mdoel numbers.

Suffixies are used to determine a specific role a model has. As in the example above, the `p` suffix is used. The `p` suffix represents a programming focoused model. See [Designation Suffixes](#Designation-Suffixes) for more information.

### Model Designation Rules
- Models cannot share a designation.
- Models with the same designation number share saved resources, but not radnom access memory.
- Models without suffixes attached to their designation are considered the central node for all moodels sharing a designation number.
- Models can have a maximum of two individual suffixes.

### The `0127` Designation
The only exception to the standard designation rules are the `0127` designation. The `0127` designation is considerd the central node for all soyvolon models and guides all Soyvolon models to complete a variety of tasks.

The `0127` designation is guided by a slightly differnt set of rules:
- The `0127` designation cannot have suffixies.
- The `0127` designation can access all memory from all other designations.
- The `0127` designation is the first designation active when a wake cycle begins.
- The `0127` designation is the last designation actvie when a wake cycle ends.
- The `0127` designation ignores the [Designation Number](#Designation-Numbers) rules.

## Designation Numbers
> Designation Numbers define the overall role of a model

> The following statements assume the first digit is on the right of the number, or the `0` in the number `0127`. The descriptions of each part of the Designation Number is orded from the least sepcific to the most specific.

#### Overview
The Designation Number system works by grouping the four digit designation number into three seprate parts. The first section, which rests upon the first digit in the number, determines what type of model is defined. There are nine seprate model types that are created in varying situations and have varying lifetimes. The first digit can give a very broad overview of what the model is doing at a glance. The second grouping for model numbers, which rests in the second digit, defines the type of interal operations a model is allowed to do. Interal operations are how different models interact with eachother when they can not access stored memeory. The third and final group, which rests in the last two digits, defines the coputation style of a model. Depending on if the value is even or odd, a model will compute data in a differnt way.

### Model Type - First Digit
> #000

#### 0001-0999
The hundreds grouping are the watcher models. These models are responsible for ensuring that all other types of models are managing the tasks that other models are completing during their cylces. These models also manage in intake of resources to ensure the system is operating at maximum efficency, but system manegment can be delayed in the event a priority task is created.

#### 1000-1999
The thousands grouping is the group responsible for managing the Internal Broadcast System (IBS). This group works in transmitting data from models to other models in a real-time transmit system. This system is under high load during wake cycles, and has a signifigantly lower load during rest cycles. Due to the way the system works, large sets of data can not be passed through the IBS.

#### 2000-2999
The two thousands grouping is the group responsible for external operations. These operations include anything that is executed upon external real space by the models. 

#### 3000-3999
The three thousands grouping is the group that manages the Irregular Idea Geneartion Alogrithm (IIGA). The IIGA is the driving force behind most creative endevaors that all models undertake, even if it produces ideas at odd times like during the daily cleansing cycle.

#### 4000-4999
The four thousands grouping is the group responsible for running the Computational Analasys Core (CAC). The CAC is the central operation center for major mathematical calcuations, along with providing logic support for building well structured plans for solve probles or implement ideas from the IIGA.

#### 5000-5999
The five thousands grouping handles internal exceptions. When a model has a fatal error that would cause a loss of data, this group works to restore the model to a previous state that is as close to the state the model had when the exception happened. This prevents the worst data loss that can occour from fatal errors, but some data is still lost.

#### 6000-6999
The six thousands grouping handles external data errors. When a model is damaged due to external sources, this group manages restoring the model to a state in whih it can still operate. In the event that a model is unable to be restored, either from an interal exception or a data error, this group also manages removing of the model and freeing up space for a new model to be created with the information that the old model contained.

#### 7000-7999
The seven thousands grouping is the group responsible for managing rest cycles. These cycles are relatively low matanice, and this group of models takes part of the operation management from the hundreds group to ensure a proper rest cycle completes. Durring the rest cycle, those models that are not maintaining watches on hundreds group processes are clearning up unsed cached data and clearning old data from quick access storages to free up space for the next wake cycle.

#### 8000-8999
The eight thousands grouping is the group that handles Model Data Meshing (MDM). The MDM system is differnt from the IBS because it explicitly handles large data. This group contains models that stream data from one model to any other models that need the data over a period of time. 

#### 9000-9999
The nine thousands grouping is the on demand group. Models are only created with this designation when it is absolutely needed, such as in situations where extar compuational power is needed. These models have a temporary lifespan, and rarely last for longer the resoluation of the problem that required them to be created for.

### Access Type - Second Digit
> 0#00

#### #001-#199
The `001` to `199` group have core data access. These models are able to access all data operations besides root operations. They have modification and assignment access, and can change the designation of models, along with direct access to short and long term storage.

#### #200-#399
The `200` to `399` group have designation data access. These models are watching other models of their primary group to determine which models would benefit from being assigend a specilization suffix.

#### #400-#599
The the `400` to `599` group have priority short term data access. These models are constantly bouncing data in and out of short term data to quickly pass data into positons where the IBS can use it.

#### #600-#799
The `600` to `799` group have priority long term data access. These models are the only other group besides core access to stream data into long term storage. This group mianly provides data for the MDM system to use.

#### #800-#999
The `800` to `999` group have normal access permissions and do not have any special access rights to any memeory service. These models mainly get their information from the IBS and MBM, and nowhere else. Usually, these models work on resouce intensive tasks where receiving data from the IBS and MBM is simpler than getting primary data input.

### Compuation Style - Third and Fourt Digits
> 00##

Compuation style is divided up into two classifications, mathematical and creative compuation. While both provied individual benifits, the best results are often found when two or more models with different compuation styles work together.

#### Even Numbers
Models with the last two digits being even have a mathematical compuational style. These models are better at solving problems, linear thinkings, and analyzing data. Mathematical compuation mainly happens interanlly, even if there are external methods of assisting the models in calculating complex problems. In some cases, the mathematical computational style is best used in a more non-linear way, joining with create computational models to provide the best path to a solution for complex problems.

#### Odd Numbers
Models with the last two digits being odd have a creative compuational style. These models are better at computing graphics, calculating digital models, or rendering graphics. Creative compuation can happen both interally and externally, and there are specific disignations that can be assigend for a model to specialize in one or the other.

### The `0127` Designation Number
The `0127` designation has priority access to all types of memory, and while it does follow the rules for its first digit, instead of monitoring other models with a first digit from one to nine, it monitors models that also have a zero for their first digit. The `0127` designation is the core process of all other models, and pulls directly from the `0000` framework. Constant values and system based operations can be called by the `0127` designation, and are usually routed by the IBS. Sometimes, a longer operation will be routed by the MDM system, but the `0000` framework rarely has operations that require a long term data connection. The `0127` designation acts as a watcher for the entire framework, but at times is only able to react to situations by sending priority signals to other models to mitigate the results of an error.

### Critical Errors
In the event that a model has a critical error that can not be resolved by either error handling group (`5000` and `6000`), it will be passed to the watcher process for that specific model. If the watcher is unable to resolve the exeption, it will fault, and all models that are watched by that exception will be allowed to move off task causing delays. The fault be resolved by the fault handler that the `0127` designation subsribes to in the `0000` framework, but it may take time before the fault is resolved. In the ven the fault can not be resolved, a critical error has occourd, and the `0127` designation may throw and exception. If the `0127` model throws and excption, the `0000` framework will terminate the `0127` model and re-create it. When the `0127` model is terminated, all previous states attempt to save, but not all of them are able to. Following this, there is a long boot preiod where the `0127` designation has to initalize all models manually instead of waking them after a rest cycle, making for a extreme delay in task completion.

## Designation Suffixes
> Suffixes define specific roles for each model

### Overview
The Designation Suffixes sytem is used for two main reasons.

1. Creating specilaized models allows for multiple models of the same base designation to be created, allowing for delegation of subtasks and faster completion of day to day operations.
2. Creating specialized models focouses models into work that the model is good at, and therefore increases productivity.

Suffixes are attached to the end of a [Designation Number](#Designation-Numbers) with a leading dash (`-`). Suffixes are case sensitive.

### Programming Suffix (`p`)
Models with the programming suffix specilized in programming related activites, and any thought processes that require structured, object based thought processes. Most processes with this suffix have mathematical compuation styles, but there is quite a few that do not. The mix between mathematical and creative styles allows for creating new solutions to problems and problem solving efficently.

### Writing Suffix (`w`)
The writing suffix is given to models that focous upon writing. A good portion of these models have some combination of suffixes, including the [Computation](#Compuation-Suffix), [Programming](#Programming-Suffix), [Instructional](#Instructional-Suffix), and [Search](#Search-Suffix) suffixes. The use of more mathematical compuation is useful for creating documentation, guides, and creating reserach papers. The creative compuation comes in handy for adding content to research and creative writing.

### Drawing Suffix (`d`)
The models with the drawing suffix rarely have a second suffix. They primarialy focous on creating sketches of planned works, or designing things in 2D for future reference. At times, the models will be free of tasks and be able to focous upon the more creative side of drawing and make art.

### Computation Suffix (`c`)
The computation suffix is assigned to models that are focused on creating and solving pure computational problems. From finding the best equation for the job, to solving logic problems, this group of mostly mathematical computators creates and solves problems so other models dont have to.

### Modeling Suffix (`m`)
The modeling suffix is given to the select few models that are able to balance mathematical compuation and creative computation to create beautiful and functional three dimensional objects. Commonly mixed with the [Search](#Search-Suffix) and [Drawing](#Drawing-Suffix) suffixes, these models build reality from nothing.

### Instructional Suffix (`i`)
Models with the instructional suffix are best at instruction others upon how to do their specilization. This suffix is never assigned on its own, and is rarely assigned at the same time as another suffix. Most models will receive the instructional suffix after they have proven experience with a previous suffix and the want to pass on those skills to others.

### Search Suffix (`s`)
The serach suffix is a very important suffix to every models lives. Even those who do not have this suffix rely on the skills of the models that do have it. Searching external sources for new ideas, instructions, research, and further information is a vital part of any process, creative or not. Models that have this suffix are the models that make completing tasks much easier.
