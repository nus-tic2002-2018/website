<frontmatter>
title: "Full Schedule of Module Activities"
footer: footer.md
head: scheduleHead.md
</frontmatter>

{% import "common/outcomes.njk" as outcomes with context %}

{% set weeks = [
    {num: "1", day:"Aug 13"},
    {num: "2", day:"Aug 20"},
    {num: "3", day:"Aug 27"}, 
    {num: "4", day:"Sep 3"},
    {num: "5", day: "Sep 10" },
    {num: "6", day: "Sep 17" },
    {num: "7", day: "Oct 1" },
    {num: "8", day: "Oct 8" },
    {num: "9", day: "Oct 15" },
    {num: "10", day: "Oct 22" },
    {num: "11", day: "Oct 29" },
    {num: "12", day: "Nov 5" },
    {num: "13", day: "Nov 12" }
] %}


{% set current_weeks = ["1", "2"] %}


{% set all_outcomes = [
{week: "1"},
  {name: "SE Intro"},
    {heading: "Can explain pros and cons of software engineering"},
      {location: ["softwareEngineering", "introduction", "prosAndCons"]},
  {name: "Implementation"},
    {heading: "Can explain Java"},
      {location: ["cppToJava", "about"], omit_evidence: true},
      {location: ["cppToJava", "javaWorld", "what"], omit_evidence: true},
      {location: ["cppToJava", "javaWorld", "how"], omit_evidence: true},
      {location: ["cppToJava", "javaWorld", "editions"], omit_evidence: true},
    {heading: "Can do HelloWorld in Java"},
      {location: ["cppToJava", "gettingStarted", "installation"], omit_evidence: true},
      {location: ["cppToJava", "gettingStarted", "helloWorld"], omit_evidence: true},
      {location: ["cppToJava", "gettingStarted", "compiling"], omit_evidence: true},
      {location: ["cppToJava", "gettingStarted", "running"], omit_evidence: true},
    {heading: "Can use data types in Java"},
      {location: ["cppToJava", "dataTypes", "primitiveTypes"], omit_evidence: true},
      {location: ["cppToJava", "dataTypes", "variables"], omit_evidence: true},
      {location: ["cppToJava", "dataTypes", "operators"], omit_evidence: true},
      {location: ["cppToJava", "dataTypes", "arrays"], omit_evidence: true},
    {heading: "Can use basic control flow in Java"},
      {location: ["cppToJava", "controlFlow", "branching"], omit_evidence: true},
      {location: ["cppToJava", "controlFlow", "loops"], omit_evidence: true},
      {location: ["cppToJava", "controlFlow", "methods"], omit_evidence: true},
{week: "2"},
  {name: "OOP"},
    {heading: "Can explain OOP"},
      {location: ["oop", "introduction", "what"], omit_evidence: true},
      {location: ["oop", "objects", "what"]},
      {location: ["oop", "classes", "what"]},
      {location: ["oop", "objects", "abstraction"], omit_evidence: true},
      {location: ["oop", "objects", "encapsulation"], omit_evidence: true},
  {name: "Implementation"},
    {heading: "Can use Java objects"},
      {location: ["cppToJava", "objects", "usingObjects"], omit_evidence: true},
      {location: ["cppToJava", "objects", "instanceMembers"], omit_evidence: true},
      {location: ["cppToJava", "objects", "passingObjects"], omit_evidence: true},
      {location: ["cppToJava", "objects", "garbageCollection"], omit_evidence: true},
    {heading: "Can write Java classes"},
      {location: ["cppToJava", "classes", "definingClasses"], omit_evidence: true},
      {location: ["cppToJava", "classes", "gettersAndSetters"], omit_evidence: true},
      {location: ["cppToJava", "classes", "classLevelMembers"], omit_evidence: true},
    {heading: "Can use some useful Java classes"},
      {location: ["cppToJava", "usefulClasses", "api"], omit_evidence: true},
      {location: ["cppToJava", "usefulClasses", "stringClass"], omit_evidence: true},
      {location: ["cppToJava", "usefulClasses", "wrapperClasses"], omit_evidence: true},
      {location: ["cppToJava", "usefulClasses", "arraysClass"], omit_evidence: true},
      {location: ["cppToJava", "usefulClasses", "scannerClass"], omit_evidence: true},
    {heading: "Can use basic features of an IDE"},
      {location: ["ides", "introduction", "what"]},
      {location: ["intellij", "projectSetup"]},
      {location: ["intellij", "codeNavigation"]},
{week: "3"},
  {name: "OOP"},
    {heading: "Can use inheritance in Java"},
      {location: ["cppToJava", "inheritance", "basic"], omit_evidence: true},
      {location: ["cppToJava", "inheritance", "objectClass"], omit_evidence: true},
      {location: ["cppToJava", "inheritance", "interfaces"], omit_evidence: true},
      {location: ["cppToJava", "inheritance", "polymorphism"], omit_evidence: true},
      {location: ["cppToJava", "inheritance", "abstractClassesAndMethods"], omit_evidence: true},
  {name: "Refactoring"},
    {heading: "Can refactor code at a basic level"},
      {location: ["refactoring", "what"]},
      {location: ["intellij", "refactoring"]},
      {location: ["refactoring", "how"]},
      {location: ["refactoring", "when"]},
  {name: "IDEs"},
    {heading: "Can use intermediate level features of an IDE"},
      {location: ["ides", "debugging", "what"], omit_evidence: true},
      {location: ["intellij", "debuggingBasic"]},
      {location: ["intellij", "productivityShortcuts"]},
  {name: "Revision Control"},
    {heading: "Can communicate with a remote repo"},
      {location: ["revisionControl", "remoteRepositories"], omit_evidence: true},
      {location: ["gitAndGithub", "clone"]},
      {location: ["gitAndGithub", "pull"]},
      {location: ["gitAndGithub", "push"]},
    {heading: "Can traverse Git history"},
      {location: ["revisionControl", "usingHistory"], omit_evidence: true},
      {location: ["gitAndGithub", "checkout"]},
      {location: ["gitAndGithub", "tag"]},
      {location: ["gitAndGithub", "stash"]},
  {name: "Documentation"},
    {heading: "Can use some common documentation tools"},
      {subheading: "Javadoc"},
        {location: ["documentation", "tools", "javaDoc", "what"], omit_evidence: true},
        {location: ["documentation", "tools", "javaDoc", "how"], omit_evidence: true},
      {subheading: "Markdown"},
        {location: ["documentation", "tools", "markdown", "what"], omit_evidence: true},
        {location: ["documentation", "tools", "markdown", "how"], omit_evidence: true},
      {subheading: "AsciiDoc"},
        {location: ["documentation", "tools", "asciiDoc", "what"], omit_evidence: true},
  {name: ":parking: Project"},
    {heading: "Can define the target of a product", priority: "1", file: "project.md#inception"},
    {heading: "Can work with a 1KLoC code base", priority: "1", file: "project.md#1kloc"},
{week: "4"},
  {name: "Implementation"},
    {heading: "Can use exceptions in Java"},
      {location: ["cppToJava", "exceptions", "what"], omit_evidence: true},
      {location: ["cppToJava", "exceptions", "how"], omit_evidence: true},
  {name: "Requirements"},
    {heading: "Can explain requirements"},
      {location: ["requirements", "introduction"], omit_evidence: true},
      {location: ["requirements", "nonFunctionalRequirements"], omit_evidence: true},
      {location: ["requirements", "prioritizing"], omit_evidence: true},
      {location: ["requirements", "quality"], omit_evidence: true},
    {heading: "Can explain some techniques for gathering requirements"},
      {location: ["gatheringRequirements", "brainstorming"], omit_evidence: true},
      {location: ["gatheringRequirements", "productSurveys"], omit_evidence: true},
      {location: ["gatheringRequirements", "observation"], omit_evidence: true},
      {location: ["gatheringRequirements", "userSurveys"], omit_evidence: true},
      {location: ["gatheringRequirements", "interviews"], omit_evidence: true},
      {location: ["gatheringRequirements", "focusGroups"], omit_evidence: true},
      {location: ["gatheringRequirements", "prototyping"], omit_evidence: true},
    {heading: "Can use some techniques for specifying requirements"},
      {subheading: "Prose"},
        {location: ["specifyingRequirements", "prose", "what"], omit_evidence: true},
      {subheading: "Feature Lists"},
        {location: ["specifyingRequirements", "featureList", "what"], omit_evidence: true},
      {subheading: "User Stories"},
        {location: ["specifyingRequirements", "userStories", "introduction"]},
        {location: ["specifyingRequirements", "userStories", "details"], omit_evidence: true},
        {location: ["specifyingRequirements", "userStories", "usage"]},
      {subheading: "Use Cases"},
        {location: ["specifyingRequirements", "useCases", "introduction"], omit_evidence: true},
      {subheading: "Glossary"},
        {location: ["specifyingRequirements", "glossary", "what"], omit_evidence: true},
      {subheading: "Supplementary Requirements"},
        {location: ["specifyingRequirements", "supplementaryRequirements", "what"], omit_evidence: true},
  {name: "Design"},
    {heading: "Can explain models"},
      {location: ["modeling", "introduction", "what"], omit_evidence: true},
      {location: ["modeling", "introduction", "how"]},
    {heading: "Can explain basic object/class structures"},
      {location: ["modeling", "modelingStructures", "ooStructures"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "classDiagramsBasic"]},
      {location: ["uml", "miscellaneous", "objectVsClassDiagrams"], omit_evidence: true},
    {heading: "Can explain single responsibility principle"},
      {location: ["principles", "singleResponsibilityPrinciple"]},
  {name: "Implementation"},
    {heading: "Can implement classes"},
    {heading: "Can do exception handling in code"},
      {location: ["errorHandling", "introduction", "what"], omit_evidence: true},
      {location: ["errorHandling", "exceptions", "what"], omit_evidence: true},
      {location: ["errorHandling", "exceptions", "how"]},
      {location: ["errorHandling", "exceptions", "when"], omit_evidence: true},
    {heading: "Can use Java enumerations"},
      {location: ["oop", "classes", "enumerations"]},
      {location: ["javaTools", "enums"]},
  {name: "Project Management"},
    {heading: "Can create PRs on GitHub"},
      {location: ["revisionControl", "branching"]},
      {location: ["gitAndGithub", "branch"]},
      {location: ["gitAndGithub", "createPRs"]},
  {name: ":parking: Project"},
    {heading: "Can define requirements of a product", priority: "1", file: "project.md#v10"},
{week: "5"},
  {name: "Java"},
    {heading: "Can use Generics in Java"},
      {location: ["cppToJava", "generics", "what"], omit_evidence: true},
      {location: ["cppToJava", "generics", "how"], omit_evidence: true},
    {heading: "Can use Collections in Java"},
      {location: ["cppToJava", "collections", "what"]},
      {location: ["cppToJava", "collections", "arrayListClass"], omit_evidence: true},
      {location: ["cppToJava", "collections", "hashMapClass"], omit_evidence: true},
  {name: "Requirements"},
    {heading: "Can apply basic product design guidelines", priority: "3", file: "project.md#product_design"},
  {name: "Implementation"},
    {heading: "Can implement inheritance"},
      {location: ["oop", "inheritance", "what"], omit_evidence: true},
    {heading: "Can implement class-level members"},
      {location: ["oop", "classes", "classLevelMembers"], omit_evidence: true},
      {location: ["oop", "inheritance", "overloading"], omit_evidence: true},
    {heading: "Can implement overloading"},
    {heading: "Can implement polymorphism"},
      {subheading: "Method Overriding"},
        {location: ["oop", "inheritance", "overriding"], omit_evidence: true},
      {subheading: "Polymorphism"},
        {location: ["oop", "polymorphism", "what"], omit_evidence: true},
      {subheading: "Abstract Classes"},
        {location: ["oop", "inheritance", "abstractClasses"], omit_evidence: true},
      {subheading: "Interfaces"},
        {location: ["oop", "inheritance", "interfaces"], omit_evidence: true},
  {name: "Quality Assurance"},
    {heading: "Can use simple JUnit tests"},
      {location: ["testing", "testingTypes", "developerTesting", "what"], omit_evidence: true},
      {location: ["testing", "testingTypes", "developerTesting", "why"]},
      {location: ["testing", "testAutomation", "usingTestDrivers"], omit_evidence: true},
      {location: ["testing", "testAutomation", "tools"], omit_evidence: true},
      {location: ["junit", "basic"]},
  {name: "Project Management"},
    {heading: "Can use GitHub PRs in a workflow"},
      {location: ["gitAndGithub", "mergeConflicts"]},
      {location: ["gitAndGithub", "managePRs"]},
    {heading: "Can follow Forking Workflow"},
      {location: ["revisionControl", "forkingWorkflow"], omit_evidence: true},
      {location: ["gitAndGithub", "forkingWorkflow"]},
      {location: ["revisionControl", "drcsVsCrcs"], omit_evidence: true},
      {location: ["revisionControl", "featureBranchFlow"], omit_evidence: true},
      {location: ["revisionControl", "centralizedFlow"], omit_evidence: true},
  {name: ":parking: Project"},
    {heading: "Can work with a 2KLoC code base", priority: "1", file: "project.md#2kloc"},
    {heading: "Can conceptualize a product", priority: "1", file: "project.md#v10"},
{week: "6"},
  {name: "Design"},
    {heading: "???"},
      {location: ["design", "introduction", "what"], omit_evidence: true},
    {heading: "Can use intermediate-level class diagrams"},
      {location: ["uml", "classDiagrams", "dependencies", "what"], omit_evidence: true},
      {location: ["uml", "notes", "notes"], omit_evidence: true},
      {location: ["uml", "notes", "constraints"], omit_evidence: true},
      {location: ["uml", "classDiagrams", "associationsAsAttributes", "what"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "classDiagramsIntermediate"], omit_evidence: true},
    {heading: "Can interpret basic sequence diagrams"},
      {location: ["uml", "sequenceDiagrams", "introduction"], omit_evidence: true},
      {location: ["uml", "sequenceDiagrams", "basic"], omit_evidence: true},
      {location: ["uml", "sequenceDiagrams", "loops"], omit_evidence: true},
      {location: ["uml", "sequenceDiagrams", "objectCreation"], omit_evidence: true},
      {location: ["uml", "sequenceDiagrams", "minimalNotation"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "sequenceDiagramsBasic"]},
  {name: "Implementation"},
    {heading: "Can implement composition"},
      {location: ["oop", "associations", "composition"], omit_evidence: true},
    {heading: "Can implement aggregation"},
      {location: ["oop", "associations", "aggregation"], omit_evidence: true},
    {heading: "Can use logging"},
      {location: ["errorHandling", "logging", "what"], omit_evidence: true},
      {location: ["errorHandling", "logging", "how"]},
    {heading: "Can use assertions"},
      {location: ["errorHandling", "assertions", "what"], omit_evidence: true},
      {location: ["errorHandling", "assertions", "how"]},
      {location: ["errorHandling", "assertions", "when"]},
    {heading: "Can use Java8 streams"},
      {location: ["javaTools", "streamsBasic"]},
    {heading: "Can use JavaFX to build a simple GUI"},
      {location: ["javaTools", "javaFXBasic"]},
  {name: ":parking: Project"},
    {heading: "Can contribute to project documentation", priority: "1", file: "project.md#mid-v11"},
{week: "7"},
  {name: "Design"},
    {heading: "Can explain APIs"},
      {location: ["reuse", "apis", "what"]},
    {heading: "Can use intermediate-level sequence diagrams"},
      {location: ["uml", "sequenceDiagrams", "objectDeletion"], omit_evidence: true},
      {location: ["uml", "sequenceDiagrams", "selfInvocation"], omit_evidence: true},
      {location: ["uml", "sequenceDiagrams", "alternativePaths"], omit_evidence: true},
      {location: ["uml", "sequenceDiagrams", "optionalPaths"], omit_evidence: true},
      {location: ["uml", "sequenceDiagrams", "referenceFrames"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "sequenceDiagramsIntermediate"]},
      {location: ["uml", "sequenceDiagrams", "parallelPaths"], omit_evidence: true},
  {name: "Implementation"},
    {heading: "Can follow a simple style guide"},
      {location: ["codeQuality", "introduction", "basic"], omit_evidence: true},
      {location: ["codeQuality", "followStandard", "introduction"]},
      {location: ["codeQuality", "followStandard", "basic"]},
      {location: ["codeQuality", "followStandard", "intermediate"]},
    {heading: "Can improve code readability"},
      {location: ["codeQuality", "maximiseReadability", "introduction"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidLongMethods"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidDeepNesting"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidComplicatedExpressions"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidMagicNumbers"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "basic", "makeCodeObvious"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "structureCodeLogically"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "dontTripReader"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "practiceKISSing"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "avoidPrematureOptimizations"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "slapHard"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "advanced", "makeHappyPathProminent"], omit_evidence: true},
    {heading: "Can use good naming"},
      {location: ["codeQuality", "nameWell", "introduction"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "basic", "nounsAndVerbsAsNames"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "basic", "useStandardWords"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "intermediate", "useNameExplain"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "intermediate", "notTooLongNorShort"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "intermediate", "avoidMisleadingNames"], omit_evidence: true},
    {heading: "Can write good code comments"},
      {location: ["codeQuality", "commentMinimally", "introduction"], omit_evidence: true},
      {location: ["codeQuality", "commentMinimally", "basic", "dontRepeatObvious"], omit_evidence: true},
      {location: ["codeQuality", "commentMinimally", "basic", "writeToReader"], omit_evidence: true},
      {location: ["codeQuality", "commentMinimally", "intermediate", "explainWhatWhyNotHow"], omit_evidence: true},
  {name: ":parking: Project"},
    {heading: "Can do small changes to an existing software", priority: "1", file: "project.md#v11"},
{week: "8"},
  {name: "Design"},
    {heading: "Can use basic software design principles"},
      {subheading: "Abstraction"},
        {location: ["designFundamentals", "abstraction", "what"], omit_evidence: true},
      {subheading: "SoC and OCP"},
        {location: ["principles", "separationOfConcernsPrinciple"]},
        {location: ["principles", "openClosedPrinciple"]},
  {name: "Implementation"},
    {heading: "Can implement association classes"},
      {location: ["oop", "associations", "associationClasses"]},
  {name: "Quality Assurance"},
    {heading: "Can explain different types of testing"},
      {subheading: "Unit Testing"},
        {location: ["testing", "testingTypes", "unitTesting", "what"]},
        {location: ["testing", "testingTypes", "unitTesting", "stubs"]},
      {subheading: "Integration Testing"},
        {location: ["testing", "testingTypes", "integrationTesting", "what"]},
        {location: ["testing", "testingTypes", "integrationTesting", "how"]},
      {subheading: "System Testing"},
        {location: ["testing", "testingTypes", "systemTesting", "what"]},
        {location: ["testing", "testAutomation", "testingGuis"]},
      {subheading: "Acceptance Testing"},
        {location: ["testing", "testingTypes", "acceptanceTesting", "what"]},
        {location: ["testing", "testingTypes", "acceptanceTesting", "acceptanceVsSystemTesting"]},
      {subheading: "Alpha/Beta Testing"},
        {location: ["testing", "testingTypes", "alphaBetaTesting", "what"]},
  {name: "Project Management"},
    {heading: "Can use basic scheduling and tracking tools"},
      {location: ["projectPlanning", "milestones"]},
      {location: ["projectPlanning", "buffers"]},
      {location: ["projectPlanning", "issueTrackers"]},
      {location: ["projectPlanning", "workBreakdownStructure"]},
      {location: ["projectPlanning", "ganttCharts"], omit_evidence: true},
      {location: ["projectPlanning", "pertCharts"], omit_evidence: true},
      {location: ["teamwork", "teamStructures"]},
  {name: ":parking: Project"},
    {heading: "Can plan/track project schedule", priority: "1", file: "project.md#mid-v12"},
{week: "9"},
  {name: "Design"},
    {heading: "Can use intermediate-level design principles"},
      {subheading: "How Polymorphism Works"},
        {location: ["oop", "inheritance", "substitutability"], omit_evidence: true},
        {location: ["oop", "inheritance", "dynamicAndStaticBinding"], omit_evidence: true},
        {location: ["oop", "polymorphism", "how"]},
      {subheading: "More Design Principles"},
        {location: ["principles", "liskovSubstitutionPrinciple"]},
  {name: "Quality Assurance"},
    {heading: "Can use intermediate-level testing techniques"},
      {location: ["testing", "introduction", "testability"], omit_evidence: true},
      {location: ["junit", "intermediate"]},
    {heading: "Can explain some QA techniques complementary to testing"},
      {location: ["qualityAssurance", "introduction", "what"], omit_evidence: true},
      {location: ["qualityAssurance", "introduction", "validationVsVerification"]},
      {location: ["qualityAssurance", "codeReviews", "what"]},
      {location: ["qualityAssurance", "staticAnalysis", "what"]},
      {location: ["qualityAssurance", "formalVerification", "what"], omit_evidence: true},
  {name: ":parking: Project"},
    {heading: "Can write developer documentation", priority: "1", file: "project.md#v12"},
{week: "10"},
  {name: "SE"},
    {heading: "Can explain SE principles"},
      {location: ["principles", "lawOfDemeter"]},
      {location: ["principles", "yagniPrinciple"], omit_evidence: true},
      {location: ["principles", "dryPrinciple"], omit_evidence: true},
      {location: ["principles", "brooksLaw"], omit_evidence: true},
  {name: "Implementation"},
    {heading: "Can get reuse benefits from frameworks, libraries, and platforms"},
      {subheading: "Reuse"},
        {location: ["reuse", "introduction", "what"], omit_evidence: true},
        {location: ["reuse", "introduction", "when"]},
      {subheading: "Libraries"},
        {location: ["reuse", "libraries", "what"]},
        {location: ["reuse", "libraries", "how"]},
      {subheading: "Frameworks"},
        {location: ["reuse", "frameworks", "what"]},
        {location: ["reuse", "frameworks", "frameworksVsLibraries"]},
      {subheading: "Platforms"},
        {location: ["reuse", "platforms", "what"]},
  {name: ":parking: Project"},
    {heading: "Can evolve a product incrementally", priority: "1", file: "project.md#mid-v13"},
{week: "11"},
  {name: "Requirements"},
    {heading: "Can explain object oriented domain models"},
      {location: ["modeling", "modelingStructures", "objectOrientedDomainModels"], omit_evidence: true},
  {name: ":parking: Project"},
    {heading: "Can release a product incrementally", priority: "1", file: "project.md#v13"},
{week: "12"},
  {name: "Design"},
    {heading: "Can explain some UML models"},
      {location: ["modeling", "modelingStructures", "deploymentDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "componentDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "packageDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "compositeStructureDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "timingDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "interactionOverviewDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "communicationDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "stateMachineDiagrams"], omit_evidence: true},
  {name: ":parking: Project"},
    {heading: "Can describe a technical contribution", priority: "1", file: "project.md#mid-v14"},
{week: "13"},
  {name: ":parking: Project"},
    {heading: "Can acceptance-test a product", priority: "1", file: "project.md#v14"},
    {heading: "Can evaluate a technical effort", priority: "1", file: "project.md#v14"},
    {heading: "Can demo a product", priority: "1", file: "project.md#v14"}
]%}


{% macro show_week_outcomes(week_num, path="") %}
<panel type="seamless" popup-url="{{baseUrl}}/schedule/week{{ week_num }}/outcomes.html" expanded no-close>
  <span slot="header" class="card-title activity-type">{{ icon_outcome }} Outcomes</span>
  <div class="indented">
  {{ outcomes.show_week_schedule_main(week_num, all_outcomes, path) }}
  </div>
</panel>
{% endmacro %}


{% macro show_week_todos(week_num, path="") %}
<panel type="seamless" expanded no-close>
  <span slot="header" class="card-title activity-type">{{ icon_todo }} Todo</span>
  <div class="indented">
  <include src="{{ path }}todo.md" />
  </div>
</panel>
{% endmacro %}


{% macro show_week_tutorial(week_num, path="") %}
<panel type="seamless" expanded no-close>
<span slot="header" class="card-title activity-type">{{ icon_tutorial }} Tutorial {{ week_num }}</span>
   <div class="indented">
   <include src="{{ path }}tutorial.md" />
   </div>
</panel>
{% endmacro %}


{% macro show_week_lecture(week_num, path="") %}
<panel type="seamless" expanded no-close>
<span slot="header" class="card-title activity-type">{{ icon_lecture }} Lecture {{ week_num }}</span>
  <div class="indented">
  <include src="{{ path }}lecture.md" />
  </div>
</panel>
{% endmacro %}


{% macro show_week_schedule(week_num, path="") %}
{{ show_week_todos(week_num, path) }}
{{ show_week_outcomes(week_num, path) }}
{{ show_week_tutorial(week_num, path) }}
{{ show_week_lecture(week_num, path) }}

{% endmacro %}


{% macro show_past_week(week) %}
<panel type="seamless" src="week{{ week.num }}/index.md" no-close>
<span slot="header" class="card-title week-past"> Week {{ week.num }} [{{ week.day }}]</span>
</panel>
{% endmacro %}


{% macro show_future_week(week) %}
<panel type="seamless" src="week{{ week.num }}/index.md" no-close>
<span slot="header" class="card-title week-future"> Week {{ week.num }} [{{ week.day }}]</span>
</panel>
{% endmacro %}


{% macro show_current_week(week) %}
<panel type="seamless" src="week{{ week.num }}/index.md" no-close>
<span slot="header" class="card-title week"> Week {{ week.num }} [{{ week.day }}]</span>
</panel>
{% endmacro %}

<!-- ============================= page content ============================================ -->

<include src="../common/header.md" />

<div class="website-content" id="main">

# Full Schedule of Module Activities

<panel src="overview/index.md" header=":exclamation: **Info relevant to all weeks**"  />
<panel src="../admin/tutorials.md#tutorialTimetable" header="**{{glyphicon_calendar}} Tutorial Timetable**" />

<p/>

{% for week in weeks %}
{% set current_week_num = current_weeks[0] | int %}
{% set week_num = week.num | int %}
{% if week.num in current_weeks %} 
  {{ show_current_week(week) }}
{% elseif week_num < current_week_num %}
  {{ show_past_week(week) }}
{% else %}
  {{ show_future_week(week) }}
{% endif %}
{% endfor %}


</div>