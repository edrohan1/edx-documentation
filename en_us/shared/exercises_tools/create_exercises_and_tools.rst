.. _Create Exercises:

############################
Exercises and Tools
############################

You can add a wide variety of different types of exercises and tools to your
course outline. By default, a core set of exercises is available for you to add
to your course. There are also numerous additional exercises and tools that you
can review and add to your course.

The level of support that edX provides for each tool varies. The description of
each exercise and tool indicates the level of support: full, provisional or no
support.

Exercises and tools with provisional support might lack the robustness of
functionality that courses you build using edX require. Exercises and tools
with no support are not maintained by edX, and might be deprecated in the
future.

.. contents::
  :local:
  :depth: 1

************************************
Introduction to Exercises and Tools
************************************

"Exercises and tools" is a general way to refer to the robust variety of
content that you can integrate into an online course. The graded and ungraded
assessments in your course use different types of exercises or problems, while
various tools deliver different types of course content. Software developers
use the XBlock component architecture to contribute new exercises and tools to
the Open edX platform and provide new and varied options for reaching learners.

* You might need to explicitly enable an exercise or tool that you want to use
  in your course. For more information, see :ref:`Enable Additional Exercises
  and Tools`.

* After you enable an exercise or tool for use with your course, when you add a
  component to a unit, that exercise or tool might be listed as an
  **Advanced**, **HTML**, or **Problem** option for the component.

The topics in this section describe different exercises and tools. Information
about how to enable specific exercises and tools is provided, followed by
examples and step-by-step instructions for how you use Studio to add components
to your course. For many of the exercises and tools, when you add a component
Studio presents a template for you to use as a starting point for your work.
XML examples and descriptions of the attributes, tags, and elements that you
can use in an XML editor are also provided.

.. note:: When you create problems, you must include labels for accessibility.
   Accessible labels generally include the text of the main question in your
   problem. Instructions for adding labels appear in the page for each
   individual problem.

****************************
General Exercises and Tools
****************************

.. only:: Open_edX

  .. note:: In addition to the following exercises and tools, Open edX offers
   the :ref:`Notes tool<Notes Tool>`. The Notes tool allows learners to
   highlight and make notes about what they read in the courseware. This tool
   is not available for courses on edx.org.

