<img src="images/mlops-horizontal-color.svg"/>

# MLOps SIG Roadmap Draft 2020

## NOT YET PUBLISHED

This document sets out the current state of MLOps and provides a five year roadmap for future customer needs which is intended to support pre-competitive collaboration across the industry with a view to improving the overall state of MLOps as a capability for all.

It is intended that this document be iteratively refined by group consensus within the MLOps SIG across a series of regular meetings and then published annually whilst relevant.

Acknowledgements

Current active contributors to the MLOps SIG Roadmap: 

Terry Cox, Bootstrap Ltd <terry@bootstrap.je>

> Amend list of contributors here



# Introduction

## Current State of MLOps

> NOTES: Overview of the current state of MLOps for this year - revised annually. Define principles and methodologies.

### What is MLOps?

MLOps could be narrowly defined as "the ability to apply DevOps principles to Machine Learning applications" however as we shall see shortly, this narrow definition misses the true value of MLOps to the customer. Instead, we define MLOps as “the extension of the DevOps methodology to include Machine Learning and Data Science assets as first class citizens within the DevOps ecology”.

MLOps should be viewed as a practice for consistently managing the ML aspects of products in a way that is unified with all of the other technical and non-technical elements necessary to successfully commercialise those products with maximum potential for viability in the marketplace. This includes DataOps, too, as machine learning without complete, consistent, semantically valid, correct, timely, and unbiased data is problematic or leads to flawed solutions that can exacerbate built-in biases.


> MLOps is not to be confused with "AIOps". AIOps often means an application of AI technologies to Ops data with sometimes unclear aims for gaining insights. These terms are still evolving, but for the purposes of this document we do not mean AIOps in the latter usage. Some organisations are more comfortable with the designation 'AI' rather than 'Machine Learning' and so it is to be expected that MLOps may be referred to by AIOps in those domains, however the reverse is not true as use of the term 'AIOps' may not refer to the MLOps methodology.


### What is MLOps not?

It sometimes helps to consider what anti-patterns exist around a concept in order to better understand it.

For example, MLOps is not "putting Jupyter Notebooks into production environments".

RAD tools like Jupyter Notebooks can be extremely useful, both in classroom environments and in exploring problem spaces to understand potential approaches to mathematical problems. However, like all Rapid Application Development tools, they achieve the rapid element of their name by trading off other key non-functional requirements like maintainability, testability and scalability.

In the next section, we will discuss the key drivers for MLOps and expand upon the requirements for a true DevOps approach to managing ML assets. At this point in the development of the practice, it perhaps helps to understand that much of ML and AI research and development activity has been driven by Data Science rather than Computer Science teams. This specialisation has enabled great leaps in the ML field but at the same time means that a significant proportion of ML practitioners have never been exposed to the lessons of the past seventy years of managing software assets in commercial environments.

As we shall see, this can result in large conceptual gaps between what is involved in creating a viable proof of concept of a trained ML model on a Data Scientist’s laptop vs what it subsequently takes to be able to safely transition that asset into a commercial product in production environments. It is not therefore unfair to describe the current state of MLOps in 2020 as still on the early path towards maturity and to consider that much of the early challenge for adoption will be one of education and communication rather than purely technical refinements to tooling.

Compounding this challenge, Machine Learning solutions tend to be decision-making systems rather than just data processing systems and thus will be required to be held accountable to much higher standards than those applied to the best quality software delivery projects. The bar for quality and governance processes is therefore very high, in many cases representing legal compliance processes mandated by regional legislation.

As these decision-making solutions increasingly displace human decision-makers in commerce and government, we encounter a new class of governance problems, collectively known as ‘Responsible AI’. These introduce a range of challenges around complex issues such as ethics, fairness and bias in ML models and often fall under government regulation requiring interpretability and explainability of models, often to a standard higher than that applied to human staff.

