# <center>UniSinger: Unified End-to-End Singing Voice Synthesis With Cross-Modality Information Matching</center>

**Introduction:**<br> 
In this work, we propose UniSinger, a unified end-to-end singing voice synthesizer, which integrates three abilities related to singing voice generation: singing voice synthesis (SVS), singing voice conversion (SVC), and singing voice editing (SVE) into a single framework. 

All experiments in the paper are conducted on a large-scale singing voice dataset OpenSinger. There are some audio samples to demonstrate the performance of SVS, SVC and SVE applications.

## 1 Singing Voice Synthesis

<div>
    <table style='width: 100%;'>
        <thead>
        <tr>
            <th>index</th>
            <th>GT</th>
            <th>GT (mel + HiFiGAN)</th>
            <th>FastSpeech 2 + HiFiGAN</th>
            <th>FastSpeech 2s</th>
            <th>VISinger</th>
            <th>UniSinger</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <th>#1</th>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
        <tr>
            <th>#2</th>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
        <tr>
            <th>#3</th>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
        <tr>
            <th>#4</th>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
        <tr>
            <th>#5</th>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    </table>
</div>

## 2 Singing Voice Conversion
<div>
    <table style='width: 100%;'>
        <thead>
        <tr>
            <th>index</th>
            <th>Source</th>
            <th>Reference</th>
            <th>Reference (mel + HiFiGAN)</th>
            <th>SpeechFlow (Pitch)</th>
            <th>SpeechFlow (Timbre)</th>
            <th>SpeechFlow (Pitch + Timbre)</th>
            <th>UniSinger (Pitch)</th>
            <th>UniSinger (Timbre)</th>
            <th>UniSinger (Pitch + Timbre)</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <th>#1</th>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
        <tr>
            <th>#2</th>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
        <tr>
            <th>#3</th>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
        <tr>
            <th>#4</th>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
        <tr>
            <th>#5</th>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    </table>
</div>

## 3 Singing Voice Editing
#### Exp. 1:
original lyrics: 爱可以不问对错 —— <BOS> ai # k e | y i # b u | w en # d ui | c uo <EOS> <br>
insertion: 爱<font color="red">怎么</font>可以不问对错 —— <BOS> ai # <font color="red">z en | m e #</font> k e | y i # b u | w en # d ui | c uo <EOS> <br>
replacement: 爱<font color="red">怎么(<strike>可以</strike>)</font>不问对错 —— <BOS> ai #<font color="red"> z en | m e # (<strike>k e | y i #</strike>) </font>  b u | w en # d ui | c uo <EOS> <br>
deletion: 爱<font color="red">(<strike>可以</strike>)</font>不问对错 —— <BOS> ai # <font color="red">(<strike> k e | y i #</strike>)</font> b u | w en # d ui | c uo <EOS> <br>
<div>
    <table style='width: 100%;'>
        <thead>
        <tr>
            <th>GT</th>
            <th>GT(Mel+PWG)</th>
            <th>EditSinger(insertion)</th>
            <th>EditSinger(replacement)</th>
            <th>EditSinger(deletion)</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000002.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000002.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000002.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000002.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000002.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    </table>
</div>

#### Exp. 2:
original lyrics: 你何苦非为他等在雨中 —— <BOS> n i # h e | k u # f ei | w ei # t a # d eng # z ai # y u # zh ong <EOS> <br>
insertion: 你何苦非为他<font color="red">傻傻</font>等在雨中 —— <BOS> n i # h e | k u # f ei | w ei # t a # <font color="red">sh a | sh a #</font> d eng # z ai # y u # zh ong <EOS> <br>
replacement: 你何苦非为他<font color="red">伫立风(<strike>等在雨</strike>)</font>中 —— <BOS> n i # h e | k u # f ei | w ei # t a # <font color="red">zh u | l i # f eng | (<strike> d eng # z ai # y u #</strike>)</font> zh ong <EOS> <br>
deletion: 你<font color="red">(<strike>何苦非</strike>)</font>为他等在雨中 —— <BOS> n i # <font color="red">(<strike> h e | k u # f ei |</strike>)</font> w ei # t a # d eng # z ai # y u # zh ong <EOS> <br>
<div>
    <table style='width: 100%;'>
        <thead>
        <tr>
            <th>GT</th>
            <th>GT(Mel+PWG)</th>
            <th>EditSinger(insertion)</th>
            <th>EditSinger(replacement)</th>
            <th>EditSinger(deletion)</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000003.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000003.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000003.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000003.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000003.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    </table>
