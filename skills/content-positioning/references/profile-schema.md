# Profile Schemas

Use these fields as the semantic contract. The host application may store them in a database instead of literal files.

## Private Positioning Profile

```json
{
  "schemaVersion": 1,
  "profileId": "",
  "ownerId": "",
  "visibility": "private",
  "status": "draft|confirmed",
  "sourceFacts": {
    "identity": "",
    "domain": "",
    "goals": [],
    "credibleAdvantages": [],
    "proof": [],
    "primaryAudience": {
      "identity": "",
      "stage": "",
      "painPoints": [],
      "desiredOutcome": "",
      "sophistication": ""
    },
    "secondaryAudiences": [],
    "businessPath": [],
    "platforms": [],
    "voice": {
      "adjectives": [],
      "phrasesToUse": [],
      "phrasesToAvoid": []
    },
    "boundaries": {
      "excludedTopics": [],
      "excludedAudiences": [],
      "claimsToAvoid": []
    }
  },
  "selectedStrategy": {
    "name": "",
    "type": "accessible|authority|outcome|custom",
    "coreProblem": "",
    "promisedTransformation": "",
    "creatorRole": "",
    "credibilityBasis": [],
    "positioningStatement": "",
    "contentPillars": [
      {"name": "", "angle": "", "subtopics": []}
    ],
    "preferredPrototypes": [],
    "businessPath": "",
    "advantages": [],
    "risks": [],
    "assumptions": [],
    "scores": {}
  },
  "creatorHandoff": {
    "audience": "",
    "corePromise": "",
    "credibilityEvidence": [],
    "contentPillars": [],
    "preferredPrototypes": [],
    "tone": [],
    "excludedTopics": [],
    "defaultDurationSeconds": null,
    "conversionGoal": ""
  },
  "incompleteFields": [],
  "versions": [
    {"version": 1, "date": "YYYY-MM-DD", "summary": "Initial confirmed positioning"}
  ]
}
```

## Public Template

```json
{
  "schemaVersion": 1,
  "templateId": "",
  "name": "",
  "description": "",
  "visibility": "public",
  "creatorDisplayName": "",
  "sourceTemplateId": null,
  "version": 1,
  "usageTerms": "",
  "applicableCreators": [],
  "audienceModel": {
    "identity": "",
    "stage": "",
    "commonPainPoints": [],
    "desiredOutcomePattern": ""
  },
  "strategyType": "",
  "positioningPattern": "",
  "contentPillarTemplates": [
    {"name": "", "anglePrompt": "", "subtopicPrompts": []}
  ],
  "recommendedPrototypes": [],
  "sampleTopics": [],
  "setupQuestions": [],
  "sanitizationConfirmed": false
}
```

## Privacy Rules

Never copy these fields from a private profile into a public template unless the user explicitly supplies them for publication:

- Owner identifiers and contact details
- Client identities or confidential case details
- Private revenue, conversion, or audience targets
- Unpublished proof and personal examples
- Verbatim notes from the positioning interview

Templates must express reusable patterns, not impersonate their original creator.
