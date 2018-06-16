{% set chapters = { 
  architecture : {
    name: "architecture", 
    heading: "Architecture",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {name: "", level_three_topics: [{name: "what", heading: "What", priority: "1"}]}
        ]
      },
      {
        name: "architectureDiagrams",
        level_two_topics: [
          {name: "", level_three_topics: [{name: "reading", heading: "Reading", priority: "2"}, {name: "drawing", heading: "Drawing", priority: "3"}]}
        ]
      },
      {
        name: "architecturalStyles",
        level_two_topics: [
          {name: "introduction", level_three_topics: [{name: "what", heading: "What", priority: "1"}]},
          {name: "nTier", level_three_topics: [{name: "what", heading: "What", priority: "2"}]},
          {name: "clientServer", level_three_topics: [{name: "what", heading: "What", priority: "2"}]},
          {name: "transactionProcessing", level_three_topics: [{name: "what", heading: "What", priority: "2"}]},
          {name: "serviceOriented", level_three_topics: [{name: "what", heading: "What", priority: "3"}]},
          {name: "eventDriven", level_three_topics: [{name: "what", heading: "What", priority: "2"}]},
          {name: "more", level_three_topics: [{name: "moreStyles", heading: "More styles", priority: "1"}, {name: "usingStyles", heading: "Using styles", priority: "4"}]}
        ]
      }
    ]
  },
  codeQuality : {
    name: "codeQuality", 
    heading: "Code Quality",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {name: "", level_three_topics: [{name: "basic", heading: "Basic", priority: "1"}]}
        ]
      },
      {
        name: "maximiseReadability",
        level_two_topics: [
          {
            name: "", 
            level_three_topics:[{name: "introduction", heading: "Introduction", priority: "1"}]
          },
          {
            name: "basic", 
            level_three_topics:[
              {name: "avoidLongMethods", heading: "Avoid Long Methods", priority: "1"}, 
              {name: "avoidDeepNesting", heading: "Avoid Deep Nesting", priority: "1"}, 
              {name: "avoidComplicatedExpressions", heading: "Avoid complicated expressions", priority: "1"}, 
              {name: "avoidMagicNumbers", heading: "Avoid Magic Numbers", priority: "1"}, 
              {name: "makeCodeObvious", heading: "Make the Code Obvious", priority: "1"}
            ]
          },
          {
            name: "intermediate", 
            level_three_topics: [
              {name:"structureCodeLogically", heading: "Structure code logically", priority: "2"},
              {name:"dontTripReader", heading: "Do not 'trip up' the reader", priority: "2"},
              {name:"practiceKISSing", heading: "Practice KISSing", priority: "2"},
              {name:"avoidPrematureOptimizations", heading: "Avoid premature optimizations", priority: "2"},
              {name:"slapHard", heading: "SLAP hard", priority: "2"}
            ]
          },
          {
            name: "advanced", 
            level_three_topics: [{name: "makeHappyPathProminent", heading: "Make the happy path prominent", priority: "3"}]
          }
        ]
      },
      {
        name: "followStandard",
        level_two_topics: [
          {
            name: "", 
            level_three_topics:[
              {name: "introduction", heading: "Introduction", priority: "1"},
              {name: "basic", heading: "What", Basic: "2"},
              {name: "intermediate", heading: "Intermediate", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "nameWell",
        level_two_topics: [
          {
            name: "", 
            level_three_topics:[{name: "introduction", heading: "Introduction", priority: "1"}]
          },
          {
            name: "basic", 
            level_three_topics:[
              {name: "nounsAndVerbsAsNames", heading: "Use nouns for things and verbs for actions", priority: "1"}, 
              {name: "useStandardWords", heading: "Use standard words", priority: "1"}
            ]
          },
          {
            name: "intermediate", 
            level_three_topics: [
              {name:"useNameExplain", heading: "Use the name to explain", priority: "1"},
              {name:"notTooLongNorShort", heading: "Not too long, not too short", priority: "1"},
              {name:"avoidMisleadingNames", heading: "Avoid misleading names", priority: "1"}
            ]
          }
        ]
      },
      {
        name: "avoidShortcuts",
        level_two_topics: [
          {
            name: "", 
            level_three_topics:[{name: "introduction", heading: "Introduction", priority: "1"}]
          },
          {
            name: "basic", 
            level_three_topics:[
              {name: "useDefaultBranch", heading: "Use the default branch", priority: "1"}, 
              {name: "dontRecycleVarsOrParams", heading: "Don't recycle variables or parameters", priority: "1"}, 
              {name: "avoidEmptyCatchBlocks", heading: "Avoid empty catch blocks", priority: "1"}, 
              {name: "deleteDeadCode", heading: "Delete dead code", priority: "1"}
            ]
          },
          {
            name: "intermediate", 
            level_three_topics: [
              {name:"minimiseVariableScope", heading: "Minimise variable scope", priority: "2"},
              {name:"minimiseCodeDuplication", heading: "Minimise code duplication", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "commentMinimally",
        level_two_topics: [
          {
            name: "", 
            level_three_topics:[{name: "introduction", heading: "Introduction", priority: "1"}]
          },
          {
            name: "basic", 
            level_three_topics:[
              {name: "dontRepeatObvious", heading: "Don't repeat the obvious", priority: "1"}, 
              {name: "writeToReader", heading: "Write to the reader", priority: "1"}
            ]
          },
          {
            name: "intermediate", 
            level_three_topics: [{name:"explainWhatWhyNotHow", heading: "Explain WHAT and WHY, not HOW", priority: "2"}]
          }
        ]
      }
    ]
  },
  design : {
    name: "design", 
    heading: "Software Design",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {name: "", level_three_topics: [{name: "what", heading: "What", priority: "1"}]}
        ]
      }
    ]
  }
} %}

{% set topics = [
  {heading: "Design", chapters: [chapters.design, chapters.architecture]},
  {heading: "Implementation", chapters: [chapters.codeQuality]}
  ] 
%}