.. list-table::
   :widths: 25 60 20
   :header-rows: 1

   * - Type
     - Description
     - Support
   * - :ref:`Annotation`
     - Annotation problems ask students to respond to questions about a
       specific block of text. The question appears above the text when the
       student hovers the mouse over the highlighted text so that students can
       think about the question as they read.
     - Provisional support
   * - :ref:`Calculator`
     - The calculator tool is available for every course through the course
       advanced settings. When the calculator tool is enabled, it appears on
       every courseware page. Learners can enter input that includes Greek
       letters, trigonometric functions, and scientific or ``e`` notation in
       addition to common operators.
     - Provisional support
   * - :ref:`Conditional Module`
     - You can create a conditional module to control versions of content that
       groups of students see. For example, students who answer "Yes" to a poll
       question then see a different block of text from the students who answer
       "No" to that question.
     - Provisional support
   * - :ref:`Custom JavaScript`
     - Custom JavaScript display and grading problems (also called *custom
       JavaScript problems* or *JS Input problems*) allow you to create a
       custom problem or tool that uses JavaScript and then add the problem or
       tool directly into Studio.
     - Full support
   * - :ref:`External Grader`
     - An external grader is a service that receives student responses to a
       problem, processes those responses, and returns feedback and a problem
       grade to the edX platform. You build and deploy an external grader
       separately from the edX platform. An external grader is particularly
       useful for software programming courses where students are asked to
       submit complex code.
     - Provisional support
   * - :ref:`Google Calendar Tool`
     - You can embed a Google calendar in your course so that students see the
       calendar in the courseware. You can use a Google calendar to share quiz
       dates, office hours, or other schedules of interest to students.
     - Full support
   * - :ref:`Google Drive Files Tool`
     - You can embed a Google Drive file, such as a document, spreadsheet, or
       image, in your course so that students see the file in the courseware.
     - Full support
   * - :ref:`Google Instant Hangout`
     - You can add the ability for students to participate in instant hangouts
       directly from your course. With instant hangouts, students can interact
       through live video and voice, share screens and watch videos together,
       and collaborate on documents.
     - Provisional support
   * - :ref:`IFrame`
     - IFrames allow you to integrate ungraded exercises and tools from any
       Internet site into an HTML component in your course.
     - Provisional support
   * - :ref:`LTI Component`
     - LTI components allow you to add an external learning application or non-
       PDF textbook to Studio.
     - Full support
   * - :ref:`Open Response Assessments 2`
     - In open response assessments, students receive feedback on written
       responses of varying lengths as well as image files that the students
       upload. Open response assessments include self assessment and peer
       assessment.
     - Full support
   * - :ref:`Oppia Exploration Tool`
     - You can embed Oppia explorations in your course so that learners can
       interact with them directly in the courseware.
     - Full support
   * - :ref:`Poll Tool`
     - You can include polls in your course to gather learners' opinions on
       various questions. You can use the Poll Tool in Studio.
     - Full support
   * - :ref:`Poll`
     - You can run polls in your course so that your students can share
       opinions on different questions. You can use this type of poll only in
       OLX, not Studio.
     - Provisional support
   * - :ref:`Problem with Adaptive Hint`
     - A problem with an adaptive hint evaluates a student's response, then
       gives the student feedback or a hint based on that response so that the
       student is more likely to answer correctly on the next attempt. These
       problems can be text input or multiple choice problems.
     - Provisional support
   * - :ref:`Problem Written in LaTeX`
     - If you have a problem that is already written in LaTeX, you can use
       this problem type to easily convert your code into XML.
     - No support
   * - :ref:`Qualtrics Survey`
     - You can import surveys that you have created in Qualtrics. The survey
       appears inside an IFrame in your course.
     - Full support
   * - :ref:`Survey Tool`
     - You can include surveys in your course to collect learner responses to
       multiple questions. You can use the Survey Tool in Studio.
     - Full support
   * - :ref:`Text Input`
     - In text input problems, students enter text into a response field. The
       response can include numbers, letters, and special characters such as
       punctuation marks.
     - Full support
   * - :ref:`Word Cloud`
     - Word clouds arrange text that students enter - for example, in response
       to a question - into a colorful graphic that students can see.
     - Provisional support
   * - :ref:`Write Your Own Grader`
     - In custom Python-evaluated input (also called "write-your-own-grader")
       problems, the grader uses a Python script that you create and embed in
       the problem to evaluates a student's response or provide hints. These
       problems can be any type.
     - Provisional support
   * - :ref:`RecommenderXBlock`
     - RecommenderXBlock can hold a list of resources for misconception
       remediation, additional reading, and so on. This tool allows the
       course team and students to work together to maintain the list of
       resources. For example, team members and students can suggest new
       resources, vote for useful ones, or flag abuse and spam.
     - Full support

********************************
Image-Based Exercises and Tools
********************************

.. list-table::
   :widths: 25 60 20
   :header-rows: 1

   * - Type
     - Description
     - Support
   * - :ref:`Drag and Drop`
     - In drag and drop problems, students respond to a question by dragging
       text or objects to a specific location on an image.
     - Provisional support
   * - :ref:`Full Screen Image`
     - The Full Screen Image tool allows a student to enlarge an image in the
       whole browser window. This is useful when the image contains a large
       amount of detail and text that is easier to view in context when
       enlarged.
     - Full support
   * - :ref:`Image Mapped Input`
     - In an image mapped input problem, students click inside a defined area
       in an image. You define this area by including coordinates in the body
       of the problem.
     - Provisional support
   * - :ref:`Zooming Image`
     - Zooming images allow you to enlarge sections of an image so that
       students can see the section in detail.
     - Full support

