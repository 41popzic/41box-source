# Slarmoo's Box Contributions

Hello! Slarmoo's Box is and always will be open source, and one of the benefits of that is other people can contribute to the codebase

To help keep things organized, here are some steps and standards that you should follow when contributing:
## 1. Location of Contribution
- The first thing you should consider is where to send your change:
- Small bugfixes, grammar or spelling corrections, etc should be submitted to [The Main Repository](https://github.com/slarmoo/slarmoosbox) so that users can access them as soon as possible. 
- However, Large bugfixes (especially breaking* ones), new features, or things of similar nature should be submitted to [The Testing Repostiory](https://github.com/slarmoo/slarmoosboxtesting) so that they can be tested first and to bundle them with other changes**. 
- Finally, as a fork, Slarmoo's Box is built on the shoulders of other mods. Thus, in many cases a bug or unintended behavior is inherited from them. In this case, it's recommended that you send your bugfix there. Sampling fixes for example should be made to [The Ultrabox Repository](https://github.com/ultraabox/ultrabox_typescript). 

## 2. Tests
- When you submit a contribution, please make sure that it works first. For a bugfix, this means testing that the bug is indeed fixed, and does not create any unintended side effects. For a feature this should a lot more intensive, but doesn't need to be perfect since we have community testing on The Testing Repository. 
- Some things to check when you make a contribution are: 
    - Does the ui render properly after prolonged use and interaction? 
    - Are there any edge cases with slider values that cause the synth to break?
    - Does this work properly on every instrument type / effect / envelope?
    - How does it look for different layouts? For different screen widths? For mobile?

## 3. Committing
- Please include only one feature per contribution so that I can more easily review your code. 
    - This does not apply if newer feature contributions need to build upon older ones
- Most of your commit names can be done however you please. However, I request that your final big one has a clear and descriptive name that says what you added. You can then add fixing commits on top of this that state what they fixed. 

## 4. Style
- While I don't have any true style guide for how you should write your code, I do request that you don't needlessly change the structure or formatting of old code to keep your changes easy to review. 

## 5. Responsibility
- When you make a contribution, you are affecting the many users that create in Slarmoo's Box. The hope is that this is for the better. These guidelines are here to help that to be the case. 
- If something *does* go awry because of a contribution you made, I may reach out to you for help to solve the issue
- Finally, this is not a final document. Things may change in here over time, and it is your responsibility to stay up to date with the standards listed here

Thank you for helping to contribute to Slarmoo's Box, and the greater Beepbox community <3

## Appendix of Terms
A list of terms used in this document and conversation about contributing to Slarmoo's Box
### Breaking: 
A change to how the synth works that adjusts how sound is generated in a way that causes a discrepancy between updates. An example of this is how song detune affects envelopes. It's an unintended behavior that should be fixed, but because old songs are built within this framework, making this change affects how old songs sound. 
Breaking changes should be handled with care and discussion. Sometimes the right move is to add a toggle. Other times it's to change it anyways and provide an [archived](https://slarmoo.github.io/slarmoosbox/archive/) version. And still other times it's to leave it alone for now. 
### Bundling with other Changes
Many feature additions require more information to be stored in the url. While in and of itself this is not a bad thing, in order to properly parse urls we need to provide a version number in the url and write a lot of if/else statements based on this version. The more versions we add, the more complex the code gets. Thus, it's recommended that features that change the url are all added in batches to reduce version parsing. 