As a result, it will be necessary for MLOps to develop in a manner that facilitates complex and sensitive governance processes that are of a standard appropriate to what is expected to become a highly regulated area.



## Drivers

> NOTES: Driving forces for the current snapshot of the roadmap.

### General DevOps drivers applied to MLOps

* Optimising the process of taking ML features into production by reducing Lead Time

* Optimising the feedback loop between production and development for ML assets

* Supporting the problem-solving cycle of experimentation and feedback for ML applications

* Unifying the release cycle for ML and conventional assets

* Enabling automated testing of ML assets

* Application of Agile principles to ML projects

* Supporting ML assets as first class citizens within CI/CD systems

* Enabling shift-left on Security to include ML assets

* Improving quality through standardisation across conventional and ML assets

* Applying Static Analysis, Dynamic Analysis, Dependency Scanning and Integrity Checking to ML assets

* Reducing Mean Time To Restore for ML applications

* Reducing Change Fail Percentage for ML applications

* Management of technical debt across ML assets

* Enabling whole-of-life cost savings at a product level

* Reducing overheads of IT management through economies of scale

* Facilitating the re-use of ML approaches through template or ‘quickstart’ projects

* Managing risk by aligning ML deliveries to appropriate governance processes



### Drivers unique to Machine Learning solutions that represent MLOps requirements

* Mitigating the risks associated with producing decision-making products

* Provide specific testing support for detecting ML-specific errors

* Verifying that algorithms make decisions aligned to customer values

* Tracking long-term stability of ML asset performance

* Incorporate ethical governance into management of ML assets

* Enabling automated bias detection testing

* Ensuring explainability of decisions

* Ensuring fairness in decisions

* Providing transparency and audit-ability of ML assets

* Allowing for provability of decision-making algorithms

* Ensuring long term supportability of long-lived ML assets

* Manage ML-specific security risks such as adversarial attacks

* Providing clear action paths to suspend or revert failed ML assets in production environments

* Managing economic risks associated with deployment of key decision-making systems on customer infrastructure

* Leveraging ML techniques to improve MLOps solutions

* Mitigating liability risk and accountability through appropriate due-diligence over ML assets

* Facilitating compliance verification against regional AI legislation

* Enabling fast development life cycles by offering out-of-the-box (correlated) sampling of relevant data sets

* Enabling online (streaming) and offline (batch) model predictions

* Accelerating enterprise-wide development of models through ready-to-reuse features (i.e. feature stores)


## Vision

> NOTES: Narrative vision for the future of MLOps.

An optimal MLOps experience is one where Machine Learning assets are treated consistently with all other software assets within a CI/CD environment. Machine Learning models can be deployed alongside the services that wrap them and the services that consume them as part of a unified release process.

MLOps must be language-agnostic. Training scripts for ML models can be written in a wide range of different programming languages, so a focus on Python is artificially limiting to widespread adoption.

MLOps must be framework-agnostic. There are a plethora of different Machine Learning frameworks commonly in use today and it is to be expected that these will continue to proliferate over time. It must be possible to use any desired framework within an MLOps context and be possible to combine multiple frameworks in any given deployment.

MLOps must be platform and infrastructure agnostic. Adoption of MLOps is predicated upon being able to operate using this approach within the constraints of previously defined corporate infrastructure. It should be presumed unlikely that MLOps alone is a sufficient driver to motivate fundamental change to infrastructure.

It is very important that MLOps should make no over-simplified assumptions with respect to hardware. To achieve currently known customer requirements in a range of ML fields, it will be necessary to achieve performance gains of at least three orders of magnitude. This can be expected to lead to significant change with respect to the hardware utilised to train and execute models.

We make the following assertions:

- Models may expect to be **trained** on various combinations CPU, GPU, TPU, dedicated ASICs or custom neuro-morphic silicon, with new hardware entering the market regularly.
- Models may expect to be **executed** on various combinations CPU, GPU, TPU, dedicated ASICs or custom neuro-morphic silicon, again with new hardware entering the market regularly.
- It **must not** be assumed that models will be executed on the same hardware as they are trained upon.

