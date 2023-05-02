Download Link: https://assignmentchef.com/product/solved-cpe212-project03
<br>



Project03 Goals

A          fundamental  software         engineering    skill     is         the      design,            implementation,        and      testing of         a software         component     that     must   be        integrated      into     a          larger  software         product.                      The     software component     must   conform          to         a          previously      agreed upon   interface         format.            As        part     of         this assignment,    you      will      practice          this      skill     by        completing     the      implementation         of         <strong>two     stack  classes </strong>(<strong>MiniStack    </strong>and<strong>      </strong><strong>BigStack</strong>)       that     will      be        integrated      into     a          larger  software         product          provided        by the      instructor.                  Along  the      way     you      will      review basic   C++     programming and      Linux  file       management skills   required         for       successful       completion     of         CPE     212.

<h1>Project03 Overview</h1>

For      this      project,           you      will      <strong><em>complete</em></strong>        the      provided        partial C++     program         that     utilizes            classes to implement     a          stack.              The     <strong>MiniStack</strong>      class    is         an        array-based   implementation         of         the      Stack Abstract          Data    Type   (ADT) where the      array   size     is         limited            to         five      elements        of         type    <strong>char</strong>.<strong>   MiniStack      </strong>objects            are      used    by<strong>        BigStack</strong>        to         create a          doubly-linked-node, stack-of-<strong>MiniStacks</strong> implementation         of         the      Stack   ADT.                            So        with    this      project,           you      practice          implementing both an        array-based   stack   (<strong>MiniStack</strong>)   and      a          linked-node   stack   (<strong>BigStack</strong>).

The      <strong>Project03_Materials.zip</strong>     file       includes          four     source code    files     and      a          <strong>makefile</strong>.

<table width="735">

 <tbody>

  <tr>

   <td width="110"><strong>Filename                  </strong></td>

   <td width="191"><strong>Project03_Materials.zip                  </strong></td>

   <td width="433"><strong>Description         </strong></td>

  </tr>

  <tr>

   <td width="110"><strong>main.cpp                  </strong></td>

   <td width="191">Included</td>

   <td width="433">Driver    program                  to              test          <strong>MiniStack</strong>             and                  <strong>BigStack                </strong>classes</td>

  </tr>

  <tr>

   <td width="110"><strong>ministack.h                  </strong></td>

   <td width="191">Included<strong>                 </strong></td>

   <td width="433">Specification         file            for            <strong>MiniStack</strong>             class</td>

  </tr>

  <tr>

   <td width="110"><strong>ministack.cpp                  </strong></td>

   <td width="191"><strong>Write     and          submit  this                  file</strong></td>

   <td width="433">Implementation  file            for            <strong>MiniStack</strong>             class</td>

  </tr>

  <tr>

   <td width="110"><strong>bigstack.h                  </strong></td>

   <td width="191">Included</td>

   <td width="433">Specification         file            for            <strong>BigStack</strong>                class</td>

  </tr>

  <tr>

   <td width="110"><strong>bigstack.cpp                  </strong></td>

   <td width="191"><strong>Write     and          submit  this                  file</strong></td>

   <td width="433">Implementation  file            for            <strong>BigStack</strong>                class</td>

  </tr>

  <tr>

   <td width="110"><strong>p03input1.txt                  </strong></td>

   <td width="191">Included</td>

   <td width="433">Tests       class        <strong>MiniStack</strong>             member                  functions</td>

  </tr>

  <tr>

   <td width="110"><strong>p03input2.txt</strong><strong>                  </strong></td>

   <td width="191">Included</td>

   <td width="433">Tests       class        <strong>BigStack</strong>                member                  functions                  (assuming              <strong>MiniStack</strong>             works)</td>

  </tr>

  <tr>

   <td width="110"><strong>p03input3.txt</strong><strong>                  </strong></td>

   <td width="191">Included</td>

   <td width="433">Tests       class        <strong>BigStack</strong>                member                  functions                  (assuming              <strong>MiniStack</strong>             works)</td>

  </tr>

 </tbody>

</table>

<strong>MiniStack      </strong>operates         as        a          regular            array-based   stack   object, and      one      may     develop          and      test      it in         isolation         from    <strong>BigStack</strong>        provided        that     the      <strong>BigStack</strong>        function          stubs   are      in         place.              As data     values are      pushed           onto    <strong>BigStack,</strong>       it          must   create a          new     node   that     will      use      a          <strong>MiniStack</strong> object  to         store   the      incoming        data.                Once   that     <strong>MiniStack</strong>      object  is         filled   to         capacity,         <strong>BigStack</strong> will      have    to         create a          new     node   to         store   any      additional       values pushed           onto    <strong>BigStack.                   </strong>

In         the      figure  below, the      character        ‘<strong>a</strong>’        was     the      first     character        added to         the      <strong>BigStack</strong>        object  (it is         now     at         the      bottom            of         the      <strong>BigStack</strong>),      and      the      character        ‘<strong>k</strong>’        was     the      last      character added (it        is         now     at         the      top      of         the      <strong>BigStack</strong>).                  So,       four     more   characters      could   be pushed           onto    this      <strong>BigStack</strong>        object  before another           node/MiniStack         object  is         needed.                       Note    that <strong>BigStack</strong>        nodes  have    both    <strong>nextPtr</strong>          and      <strong>previousPtr</strong>  links.

<strong> </strong>

<h1>Getting Started</h1>

