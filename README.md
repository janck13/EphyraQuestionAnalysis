EphyraQuestionAnalysis
======================

A collection of [OpenEphyra](http://sourceforge.net/projects/openephyra/) components necessary for question analysis. **Dependencies**: Java, Maven, WordNet. **You may need to set the right locale**, see [build.sh](build.sh). Unlike initial versions relying on LTI repositories, this is a self-sufficient one. The original OpenEphyra license is **GNU General Public License version 2.0 (GPLv2)**.

Most of the existing functionality can be initialized by calling the function [EphyraPart.initBasic](src/main/java/info/ephyra/EphyraPart.java#L23). Then, you can extract answer types and foci. An example of doing so is in [QuestionAnalysis.java](src/main/java/info/ephyra/questionanalysis/QuestionAnalysis.java#L260). This class can be invoked by calling the script [run_question_analysis.sh](run_question_analysis.sh).

One unpleasant limitation, though, is that the old system is not Maven ready: it uses additional resources in ``res`` and ``conf`` folders that are not loaded as Java resources. Therefore, these folders cannot be installed to a Maven repository, they need to be copied to one's working directory.