It is desirable to have the ability to train once but run anywhere, that is, models are trained on specific hardware to minimise training time, and optimised for different target devices based on cost or performance considerations, however this aspiration may need to be tempered with a degree of pragmatism. The ability to train on a given hardware platform requires, at minimum, dedicated driver support, and in practice usually also necessitates extensive library / framework support. The ability to execute on a given hardware platform may involve having to significantly optimise resource usage to lower product cost or require the production of dedicated silicon specific to a single task.

 Whilst there will undoubtedly be common scenarios, for example in Cloud deployment, where CPU -> CPU or GPU -> GPU is sufficient to meet requirements, MLOps must allow for a broad range of potential cross-compilation scenarios. 

MLOps implementations should follow a ‘convention over configuration’ pattern, seeking to minimise the level of build-specific assets that need to be maintained on top of the desired solution. Where configuration is necessary, it should be synthesised where possible and operate on the principle of always creating working examples that can be modified incrementally by customers to meet their needs.

The use of MLOps should teach best known methods of applying MLOps. It should be recognised that many customers will be experts in the field of Data Science but may have had relatively little exposure to DevOps or other SDLC principles. To minimise the learning curve, MLOps defaults should always align to best practice in production environments rather than ‘quick-and-dirty’ as might be the case for expert users wishing to trial an instance of the tooling in a test bench environment.



# Scope

The focus of this roadmap is upon aspects relating to extending DevOps principles to the area of Machine Learning and does not discuss basic features of DevOps or CI/CD approaches that are common across both domains. The intention is for MLOps to decorate DevOps rather than differentiate.



# Summary and Updates

> NOTES: Executive summary of the roadmap and what’s new in revised versions.

This is the first edition of the MLOps Roadmap and sets out the initial challenges for the approach with suggested potential solutions.



# Challenges

> NOTES: Identify challenges in the near and far term that constrain the customer from successfully adopting and benefiting from MLOps principles.

<table>
  <tr>
    <td>Educating data science teams regarding the risks of trying to use Jupyter Notebooks in production</td>
    <td>- Communicating the SDLC and the lessons of DevOps in a way that is comfortable for the audience<br/>
- Highlighting the dangers of using RAD tools in production<br/>
- Demonstrate simple alternatives that are easy to use as part of an MLOps process</td>
  </tr>
  <tr>
    <td>Treat ML assets as first class citizens in DevOps processes</td>
    <td>- Extend CI/CD tools to support ML assets<br/>
- Integrate ML assets with version control systems<br/></td>
  </tr>
  <tr>
    <td>Providing mechanisms by which training/testing/validation data sets, training scripts, models, experiments, and service wrappers may all be versioned appropriately</td>
    <td>- All assets under version control<br/>
- ML assets include sets of data<br/>
- Data volumes may be large<br/>
- Data may be sensitive<br/>
- Data ownership may be complex<br/>
- Multiple platforms may be involved<br/></td>
  </tr>
  <tr>
    <td>Providing mechanisms by which changes to training/testing/validation data sets, training scripts, models, experiments, and service wrappers may all be auditable across their full lifecycle</td>
    <td>- Models may be retrained based upon new training data<br/>
- Models may be retrained based upon new training approaches<br/>
- Models may be self-learning<br/>
- Models may degrade over time<br/>
- Models may be deployed in new applications<br/>
- Models may be subject to attack and require revision<br/>
- Incidents may occur that require root cause analysis and change<br/>
- Corporate or government compliance may require audit or investigation<br/></td>
  </tr>
  <tr>
    <td>Treating training/testing/validation data sets as managed assets under a MLOps workflow</td>
    <td>- Content of training/testing/validation data sets is essential to audit process, root cause analysis<br/>