</div>

#### Exp. 3:
original lyrics: 几朵云在阴天忘了该往哪儿走 —— <BOS> j i | d uo # y un # z ai # y in | t ian # w ang # l e # g ai # w ang # n a | r # z ou <EOS> <br>
insertion: 几朵<font color="red">孤独的</font>云在阴天忘了该往哪儿走 —— <BOS> j i | d uo # <font color="red">g u | d u # d e #</font> y un # z ai # y in | t ian # w ang # l e # g ai # w ang # n a | r # z ou <EOS> <br>
replacement: 几<font color="red">片叶(<strike>朵云</strike>)</font>在阴天忘了该往哪儿走 —— <BOS> j i | <font color="red">p ian # y e | (<strike>d uo # y un #</strike>)</font> z ai # y in | t ian # w ang # l e # g ai # w ang # n a | r # z ou <EOS> <br>
deletion: 几朵云<font color="red">(<strike>在阴天</strike>)</font>忘了该往哪儿走 —— <BOS> j i | d uo # y un | <font color="red">(<strike>z ai # y in | t ian #</strike>)</font> w ang # l e # g ai # w ang # n a | r # z ou <EOS> <br>
<div>
    <table style='width: 100%;'>
        <thead>
        <tr>
            <th>GT</th>
            <th>GT(Mel+PWG)</th>
            <th>EditSinger(insertion)</th>
            <th>EditSinger(replacement)</th>
            <th>EditSinger(deletion)</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000011.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000011.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000011.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000011.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000011.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    </table>
</div>

#### Exp. 4:
original lyrics: 被吹进了左耳 —— <BOS> b ei # ch ui | j in # l e # z uo | er <EOS> <br>
insertion: 被<font color="red">思念</font>吹进了左耳 —— <BOS> b ei # <font color="red">s i | n ian #</font> ch ui | j in # l e # z uo | er <EOS> <br>
replacement: 被<font color="red">传递到(<strike>吹进了</strike>)</font>左耳 —— <BOS> b ei # <font color="red">ch uan | d i # d ao # (<strike>ch ui | j in # l e # </strike>)</font> z uo | er <EOS> <br>
deletion: 被吹进<font color="red">(<strike>了</strike>)</font>左耳 —— <BOS> b ei # ch ui | j in # <font color="red">(<strike>l e #</strike>)</font> z uo | er <EOS> <br>
<div>
    <table style='width: 100%;'>
        <thead>
        <tr>
            <th>GT</th>
            <th>GT(Mel+PWG)</th>
            <th>EditSinger(insertion)</th>
            <th>EditSinger(replacement)</th>
            <th>EditSinger(deletion)</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000012.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000012.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000012.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000012.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000012.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    </table>
</div>

#### Exp. 5:
original lyrics: 在昏暗中的我 —— <BOS> z ai # h un | an # zh ong # d e # w o <EOS> <br>
insertion: 在<font color="red">那时</font>昏暗中的我 —— <BOS> z ai # <font color="red">n a | sh i #</font> h un | an # zh ong # d e # w o <EOS> <br>
replacement: 在昏暗中<font color="red">与你(<strike>的我</strike>)</font> —— <BOS> z ai # h un | an # zh ong # <font color="red">y u # n i (<strike>d e # w o</strike>)</font> <EOS> <br>
deletion: 在昏暗<font color="red">(<strike>中</strike>)</font>的我 —— <BOS> z ai # h un | an # <font color="red">(<strike> zh ong # </strike>)</font> d e # w o <EOS> <br>
<div>
    <table style='width: 100%;'>
        <thead>
        <tr>
            <th>GT</th>
            <th>GT(Mel+PWG)</th>
            <th>EditSinger(insertion)</th>
            <th>EditSinger(replacement)</th>
            <th>EditSinger(deletion)</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000013.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000013.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000013.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000013.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000013.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    </table>
</div>

