# utl-setting-your-classic-editor-dms-function-keys-mouse-actions-and-command-line
Setting your classic editor dms function keys mouse actions and command line shortcuts
    %let pgm=utl-setting-your-classic-editor-dms-function-keys-mouse-actions-and-command-line;

    Setting your classic editor dms function keys mouse actions and command line shortcuts

    github this repo
    https://tinyurl.com/yvc3mwpw
    https://github.com/rogerjdeangelis/utl-setting-your-classic-editor-dms-function-keys-mouse-actions-and-command-line

    github
    https://tinyurl.com/a75mrwxz
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories/blob/master/sas_saspac.sas

    Note you do not need to use the mouse or function keys, you can just use short command line shortcuts.

    The include below will install the sas performance package which enables command line shortcuts, function keys and mouse actions.
    %inc "c:/oto/sas_saspac.sas"; /*--- include saspac, i have this in my autoexec ---*/

    Some function keys can only be set by editing within the keys window

    For more information the youtube five part "point and shoot programming" may help.
    https://www.youtube.com/channel/UCUzsiGhcv3OFovLJTazTc2w

    F12 is the magic string

    F12      ~;;;;%end;%mend;/*'*/ *);*};*];*/;/*"*/;run;quit;%end;end;run;endcomp;%utlfix;
    SHF F7   log;file "c;\log\&pgm..log`;note z;notesubmit `%utl_logcurchk;`;"

     STEPS for Command line shortcuts, function keys and mapping mouse buttons.

      1. backup your keys
         Type "keys" on classic editor command line (not the command bar. May work in EE but you lose a lot of functionality.
         I create a copy of my sasuser.profile about every couple of weeks, this will also backup yo key settings.

         Type "save keyssave r";end; /*---- respond yes if asked to make change permanent ----*/
      2. Whenever you open keys that have changed make sure you close by entering "save r;end;" /*---- respond yes if asked ----*/
         In you have a single quote in the function key text, sas will freeze up and you have to close sas
         Try to avoild %macro? Macro variables will not be resolved, you want this.

      3. Clear keys
         dm 'keydef "F1" "~"';
         dm 'keydef "F2" "~"';
         dm 'keydef "F3" "~"';
         dm 'keydef "F4" "~"';
         dm 'keydef "F5" "~"';
         dm 'keydef "F6" "~"';
         dm 'keydef "F7" "~"';
         dm 'keydef "F8" "~"';
         dm 'keydef "F9" "~"';
         dm 'keydef "F11"     "~"';
         dm 'keydef "F12"     "~"';
         dm 'keydef "SHF F1"  "~"';
         dm 'keydef "SHF F2"  "~"';
         dm 'keydef "SHF F6"  "~"';
         dm 'keydef "SHF F7"  "~"';
         dm 'keydef "SHF F8"  "~"';
         dm 'keydef "SHF F9"  "~"';
         dm 'keydef "SHF F10" "~"';
         dm 'keydef "SHF F11" "~"';
         dm 'keydef "SHF F12" "~"';
         dm 'keydef "CTL F1"  "~"';
         dm 'keydef "CTL F2"  "~"';
         dm 'keydef "CTL F3"  "~"';
         dm 'keydef "CTL F11" "~"';
         dm 'keydef "CTL F12" "~"';
         dm 'keydef "ALT F1"  "~"';
         dm 'keydef "ALT F2"  "~"';
         dm 'keydef "ALT F3"  "~"';
         dm 'keydef "ALT F11" "~"';
         dm 'keydef "ALT F12" "~"';
         dm 'keydef "CTL B"   "~"';
         dm 'keydef "CTL D"   "~"';
         dm 'keydef "CTL E"   "~"';
         dm 'keydef "CTL G"   "~"';
         dm 'keydef "CTL H"   "~"';
         dm 'keydef "CTL I"   "~"';
         dm 'keydef "CTL J"   "~"';
         dm 'keydef "CTL K"   "~"';
         dm 'keydef "CTL L"   "~"';
         dm 'keydef "CTL M"   "~"';
         dm 'keydef "CTL Q"   "~"';
         dm 'keydef "CTL R"   "~"';
         dm 'keydef "CTL T"   "~"';
         dm 'keydef "CTL U"   "~"';
         dm 'keydef "CTL W"   "~"';
         dm 'keydef "CTL Y"   "~"';
         dm 'keydef "RMB"     "~"';
         dm 'keydef "SHF RMB" "~"';
         dm 'keydef "CTL RMB" "~"';
         dm 'keydef "MMB"     "~"';
         dm 'keydef "SHF MMB" "~"';
         dm 'keydef "CTL MMB" "~"';
         run;quit;
     3. Set keys

    You have to set these keys manually by editing inside the keys window;

    F12      ~;;;;%end;%mend;/*'*/ *);*};*];*/;/*"*/;run;quit;%end;end;run;endcomp;%utlfix;
    SHF F7   log;file "c;\log\&pgm..log`;note z;notesubmit `%utl_logcurchk;`;"

    You need to edit keys directly to change backtics to the correct quote type.
    Be careful with macro triggers.

    dm 'keydef "F1" "home;_sv;"';
    dm 'keydef "F2" "home;copy cmt;"';
    dm 'keydef "F3" "~run;quit;"';
    dm 'keydef "F4" "notesubmit;"';
    dm 'keydef "F5" "conh"';
    dm 'keydef "F6" "dmph"';
    dm 'keydef "F7" "con"';
    dm 'keydef "F8" "rfind"';
    dm 'keydef "F9" "rchange"';
    dm 'keydef "F11" "sumv"';
    dm 'keydef "F12" "~set magic key by editiong keys"';
    dm 'keydef "SHF F1" "lsa"';
    dm 'keydef "SHF F2" "unvh"';
    dm 'keydef "SHF F6" "~proc datasets lib=sd1 nolist nodetails;delete want; run;quit;"';
    dm 'keydef "SHF F7" "~set magic key by editiong keys"';
    dm 'keydef "SHF F8" "lsah"';
    dm 'keydef "SHF F9" "avgh"';
    dm 'keydef "SHF F10" "debugh"';
    dm 'keydef "SHF F11" "lsfh"';
    dm 'keydef "SHF F12" "parh"';
    dm 'keydef "CTL F1" "lsah"';
    dm 'keydef "CTL F2" "cuth"';
    dm 'keydef "CTL F3" "sqldesh"';
    dm 'keydef "CTL F11" "evlh"';
    dm 'keydef "CTL F12" "tail"';
    dm 'keydef "ALT F1" "rpth"';
    dm 'keydef "ALT F2" "xlrh"';
    dm 'keydef "ALT F3" "sasbatch"';
    dm 'keydef "ALT F11" "unvh"';
    dm 'keydef "ALT F12" "tailh"';
    dm 'keydef "CTL B" "wattention"';
    dm 'keydef "CTL D" "~proc tabulate;var a b;table a(n)*f=5.*b(n)*f=5.;run;"';
    dm 'keydef "CTL E" "~n ? `hil`;n=*`P Jone`;n gt;`Phil`;n le `Eva`;sql- eqt gtt ltt get let net"';
    dm 'keydef "CTL G" "note g.g;home;resize;"';
    dm 'keydef "CTL H" "note h.h;home;resize"';
    dm 'keydef "CTL I" "note i.i;home;resize"';
    dm 'keydef "CTL J" "~/*----                                                                   ----*/"';
    dm 'keydef "CTL K" ":mcu"';
    dm 'keydef "CTL L" ":mcl"';
    dm 'keydef "CTL M" "~proc format;value $a;proc catalog cat=formats;modify a.formatc(desc=`OK`);run;"';
    dm 'keydef "CTL Q" "~options minoperator;macro t(x=a)/minoperator;%if &x in (a b c) %then;%mend;"';
    dm 'keydef "CTL R" "~proc report data=sashelp.class named list wrap;run;quit;"';
    dm 'keydef "CTL T" "~proc tabulate data=class;class sex age;table age,sex*(n pctn<age>)/rts=8"';
    dm 'keydef "CTL U" "xpad"';
    dm 'keydef "CTL W" "~x `tree `c;/temp` /F /A | clip`"';
    dm 'keydef "CTL Y" "~where name like `B_B` `%B%` `B%B`"';
    dm 'keydef "RMB" "log;clear;out;clear;pgm;submit;home;log;z;z;"';
    dm 'keydef "SHF RMB" "ls4"';
    dm 'keydef "CTL RMB" "lsh"';
    dm 'keydef "MMB" "~assigned to f1;"';
    dm 'keydef "SHF MMB" "~assigned to shf f1 lsa all obs last datasets"';
    dm 'keydef "CTL MMB" "~assigned to cnt fl ldah all obs highlighed dataset"';
    run;quit;

    4. To revert to your saved keys. Open the keys window and type
       Type "copy keyssave"


    5.  If you are using the logitech G-502 Hero mouse, do the following mappings.
        Print the following, mount on carboard and stick in the slot above the keys in the del wired keyboard.
        You can mutiply mouse actions by holding down shf/alt/ctrl keys before hitting the mouse buttons.


                    _______________________________
                    /                               \              _____________
                   /             TOP VIEW            \            /             \
                  /   Can use with SHF CTL & ALT      \          /               \
                 /                                     \        /  SIDE VIEW      \
                |                                       |      /                   \
                |                            ___        |     |                     |
                |                           /   \       |     |    ___              |
                |                          | RMB |      |     |   /   \             |
                |                           \___/       |     |  | F11 |            |
                |                   SAS direct mapping  |     |   \___/             -\
                |                                       |     |        Scroll Wheel - |
                |                                       |     |           ___       - /
                |                                       |     |          /   \      |/
                |                                       |     |         | F5  |     |
                |    ___                                |     |          \___/      |
                |   /   \                               |     |                     |
                |  | F11 |                              |     |    ___              |
                |   \___/                               |     |   /   \             |
                |                                       |     |  | F4  |            |
                |           ___       ___      ___      |     |   \___/             |
                |          /   \     /   \    /   \     |     |                     |
                |         | F5  |   | F1  |  | F6  |    |      \                    /
                |          \___/     \___/    \___/     |       \                  /
                |                                       |        \                /
                |    ___                                |         \              /
                |   /   \                               |          \____________/
                |  | F4  |                              |
                |   \___/                               |
                |                     ___               |
                |                    /   \              |
                |                   | F2  |             |
                |                    \___/              |
                 \                                      /
                  \                                    /
                   \                                  /
                    \                                /
                     \______________________________/




    F1(MMB)     RMB         F2          F3             F4           F5      F6         F7          F8         F9          F10         F1

    version     submit      comment     run;quit       notesubmit   conh    dmph       con         rfind      rchange    lsfh        sum
    shf lsa     shf ls40    shf unvh                                        shf dmp    shf logchk  shf lsah   shf avgh   shf debugh  shf
    ctl lsah    ctl lsh     ctl cuth    ctl sqldesh                                                                                  ctl
    alt rpth                alt xlrh    alt sasbatch                                                                                 alt

    /*        _       _           _
     _ __ ___| | __ _| |_ ___  __| |  _ __ ___ _ __   ___  ___
    | `__/ _ \ |/ _` | __/ _ \/ _` | | `__/ _ \ `_ \ / _ \/ __|
    | | |  __/ | (_| | ||  __/ (_| | | | |  __/ |_) | (_) \__ \
    |_|  \___|_|\__,_|\__\___|\__,_| |_|  \___| .__/ \___/|___/
                                              |_|
    */


    https://github.com/rogerjdeangelis/Creating-command-macros-for-the_1980s-DMS-Classic-Editor
    https://github.com/rogerjdeangelis/utl-are-git classicclassic-editor-command-macros-fsview-and-fsedit-more-useful-than-viewtable
    https://github.com/rogerjdeangelis/utl-classic-editor-comment-out-a-block-of-text
    https://github.com/rogerjdeangelis/utl-classic-editor-commnand-macro-to-repair-sas-satement-with-uunbalanced-quotes
    https://github.com/rogerjdeangelis/utl-comment-out-a-block-og-code-in-the-classic-1980s-dms-editor
    https://github.com/rogerjdeangelis/utl-how-to-set-up-the-classic-1980s-classic-editor
    https://github.com/rogerjdeangelis/utl-latest-command-macros-for-the-sas-classic-editor
    https://github.com/rogerjdeangelis/utl-location-of-program-folder-and-classic-editor-program-versioning
    https://github.com/rogerjdeangelis/utl-repairing-the-calssic-l980s-display-manager-editor
    https://github.com/rogerjdeangelis/utl-sas-classic-editor-function-keys-for-comments
    https://github.com/rogerjdeangelis/utl-sas-scripting-commands-only-available-in-the_1980s-classic-editor
    https://github.com/rogerjdeangelis/utl-setting-the-path-of-the-executing-program-in-the-1980s-sas-editor
    https://github.com/rogerjdeangelis/utl-spell-check-words-in-any-classic-editor-window-ie-pgm-note-log-output
    https://github.com/rogerjdeangelis/utl-trimming-padded-lines-in-the-classic-editor
    https://github.com/rogerjdeangelis/utl_classic_editor_command_macro_performance_package
    https://github.com/rogerjdeangelis/utl_classic_editor_hilite_and_evaluate_math_functions
    https://github.com/rogerjdeangelis/utl_classic_editor_keyboard_macros_and_abbreviations
    https://github.com/rogerjdeangelis/utl_classic_editor_part_II
    https://github.com/rogerjdeangelis/utl_classic_editor_pfkeys_prefix_mouse
    https://github.com/rogerjdeangelis/utl_classic_editor_place_comment_box_at_cursor_location_with_single_keystroke
    https://github.com/rogerjdeangelis/utl_classic_editor_programatic_cursor_positioning_with_store_cut_and_paste
    https://github.com/rogerjdeangelis/utl_classic_editor_seemless_connection_workstation_unix_server
    https://github.com/rogerjdeangelis/utl_classic_editor_using_a_prefix_mask_to_facilitate_fixed_column_data_entry
    https://github.com/rogerjdeangelis/utl_classic_sas_editor_display_manager_commands_improved
    https://github.com/rogerjdeangelis/utl_performance_package_SAS_classic_editor
    https://github.com/rogerjdeangelis/utl_sas-classic-editor-point-and-shoot-a-proc-freq
    https://github.com/rogerjdeangelis/utl_sas_classic_editor

    /*                                             _   _ _
      ___ ___  _ __ ___  _ __ ___   __ _ _ __   __| | | (_)_ __   ___    _ __ ___   __ _  ___ _ __ ___  ___
     / __/ _ \| `_ ` _ \| `_ ` _ \ / _` | `_ \ / _` | | | | `_ \ / _ \  | `_ ` _ \ / _` |/ __| `__/ _ \/ __|
    | (_| (_) | | | | | | | | | | | (_| | | | | (_| | | | | | | |  __/  | | | | | | (_| | (__| | | (_) \__ \
     \___\___/|_| |_| |_|_| |_| |_|\__,_|_| |_|\__,_| |_|_|_| |_|\___|  |_| |_| |_|\__,_|\___|_|  \___/|___/

    */

     cm         Hilite the blank line and subsequent block of code and the code will be commented out
     xpad       on command line Remove DMS line padding and copy program to clipbrd
     mish       sex age Highlight dataset and type mish sex age and for crosstab of missings" ;
     unqh       sex age  distinct counts Usubjid must be in the datasets
     _sv        pf1 or mmb Save timestamped version of the program in the c:/ver folder and save program in c:/utl
     sqldesh    Hilite table and type alt and scroll button
     sasbatch   Highlight code type sasbatch on command line
     evlh       Hilite expression 2*
     sumv       Hilite a column of numbers and an proc means will run
     xlrh       Hilite a table and type xlr and table will open it in excel No need for pc acces to excel
     sumr       Hilite row of numbers type sumr and the sum will appear in the log and macro variable __sumr
     iota       A verical list sequential numbers"
     cuth       Hilite a block of code and type cuth and mutiple spaces will be reduced to single spaces
     parh       Hilite a line of code and type parh to test for unbalanced parens
     xit        When exiting sas type xit and last program will open next time you start SAS
     cntuh      Hilite table and count distinct usubjid and number of obs are in paste buffer
     cliph      Hilite a line of  and macro variable _clip will contain the statement
     cnth       sex age Hilite table and type cnth age sex and distinct counts of age sex cobinations in paste buffer
     avgby      sex age Hilite table type avgby sex age for means by sex age also output dataset avgby
     tail       Type tail and last 40 obs of last dataset in paste buffer and output window
     tailh      Hilite table and type tailh and the last 40 obs will be in output window and in paste buffer
     ls4        Type ls and a list of first 40 obs of last table in output window and paste buffer
     lsh        Type lsh for list and output in paste buffer of hilited table
     lsfh       Hilight table type lsfh for 40 obs formatted list and output in paste buffer
     lsa        Ttpe lsal to list all obs from the last dataset
     lsah       Type lsah for a list of all obs in output and in paste buffer of hilited table
     doendh     Hilite block of macro code and match dos and ends
     lsw        [dq]]age=14[dq] Use single and doubple quotes for chars, 40 obs  filter for  the _last_ table in pastebuffer and list
     avgh       Hilite table and type avgh for proc means output and table avgh will be created
     frqv       Hilite variable in _last_ table andn proc freq hiltred variable
     cntv       Hilight variable in _last_ table and get count and distinct counts on variable
     unvv       Hilite a variable from the _last_ table and proc unvariate will be run on that variable
     unvh       proc univariate on hilighted dataset
     rpth       Generate proc report code on hilighted dataset
     dmp        Type dmp and middle observation of last dataset printed vertically
     dmph       Type dmph middle observation of highlighted dataset printed vertically with type length and sample value
     frq        sex age Type frq type sex for a crosstab frequency on sex*age for last datasetakes frq dataset
     frqh       sex age Highlight dataset and type frqh sex age and  forfrequency on sex xage Also frqh dataset
     prtwh      hilite and type prtwh "sex=s ingle quote F single quote " subset listing
     debugh     Highlight macro and type debugh to debug the macro
     con        Type con and contents of last dataset in outptut
     conh       Highlight table and type conh on command line Results in output window
     vu         Type vu for viewtable of last dataset created
     vuh        Type vuh for viewtable of highlighted dataset
     xlsh       Highlight table and type xlsh and the table  will appear in excel uses libname need pc acces;
     keylist    Type keylist and a list og your function keys will be in the log
     xpy        Type xpy roger for program banner with large font https://githubcom/rogerjdeangelis/utl_program_banners


    /*              _
      ___ _ __   __| |
     / _ \ `_ \ / _` |
    |  __/ | | | (_| |
     \___|_| |_|\__,_|

    */