<ul>

 <li>Create empty function stubs   for       <strong>MiniStack</strong>      and      <strong>BigStack</strong>        member</li>

 <li>Use <strong>make</strong>  to         compile          your</li>

 <li>Once the      framework     compiles         and      executes,        implement     the      member          functions        of         <strong>MiniStack</strong></li>

 <li>Use <strong>txt</strong>           to         verify  correct            operation       of         just      <strong>MiniStack</strong>.</li>

 <li>Now implement     the      member          functions        of         <strong>BigStack</strong>.</li>

</ul>

Note    that     as        a          client  of         <strong>MiniStack,     </strong>the      class    <strong>BigStack</strong>        will      have    to         utilize (call/invoke)  the            public member          functions        of         <strong>MiniStack</strong>      to         store   and      manipulate     data     in         the      array            linked to         each    <strong>MiniStack      </strong>object.             So,       be        sure    <strong>MiniStack      </strong>is         fully    functional       first.

<ul>

 <li>Use <strong>txt</strong>           and      <strong>p03input3.txt</strong>           to         verify  correct            operation</li>

</ul>

<h1>Hints</h1>

—   The     code    for       an        array   implementation         of         the      stack   ADT    is         in         your    notes!!!                             You     will      need    to         modify            the      code    for       the      linked-list       implementation         to         include           both      <strong>nextPtr</strong>          and      <strong>previousPtr</strong>  links.

—   Implement     <strong>MiniStack</strong>      first     and      test      it          thoroughly     before attempting     <strong>BigStack</strong>

—   If         <strong>MiniStack</strong>      does    not      work,  <strong>BigStack</strong>        will      not      work

—   The     outputs           of         <strong>MiniStack      </strong>are      grouped          within<strong> (          )          </strong>to         help     you      visualize         where the      pushed           characters      have    been    stored.            The     output of         <strong>BigStack</strong>        is         bracketed       by                    <strong>[                           ]                </strong>                  and      may     consist            of         zero    or        more   <strong>MiniStack      </strong>(          )          groupings.

<h1>Step #1 – Unzipping Project Materials on blackhawk</h1>

Use      the      Firefox            browser          to         access Canvas            and      download       the      <strong>Project03_Materials.zip</strong>     file       into your    <strong>Project03</strong>      directory.                   At        terminal         window          prompt,          use      the      unzip  utility  to uncompress   the      files.                For      example,         to         unzip  the      files     into     your    current           directory:

<strong>unzip  Project03_Materials.zip </strong>

Since   this      project            is         worth  three   points, you      have    been    given   three   input   files     to         test      your    program.

<h1>Step #2 – Create Function Stubs for the Missing Support Functions</h1>

Open   a          Linux  terminal         window          and      navigate         to         the      directory        containing      the      <strong>Project03</strong> materials        downloaded   from    Canvas            (you    should be        there   already           if          you      just      completed      Step    #1 above).

Use      the      following        command       to         create the      missing           files     by        typing the      following        at         the Linux  prompt.                      Linux  is         case     sensitive         so        pay      attention        to         upper  versus lower  case     letters. <strong>gedit                           ministack.cpp                      bigstack.cpp             &amp;         </strong>

This     command       starts  the      <strong>gedit</strong>   text     editor  running          as        a          background    process           (          <strong>&amp;</strong>         ).          With    the      editor  running          in         the      background,   you      may     use      the      same   terminal         window          to compile          and      test      your    program.

—          Add     stubs   for       <strong>MiniStack</strong>      and      <strong>BigStack</strong>        functions        to         <strong>ministack.cpp          </strong>and      <strong>bigstack.cpp </strong>and      save the      files.

In         the      terminal         window,         compile          your    program         by        typing the      word   <strong>make</strong>  at         the      prompt and      press   the      Enter   key.                 If         you      see      error   messages,       use      the      text     editor  to         make   corrections to         the      function          stubs   and      switch back    to         the      terminal         window          to         type    <strong>make</strong>  again   to recompile       your    program.                    Once   your    program         compiles,        you      may     execute           it          by        typing:                                                             <strong>./project03   inputfilename       </strong>

Now    that     your    program         compiles         and      executes         using   function          stubs,  you      may     implement     and      test your    solution          function          by        function.                     Start    with    the      functions        associated      with    opening          files and      loading           data.

<strong>Running the Sample Solution on blackhawk [shows the desired output for specified input file] </strong><strong><em>The    best     description    of what   your    code    should            do        is         the      Sample           Solution         for       the      project.</em></strong>

Run     the      sample            solution          by        typing the      following        at         <strong>blackhawk</strong>    terminal         window          command prompt           where <strong>inputfilename</strong>     is         the      name   of         one      of         the      provided        input   files     (for     example, p03input1.txt).

<strong>/home/work/cpe212/project03/p03   inputfilename </strong>

Your    current           working          directory        must   contain           the      input   files     for       this      to         work.

<h1>Running the Preview Script on blackhawk [analyzes outputs for all provided input files]</h1>

Run     the      preview          script  by        typing the      following        in         a          <strong>blackhawk</strong>    terminal         window          command prompt

<strong>/home/work/cpe212data/project03/preview03.bash         </strong>

This     script  will      run      both    the      <strong>Sample           Solution</strong>         AND    your    <strong>project03</strong>      executable      program         on        the complete        set       of         input   files,    and      it          compares       the      outputs           of         the      two     programs       line      by line      to         identify           errors in         your    program’s      outputs.                      Make   sure    that     the      output of         your program         exactly            matches          the      output of         the      Sample           Solution.

<ul>

 <li><strong><em>To use      the      preview          script, your    executable     must   be        on       blackhawk</em></strong><strong><em>    </em></strong></li>

 <li><strong><em>The sample           input  files     must   be        in        your    current          working         directory       BEFORE          you execute          the      preview          script!!!</em></strong></li>

</ul>