************************************
Multiple Choice Exercises and Tools
************************************

.. list-table::
   :widths: 25 60 20
   :header-rows: 1

   * - Type
     - Description
     - Support
   * - :ref:`Checkbox`
     - In checkbox problems, the student selects one or more options from a
       list of possible answers. The student must select all the options that
       apply to answer the problem correctly.
     - Full support
   * - :ref:`Dropdown`
     - Dropdown problems allow the student to choose from a collection of
       answer options, presented as a dropdown list. Unlike multiple choice
       problems, whose answers are always visible directly below the question,
       dropdown problems don't show answer choices until the student clicks the
       dropdown arrow.
     - Full support
   * - :ref:`Multiple Choice`
     - In multiple choice problems, students select one option from a list of
       answer options. Unlike with dropdown problems, whose answer choices
       don't appear until the student clicks the drop-down arrow, answer
       choices for multiple choice problems are always visible directly below
       the question.
     - Full support
   * - :ref:`Multiple Choice and Numerical Input`
     - You can create a problem that combines a multiple choice and numerical
       input problems. Students not only select a response from options that
       you provide, but also provide more specific information, if necessary.
     - Provisional support

********************************
STEM Exercises and Tools
********************************

.. list-table::
   :widths: 25 60 20
   :header-rows: 1

   * - Type
     - Description
     - Support
   * - :ref:`Chemical Equation`
     - Chemical equation problems allow the student to enter text that
       represents a chemical equation into a text box. The grader evaluates the
       student's response by using a Python script that you create and embed in
       the problem.
     - Full support
   * - :ref:`Circuit Schematic Builder`
     - In circuit schematic builder problems, students can arrange circuit
       elements such as voltage sources, capacitors, resistors, and MOSFETs on
       an interactive grid. They then submit a DC, AC, or transient analysis of
       their circuit to the system for grading.
     - Provisional support
   * - :ref:`Gene Explorer`
     - The Gene Explorer (GeneX) simulates the transcription, splicing,
       processing, and translation of a small hypothetical eukaryotic gene.
       GeneX allows students to make specific mutations in a gene sequence, and
       it then calculates and displays the effects of the mutations on the mRNA
       and protein.
     - Provisional support
   * - :ref:`Math Expression Input`
     - The more complex of Studio's two types of math problems. In math
       expression input problems, students enter mathematical expressions to
       answer a question. These problems can include unknown variables and more
       complex symbolic expressions. You can specify a correct answer either
       explicitly or by using a Python script.
     - Full support
   * - :ref:`Molecule Editor`
     - The molecule editor allows students to draw molecules that follow the
       rules for covalent bond formation and formal charge, even if the
       molecules are chemically impossible, are unstable, or do not exist in
       living systems.
     - No support
   * - :ref:`Molecule Viewer`
     - The molecule viewer allows you to create three-dimensional
       representations of molecules for students to view.
     - No support
   * - :ref:`Numerical Input`
     - The simpler of Studio's two types of math problems. In numerical input
       problems, students enter numbers or specific and relatively simple
       mathematical expressions to answer a question. These problems only allow
       integers and a few select constants. You can specify a margin of error,
       and you can specify a correct answer either explicitly or by using a
       Python script.
     - Full support
   * - :ref:`Periodic Table`
     - An interactive periodic table of the elements shows detailed information
       about each element as the student moves the mouse over the element.
     - No support
   * - :ref:`Protein Builder`
     - The Protex protein builder asks students to create specified protein
       shapes by stringing together amino acids.
     - No support

.. The following section lists the types of problems that learners can interact with in the edX mobile app.
.. Alison, DOC-1840, June 2015

.. only:: Open_edX

  *********************************
  Mobile-Ready Problem Types
  *********************************

  .. include:: ../../../shared/exercises_tools/Section_mobile_problems.rst