- Data is not typically treated as a managed asset under conventional CI/CD<br/>
- Data may reside across multiple systems<br/>
- Data may only be able to reside in restricted jurisdictions<br/>
- Data storage may not be immutable<br/>
- Data ownership may be a factor<br/></td>
  </tr>
  <tr>
    <td>Managing the security of data in the MLOps process with particular focus upon the increased risk associated with aggregated data sets used for training or batch processing</td>
    <td>- Aggregated data carries additional risk and represents a higher value target<br/>
- Migration of data into Cloud environments, particularly for training, may be problematic</td>
  </tr>
  <tr>
    <td>Implications of privacy, GDPR and the right to be forgotten upon training sets and deployed models</td>
    <td>- The right to use data for training purposes may require audit<br/>
   - Legal compliance may require removing data from audited training sets, which in turn implies the need to retrain and redeploy models built from that data.<br/>
   -  The right to be forgotten or the right to opt out of certain data tracking may require per-user reset of model predictions</td>
  </tr>
  <tr>
    <td>Methods for wrapping trained models as deployable services in scenarios where data scientists training the models may not be experienced software developers with a background in service-oriented design</td>
    <td>Operational use of a model brings new architectural requirements that may sit outside the domain of expertise of the data scientists who created it.<br/><br/>
Model developers may not be software developers and therefore experience challenges implementing APIs around their models and integrating within solutions.<br/></td>
  </tr>
  <tr>
    <td>Approaches for enabling all Machine Learning frameworks to be used within the scope of MLOps, regardless of language or platform</td>
    <td>Common mistake to assume ML = Python<br/><br/>
Many commonly used frameworks such as PyTorch and TensorFlow exist and can be expected to continue to proliferate.<br/><br/>
MLOps must not be opinionated about frameworks or languages.<br/></td>
  </tr>
  <tr>
    <td>Approaches for enabling MLOps to support a broad range of target platforms, including but not limited to CPU, GPU, TPU, custom ASICs and neuromorphic silicon.</td>
    <td>Choice of training platform and operational platform may be varied and could be different for separate models in a single project</td>
  </tr>
  <tr>
    <td>Methods for ensuring efficient use of hardware in both training and operational scenarios</td>
    <td>- Hardware accelerators are expensive and difficult to virtualise<br/>
- Cadence of training activities impacts cost of ownership<br/>
- Elastic scaling of models against demand in operation is challenging when based upon hardware acceleration<br/></td>
  </tr>
  <tr>
    <td>Approaches for applying MLOps to very large scale problems at petabyte scale and beyond</td>
    <td>- Problems associated with moving and refreshing large training sets<br/>
- Problems associated with distributing training loads across hardware accelerators<br/>
- Problems with speed of distributing training data to correct hardware accelerators<br/>
- Problems of provisioning / releasing large pools of hardware resources<br/></td>
  </tr>
  <tr>
    <td>Providing appropriate pipeline tools to manage MLOps workflows transparently as part of existing DevOps solutions</td>
    <td>- Integration of ML assets with existing CD/CD solutions<br/>
- Extending Cloud-native build tools to support allocation of ML assets, data and hardware during training builds<br/>
- Hardware pool management<br/></td>
  </tr>
  <tr>
    <td>Testing ML assets appropriately</td>
    <td>- Conventional Unit / Integration / BDD / UAT testing<br/>
- Adversarial testing<br/>
- Bias detection<br/>
- Fairness testing<br/>
- Ethics testing<br/>
- Interpretability<br/>
- Stress testing<br/>
- Security testing<br/></td>
  </tr>
  <tr>
    <td>Governance processes for managing the release cycle of MLOps assets, including Responsible AI principles</td>
    <td>- Managing release of new training sets to data science team<br/>
- Establishing thresholds for acceptable models<br/>
- Monitoring model performance (and drift) over time to feed into thresholds for retraining and deployments<br/>
- Managing competitive training of model variants against each other in dev environments<br/>
- Managing release of preferred models into staging environments for integration and UAT<br/>
- Managing release of specific model versions into production environments for specific clients/deployments<br/>
- Managing root cause analysis for incident investigation<br/>
- Observability / interpretability<br/>
- Explainability and compliance</td>
  </tr>
  <tr>
    <td>Management of shared dependencies between training and operational phases</td>
    <td>A number of ML approaches require the ability to have reusable resources that are applied both during training and during the pre-processing of data being passed to operational models. It is necessary to be able to synchronise these assets across the lifecycle of the model. e.g. Preprocessing, Validation, Word embeddings etc.</td>
  </tr>
    <tr>
    <td>Abstraction for models</td>
    <td>Stored models are currently often little more than serialised objects. To decouple training languages, platforms and hardware from operational languages, platforms and hardware it is necessary to have broadly supported standard intermediate storage formats for models that can be used reliably to decouple training and operational phases.</td>
  </tr>
  <tr>
    <td>Longevity of ML assets</td>
    <td>Decision-making systems can be expected to require very long effective operating lifetimes. It will be necessary in some scenarios to be able to refer to instances of models across significant spans of time and therefore forward and backward compatability issues, storage formats and migration of long running transactions are all to be considered.</td>
  </tr>
  <tr>
    <td>Managing and tracking trade-offs</td>
    <td>Solutions including ML components will be required to manage trade-offs between multiple factors, for example in striking a balance between model accuracy and customer privacy, or explainability and the risk of revealing data about individuals in the data set. It may be necessary to provide intrinsic metrics to help customers balance these equations in production. It should also be anticipated that customers will need to be able to safely A/B test different scenarios to measure their impact upon this balance.</td>
  </tr>
  <tr>
    <td>Escalation of data categories</td>
    <td>As a side effect of applying governance processes to check for fairness and bias within models, it may become necessary to hold special category data providing information about race, religion or belief, sexual orientation, disability, pregnancy, or gender reassignment in order to detect such biases. As a result of this, there will be an escalation of data sensitivity and in the legal constraints that apply to the solution.</td>
  </tr>
  <tr>
    <td>Intrinsic protection of models</td>
    <td>Models are vulnerable to certain common classes of attack, such as:<br/>
    &nbsp &nbsp- Black box attempts to reverse engineer them<br/>
    &nbsp &nbsp- Model Inversion attacks attempting to extract data about individuals<br/>
    &nbsp &nbsp- Membership Inference attacks attempting to verify the presence of individuals in data sets<br/>
    &nbsp &nbsp- Adversarial attacks using tailored data to manipulate outcomes<br/>
    It should be anticipated that there will be a need for generic protections against these classes of challenge across all deployed models.</td>
  </tr>
</table>



# Technology Requirements

> NOTES: Identify specific technology requirements to enable progress against the challenges identified above.

<table>
  <tr>
    <td>Educating data science teams regarding the risks of trying to use Jupyter Notebooks in production</td>
    <td>Jupyter Notebooks are the tool we use to educate Data Scientists as they can easily be used to explore ad hoc ML problems incrementally on a laptop. Unfortunately, when all you have is a hammer, everything tends to look like a nail. </br></br>We see Jupyter Notebooks featuring in production scenarios, not because this are the best tool for the job, but because this is the tool we taught people to use and because we didn't teach about any of the problems inherent in using that tool. </br></br>This approach persists because of an ongoing gap in the tool chain.</br></br>
- Improved technology solutions are required that enable Data Scientists to easily run experiments at scale on elastic Cloud resources in a consistent, audited and repeatable way.</br>
- These solutions should integrate with existing Integrated Development Environments, Source Code Control and Quality Management tools.</br>
- Solutions should integrate with CI/CD environments so as to facilitate Data Scientists setting up multiple variations on a training approach and launching these as parallel, audited activities on Cloud infrastructure.</br>
- Working with the training of models and the consumption of trained models should be a seamless experience within a single toolchain.</br>
- Tooling should introduce new Data Scientists to the core concepts of software asset management, quality management and automated testing.</br>
- Tooling should enable appropriate governance processes around the release of ML assets into team environments.</br></td>
  </tr>
  <tr>
    <td>Treat ML assets as first class citizens in DevOps processes</td>
    <td>ML assets include but are not limited to training sets, training configurations (hyperparameters), scripts and models. Some of these assets can be large, some are more like source code assets. We should be able to track changes to all these assets, and see how the changes relate to each other. Reporting on popular devops "metrics" like "Change Failure Rate" and "Mean cycle time" should be possible if done correctly. Whilst some of these assets are large, they are not without precedent in the devops world. People have been handling changes to database configurations, copying and backup of data for some time, so they same should apply to all ML assets. In the following sections we can explore how this may be implemented.</td>
  </tr>
  <tr>
    <td>Providing mechanisms by which training sets, training scripts and service wrappers may all be versioned appropriately</td>
    <td>Training sets are prepared data sets which are extracted from production data. They may contain PII or sensitive information, so making the data available to developers in a way analagous to source code may be problematic. Training scripts are smaller artifacts but are sometimes coupled to the training sets. All scripts should be versioned in a way that makes the connected to the training sets that they are associated with. Scripts and training sets are also coupled to meta data, such as instructions as to how training sets are split up for testing and validation, so a model can be reproduced in ideally a deterministic manner if required.</td>
  </tr>
  <tr>
    <td>Providing mechanisms by which changes to training sets, training scripts and service wrappers may all be auditable across their full lifecycle</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Treating training sets as managed assets under a MLOps workflow</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Managing the security of data in the MLOps process with particular focus upon the increased risk associated with aggregated data sets used for training or batch processing</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Implications of privacy, GDPR and the right to be forgotten upon training sets and deployed models</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Methods for wrapping trained models as deployable services in scenarios where data scientists training the models may not be experienced software developers with a background in service-oriented design</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Approaches for enabling all Machine Learning frameworks to be used within the scope of MLOps, regardless of language or platform</td>
    <td>MLOps is a methodology that must be applicable in all environments, using any programming language or framework. Implementations of MLOps tooling may be opinionated about the approach to the methodology but must be agnostic to the underlying technologies used to implement the models and services associated.</br></br>
    It should be possible to use MLOps tooling to deploy solution components utilising different languages or frameworks using loosely-coupled principles to provide compatibility layers.</td>
  </tr>
  <tr>
    <td>Approaches for enabling MLOps to support a broad range of target platforms, including but not limited to CPU, GPU, TPU, custom ASICs and neuromorphic silicon.</td>
    <td>MLOps should be considered as a cross-compilation problem where the architectures of the source and target platforms may be different. In trivial cases, models may be trained on say CPU or GPU and deployed to execute on the same CPU or GPU architecture, however other scenarios already exist and should be expected to be increasingly likely in the future. This may include training on GPU / TPU and executing on CPU or, in edge devices, training on any architecture and then translating the models into physical logic that can be implemented at very low cost / size / power directly on FPGA or ASIC devices.</br></br>
    This implies the need for architecture-independent intermediate formats to facilitate cross-deployment or cross-compilation onto target platforms.</td>
  </tr>
  <tr>
    <td>Methods for ensuring efficient use of hardware in both training and operational scenarios</td>
    <td>ML training and inferencing operations are typically very processing intensive operations that can expect to be accelerated by the use of dedicated hardware. Training is essentially an intermittent ad-hoc process that may run for hours-to-days to complete a single training run, demanding full utilisation of large scale compute resources for this period and then releasing that demand outside active training runs. Similarly, inferencing on a model may be processing intensive during a given execution. Elastic scaling of hardware resources will be essential for minimising cost of ownership however the dedicated nature of existing accelerator cards makes it currently hard to scale these elastically in today's Cloud infrastructure.</br></br>
    Additionally, some accelerators provide the ability to subdivide processing resource into smaller allocation units to allow for efficient allocation of smaller work units within high capacity infrastructure.</br></br>
    It will be necessary to extend the capabilities of existing Cloud platforms to permit more efficient utilisation of expensive compute resources whilst managing overall demand across multiple customers in a way that mitigates security and privacy concerns.</td>
  </tr>
  <tr>
    <td>Approaches for applying MLOps to very large scale problems at petabyte scale and beyond</td>
    <td>As of 2020, large ML data sets are considered to start at around 50TB and very large data sets may derive from petabytes of source data, especially in visual applications such as autonomous vehicle control. At these scales, it becomes necessary to spread ML workloads across thousands of GPU instances in order to keep overall training times within acceptable elapsed time windows (less than a week per run).</br></br>
    Individual GPUs are currently able to process in the order of 1-10GB of data per second but only have around 40GB of local RAM. An individual server can be expected to have around 1TB of conventional RAM and around 15TB of local high speed storage as cache for around 8 GPUs, so may be able to transfer data between these and the compute units at high hundreds of GB/s with upstream connections to network storage running at low hundreds of GB/s.</br></br>
    Efficient workflows rely upon being able to reduce problems into smaller sub-units with constrained data requirements or systems start to become I/O bound. MLOps tooling for large problems must be able to efficiently decompose training and inferencing workloads into individual operations and data sets that can be effectively distributed as parallel activities across a homogeneous infrastructure with a supercomputing-style architecture. This can be expected to exceed the capabilities of conventional Cloud computing infrastructure and require dedicated hardware components and architecture so any MLOps tooling must have appropriate awareness of the target architecture in order to optimise deployments.</br></br>
    At this scale, it is not feasible to create multiple physical copies of petabytes of training data due to storage capacity constraints and limitations of data transfer rates, so strategies for versioning sets of data with metadata against an incrementally growing pool will be necessary.</td>
  </tr>
  <tr>
    <td>Providing appropriate pipeline tools to manage MLOps workflows transparently as part of existing DevOps solutions</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Testing ML assets appropriately</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Governance processes for managing the release cycle of MLOps assets, including Responsible AI principles</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Management of shared dependencies between training and operational phases</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Abstraction layer for models</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Longevity of ML assets</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Managing and tracking trade-offs</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Escalation of data categories</td>
    <td> TBD </td>
  </tr>
  <tr>
    <td>Intrinsic protection of models</td>
    <td> TBD </td>
  </tr>

</table>



# Potential Solutions

> NOTES: Identify potential solutions that could address the challenges above and meet technical requirements.


Show a timeline of potential solutions to set expectations.

**Key:**

<img src="images/key.svg"/>

<img src="images/solutions.svg"/>



# Cross-Cutting Concerns

> NOTES: Identify aspects of MLOps that overlap with issues covered by other SIGs and ensure alignment of work on cross-cutting concerns.

The following cross-cutting concerns are identified:

* CI/CD tooling across DevOps and MLOps scenarios

* Pipeline management

* Common testing aspects such as code coverage, code quality, licence tracking, CVE checking etc.

* Data quality

* Security



# Conclusions and Recommendations

> NOTES: Conclusions and recommendations for the current year.

# Glossary

Short definitions of terms used that aren't explained inline. 

* Training: act of combining data with (hyper) parameters to yield a model
* Model: A deployable (usually binary) artifact that is the result of training. Can be used at runtime to make predictions for example
* Hyperparameter: parameters used during training of a model, typically set by a data scientist/human
* Parameter: a configuration variable set after the training phase (usually part of a model)
* Endpoint: typically a model is deployed to an endpoint which may be a HTTPS service which serves up predictions (models may be also deployed to devices and other places)
* Training Pipeline: all the steps needed to prepare a model
* Training set: a set of example data used for training a model




# References

> NOTES: List of references.


