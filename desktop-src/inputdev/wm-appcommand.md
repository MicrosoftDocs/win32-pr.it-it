---
title: Messaggio WM_APPCOMMAND (winuser. h)
description: Notifica a una finestra che l'utente ha generato un evento del comando dell'applicazione, ad esempio facendo clic su un pulsante di comando dell'applicazione utilizzando il mouse o digitando un tasto di comando dell'applicazione sulla tastiera.
ms.assetid: ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c
keywords:
- Input della tastiera e del mouse WM_APPCOMMAND messaggio
topic_type:
- apiref
api_name:
- WM_APPCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7f5e71f9a443e12ea56cb8ca23daea148da92aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400510"
---
# <a name="wm_appcommand-message"></a>\_Messaggio APPCOMMAND WM

Notifica a una finestra che l'utente ha generato un evento del comando dell'applicazione, ad esempio facendo clic su un pulsante di comando dell'applicazione utilizzando il mouse o digitando un tasto di comando dell'applicazione sulla tastiera.


```C++
#define WM_APPCOMMAND                   0x0319
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra in cui l'utente ha fatto clic sul pulsante o ha premuto il tasto. Può trattarsi di una finestra figlio della finestra che riceve il messaggio. Per ulteriori informazioni sull'elaborazione di questo messaggio, vedere la sezione Osservazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Usare il codice seguente per ottenere le informazioni contenute nel parametro *lParam* .


```
cmd  = GET_APPCOMMAND_LPARAM(lParam);

uDevice = GET_DEVICE_LPARAM(lParam);

dwKeys = GET_KEYSTATE_LPARAM(lParam);
```



Il comando dell'applicazione è *cmd*, che può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPCOMMAND_BASS_BOOST"></span><span id="appcommand_bass_boost"></span><dl> <dt>**APPCOMMAND \_ BASS \_ Boost**</dt> <dt>20</dt> </dl>                                                                         | Attivare e disattivare il boost bass.<br/>                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BASS_DOWN"></span><span id="appcommand_bass_down"></span><dl> <dt>**APPCOMMAND \_ BASSO \_**</dt> <dt>19</dt> </dl>                                                                            | Ridurre i bassi.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BASS_UP"></span><span id="appcommand_bass_up"></span><dl> <dt>**APPCOMMAND \_ BASS \_ up**</dt> <dt>21</dt> </dl>                                                                                  | Aumentare il basso.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_BACKWARD"></span><span id="appcommand_browser_backward"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ indietro**</dt> <dt>1</dt> </dl>                                                        | Spostarsi all'indietro.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_FAVORITES"></span><span id="appcommand_browser_favorites"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ Preferiti**</dt> <dt>6</dt> </dl>                                                     | Apri Preferiti.<br/>                                                                                                                                                                                                                                                                 |
| <span id="APPCOMMAND_BROWSER_FORWARD"></span><span id="appcommand_browser_forward"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ successivo**</dt> <dt>2</dt> </dl>                                                           | Spostarsi in futuro.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BROWSER_HOME"></span><span id="appcommand_browser_home"></span><dl> <dt>**APPCOMMAND \_ \_Home page del browser**</dt> <dt>7</dt> </dl>                                                                    | Spostarsi nella Home page.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_BROWSER_REFRESH"></span><span id="appcommand_browser_refresh"></span><dl> <dt>**APPCOMMAND \_ \_Aggiornamento del browser**</dt> <dt>3</dt> </dl>                                                           | Aggiorna pagina.<br/>                                                                                                                                                                                                                                                                   |
| <span id="APPCOMMAND_BROWSER_SEARCH"></span><span id="appcommand_browser_search"></span><dl> <dt>**APPCOMMAND \_ \_Ricerca browser**</dt> <dt>5</dt> </dl>                                                              | Aprire la ricerca.<br/>                                                                                                                                                                                                                                                                    |
| <span id="APPCOMMAND_BROWSER_STOP"></span><span id="appcommand_browser_stop"></span><dl> <dt>**APPCOMMAND \_ \_Arresto del browser**</dt> <dt>4</dt> </dl>                                                                    | Interrompi download.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_CLOSE"></span><span id="appcommand_close"></span><dl> <dt>**APPCOMMAND \_ Chiudi**</dt> <dt>31</dt> </dl>                                                                                         | Chiudere la finestra (non l'applicazione).<br/>                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_COPY"></span><span id="appcommand_copy"></span><dl> <dt>**APPCOMMAND \_ COPIA**</dt> <dt>36</dt> </dl>                                                                                            | Copiare la selezione.<br/>                                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_CORRECTION_LIST"></span><span id="appcommand_correction_list"></span><dl> <dt>**APPCOMMAND \_ \_Elenco correzioni**</dt> <dt>45</dt> </dl>                                                          | Visualizza l'elenco di correzioni quando una parola viene identificata erroneamente durante l'input vocale. <br/>                                                                                                                                                                                       |
| <span id="APPCOMMAND_CUT"></span><span id="appcommand_cut"></span><dl> <dt>**APPCOMMAND \_ TAGLIA**</dt> <dt>37</dt> </dl>                                                                                               | Taglia la selezione.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_DICTATE_OR_COMMAND_CONTROL_TOGGLE"></span><span id="appcommand_dictate_or_command_control_toggle"></span><dl> <dt>**APPCOMMAND \_ Interruttore di controllo di DETTAtura \_ o \_ comando \_ \_**</dt> <dt>43</dt> </dl> | Passa tra due modalità di input vocale: dettatura e comando/controllo (assegnando comandi a un'applicazione o accedendo ai menu). <br/>                                                                                                                                               |
| <span id="APPCOMMAND_FIND"></span><span id="appcommand_find"></span><dl> <dt>**APPCOMMAND \_ TROVA**</dt> <dt>28</dt> </dl>                                                                                            | Aprire la finestra di dialogo **trova** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_FORWARD_MAIL"></span><span id="appcommand_forward_mail"></span><dl> <dt>**APPCOMMAND \_ Invia \_ posta elettronica**</dt> <dt>40</dt> </dl>                                                                   | Inviare un messaggio di posta elettronica.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_HELP"></span><span id="appcommand_help"></span><dl> <dt>**APPCOMMAND \_ Guida**</dt> <dt>27</dt> </dl>                                                                                            | Aprire la finestra di dialogo della **Guida** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_LAUNCH_APP1"></span><span id="appcommand_launch_app1"></span><dl> <dt>**APPCOMMAND \_ AVVIARE \_ App1**</dt> <dt>17</dt> </dl>                                                                      | Avviare App1.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_APP2"></span><span id="appcommand_launch_app2"></span><dl> <dt>**APPCOMMAND \_ AVVIARE \_ App2**</dt> <dt>18</dt> </dl>                                                                      | Avviare App2.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_MAIL"></span><span id="appcommand_launch_mail"></span><dl> <dt>**APPCOMMAND \_ Avvia \_ posta**</dt> <dt>15</dt> </dl>                                                                      | Aprire la posta.<br/>                                                                                                                                                                                                                                                                      |
| <span id="APPCOMMAND_LAUNCH_MEDIA_SELECT"></span><span id="appcommand_launch_media_select"></span><dl> <dt>**APPCOMMAND \_ Supporti di avvio \_ \_ selezionare**</dt> <dt>16</dt> </dl>                                             | Passare alla modalità di selezione dei supporti.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_MEDIA_CHANNEL_DOWN"></span><span id="appcommand_media_channel_down"></span><dl> <dt>**APPCOMMAND \_ \_Canale multimediale \_ inattivo**</dt> <dt>52</dt> </dl>                                                | Decrementare il valore del canale, ad esempio, per un sintonizzatore TV o radio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_CHANNEL_UP"></span><span id="appcommand_media_channel_up"></span><dl> <dt>**APPCOMMAND \_ \_Canale multimediale \_ su**</dt> <dt>51</dt> </dl>                                                      | Incrementare il valore del canale, ad esempio, per un sintonizzatore TV o radio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_FAST_FORWARD"></span><span id="appcommand_media_fast_forward"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ veloce \_ in futuro**</dt> <dt>49</dt> </dl>                                                | Aumentare la velocità di riproduzione del flusso. Questa operazione può essere implementata in molti modi, ad esempio, utilizzando una velocità fissa o attivando una serie di velocità crescenti. <br/>                                                                                                               |
| <span id="APPCOMMAND_MEDIA_NEXTTRACK"></span><span id="appcommand_media_nexttrack"></span><dl> <dt>**APPCOMMAND \_ \_NEXTTRACK media**</dt> <dt>11</dt> </dl>                                                          | Vai alla traccia successiva.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_MEDIA_PAUSE"></span><span id="appcommand_media_pause"></span><dl> <dt>**APPCOMMAND \_ \_Sospensione supporti**</dt> <dt>47</dt> </dl>                                                                      | Sospendi. Se già sospesa, non eseguire altre azioni. Si tratta di un comando di sospensione diretta senza stato. Se sono presenti pulsanti di riproduzione e sospensione discreti, le applicazioni devono eseguire l'azione su questo comando, oltre a **APPCOMMAND \_ media \_ Play \_ pause**. <br/>                               |
| <span id="APPCOMMAND_MEDIA_PLAY"></span><span id="appcommand_media_play"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PLAY**</dt> <dt>46</dt> </dl>                                                                         | Inizia la riproduzione nella posizione corrente. Se già sospesa, verrà ripresa. Si tratta di un comando di riproduzione diretta senza stato. Se sono presenti pulsanti di **riproduzione** e **sospensione** discreti, le applicazioni devono eseguire l'azione su questo comando, oltre a **APPCOMMAND \_ media \_ Play \_ pause**.<br/> |
| <span id="APPCOMMAND_MEDIA_PLAY_PAUSE"></span><span id="appcommand_media_play_pause"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ Play \_ pausa**</dt> <dt>14</dt> </dl>                                                      | Riprodurre o sospendere la riproduzione. Se sono presenti pulsanti di **riproduzione** e **sospensione** discreti, le applicazioni devono eseguire l'azione su questo comando, così come **APPCOMMAND \_ media \_ Play** e **APPCOMMAND \_ media \_ pause**.<br/>                                                                          |
| <span id="APPCOMMAND_MEDIA_PREVIOUSTRACK"></span><span id="appcommand_media_previoustrack"></span><dl> <dt>**APPCOMMAND \_ \_PREVIOUSTRACK supporti**</dt> <dt>12</dt> </dl>                                              | Passa alla traccia precedente.<br/>                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_MEDIA_RECORD"></span><span id="appcommand_media_record"></span><dl> <dt>**APPCOMMAND \_ \_Record multimediale**</dt> <dt>48</dt> </dl>                                                                   | Inizia la registrazione del flusso corrente.<br/>                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_REWIND"></span><span id="appcommand_media_rewind"></span><dl> <dt>**APPCOMMAND \_ \_Riavvolgimento supporti**</dt> <dt>50</dt> </dl>                                                                   | Tornare all'indietro in un flusso a una velocità superiore. Questa operazione può essere implementata in molti modi, ad esempio, utilizzando una velocità fissa o attivando una serie di velocità crescenti. <br/>                                                                                                   |
| <span id="APPCOMMAND_MEDIA_STOP"></span><span id="appcommand_media_stop"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ Stop**</dt> <dt>13</dt> </dl>                                                                         | Arresta la riproduzione.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_MIC_ON_OFF_TOGGLE"></span><span id="appcommand_mic_on_off_toggle"></span><dl> <dt>**APPCOMMAND \_ \_ \_ \_ Interruttore MIC on off**</dt> <dt>44</dt> </dl>                                                  | Consente di abilitare o disabilitare il microfono.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_DOWN"></span><span id="appcommand_microphone_volume_down"></span><dl> <dt>**APPCOMMAND \_ VOLUME del microfono \_ \_ inferiore**</dt> a <dt>25</dt> </dl>                                    | Ridurre il volume del microfono.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_MUTE"></span><span id="appcommand_microphone_volume_mute"></span><dl> <dt>**APPCOMMAND \_ \_Volume microfono \_ muto**</dt> <dt>24</dt> </dl>                                    | Disattiva il microfono.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_UP"></span><span id="appcommand_microphone_volume_up"></span><dl> <dt>**APPCOMMAND \_ \_Volume microfono \_ fino a**</dt> <dt>26</dt> </dl>                                          | Aumentare il volume del microfono.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_NEW"></span><span id="appcommand_new"></span><dl> <dt>**APPCOMMAND \_ NUOVO**</dt> <dt>29</dt> </dl>                                                                                               | Crea una nuova finestra.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_OPEN"></span><span id="appcommand_open"></span><dl> <dt>**APPCOMMAND \_ Apri**</dt> <dt>30</dt> </dl>                                                                                            | Aprire una finestra.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_PASTE"></span><span id="appcommand_paste"></span><dl> <dt>**APPCOMMAND \_ INCOLLARE**</dt> <dt>38</dt> </dl>                                                                                         | Incolla<br/>                                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_PRINT"></span><span id="appcommand_print"></span><dl> <dt>**APPCOMMAND \_ STAMPA**</dt> <dt>33</dt> </dl>                                                                                         | Stampa il documento corrente.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_REDO"></span><span id="appcommand_redo"></span><dl> <dt>**APPCOMMAND \_ ROLLFORWARD**</dt> <dt>35</dt> </dl>                                                                                            | Ripetere l'ultima azione.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_REPLY_TO_MAIL"></span><span id="appcommand_reply_to_mail"></span><dl> <dt>**APPCOMMAND \_ Rispondi \_ alla \_ posta**</dt> <dt>39</dt> </dl>                                                               | Rispondere a un messaggio di posta elettronica.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_SAVE"></span><span id="appcommand_save"></span><dl> <dt>**APPCOMMAND \_ Salva**</dt> <dt>32</dt> </dl>                                                                                            | Salva il documento corrente.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_SEND_MAIL"></span><span id="appcommand_send_mail"></span><dl> <dt>**APPCOMMAND \_ Invia \_ posta**</dt> <dt>41</dt> </dl>                                                                            | Inviare un messaggio di posta elettronica.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_SPELL_CHECK"></span><span id="appcommand_spell_check"></span><dl> <dt>**APPCOMMAND \_ \_Controllo ortografico**</dt> <dt>42</dt> </dl>                                                                      | Avviare un controllo ortografico.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_TREBLE_DOWN"></span><span id="appcommand_treble_down"></span><dl> <dt>**APPCOMMAND \_ TREBLE \_ giù**</dt> <dt>22</dt> </dl>                                                                      | Ridurre gli acuti.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_TREBLE_UP"></span><span id="appcommand_treble_up"></span><dl> <dt>**APPCOMMAND \_ ALTI \_**</dt> <dt>23</dt> </dl>                                                                            | Aumentare gli acuti.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_UNDO"></span><span id="appcommand_undo"></span><dl> <dt>**APPCOMMAND \_ Annulla**</dt> <dt>34</dt> </dl>                                                                                            | Annulla ultima azione.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_DOWN"></span><span id="appcommand_volume_down"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ inferiore**</dt> a <dt>9</dt> </dl>                                                                       | Abbassare il volume.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_MUTE"></span><span id="appcommand_volume_mute"></span><dl> <dt>**APPCOMMAND \_ \_Silenziamento del volume**</dt> <dt>8</dt> </dl>                                                                       | Disattivare il volume.<br/>                                                                                                                                                                                                                                                                |
| <span id="APPCOMMAND_VOLUME_UP"></span><span id="appcommand_volume_up"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_**</dt> <dt>10</dt> </dl>                                                                            | Aumentare il volume.<br/>                                                                                                                                                                                                                                                               |



 

Il componente *Udevice* indica il dispositivo di input che ha generato l'evento di input. i possibili valori sono i seguenti.



| Valore                                                                                                                                                                                                                                 | Significato                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="FAPPCOMMAND_KEY"></span><span id="fappcommand_key"></span><dl> <dt>**FAPPCOMMAND \_ CHIAVE**</dt> <dt>0</dt> </dl>            | L'utente ha premuto un tasto.<br/>                                                                           |
| <span id="FAPPCOMMAND_MOUSE"></span><span id="fappcommand_mouse"></span><dl> <dt>**FAPPCOMMAND \_**</dt> <dt>0x8000</dt> mouse </dl> | L'utente ha fatto clic con un pulsante del mouse.<br/>                                                                  |
| <span id="FAPPCOMMAND_OEM"></span><span id="fappcommand_oem"></span><dl> <dt>**FAPPCOMMAND \_**</dt> <dt>0x1000</dt> OEM </dl>       | L'evento è stato generato da un'origine hardware non identificata. Potrebbe trattarsi di un evento del mouse o della tastiera.<br/> |



 

Il componente *dwKeys* indica se varie chiavi virtuali sono inattive. i possibili valori sono i seguenti.



| Valore                                                                                                                                                                                                               | Significato                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0x0008</dt> di controllo </dl>    | Il tasto CTRL è premuto.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON </dl>    | Il pulsante sinistro del mouse è premuto.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON </dl>    | Il pulsante centrale del mouse è inattivo.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON </dl>    | Il pulsante destro del mouse è inattivo.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt> </dl>          | Il tasto MAIUSC è premuto.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1 </dl> | Il primo pulsante X è inattivo.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2 </dl> | Il secondo pulsante X è inattivo.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire **true**. Per ulteriori informazioni sull'elaborazione del valore restituito, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera il messaggio **WM \_ APPCOMMAND** quando elabora il messaggio [**WM \_ XBUTTONUP**](wm-xbuttonup.md) o [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md) oppure quando l'utente digita una chiave del comando dell'applicazione.

Se una finestra figlio non elabora questo messaggio e chiama invece [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), **DefWindowProc** invierà il messaggio alla relativa finestra padre. Se una finestra di primo livello non elabora questo messaggio e chiama invece **DefWindowProc**, **DefWindowProc** chiamerà un hook della shell con il codice hook uguale a **HSHELL \_ APPCOMMAND**.

Per ottenere le coordinate del cursore se il messaggio è stato generato con un clic del mouse, l'applicazione può chiamare [**GetMessagePos**](/windows/desktop/api/winuser/nf-winuser-getmessagepos). Un'applicazione può verificare se il messaggio è stato generato dal mouse controllando se *lParam* contiene **il \_ mouse FAPPCOMMAND**.

Diversamente da altri messaggi di Windows, un'applicazione deve restituire **true** da questo messaggio se lo elabora. In questo modo si consentirà il software che simula questo messaggio nei sistemi Windows precedenti a Windows 2000 per determinare se la routine della finestra ha elaborato il messaggio o chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OTTENERE \_ APPCOMMAND \_ lParam**](/windows/win32/api/winuser/nf-winuser-get_appcommand_lparam)
</dt> <dt>

[**Ottieni \_ \_ lParam dispositivo**](/windows/win32/api/winuser/nf-winuser-get_device_lparam)
</dt> <dt>

[**Ottieni \_ lParam stato \_**](/windows/win32/api/winuser/nf-winuser-get_keystate_lparam)
</dt> <dt>

[**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
</dt> <dt>

[**\_XBUTTONUP WM**](wm-xbuttonup.md)
</dt> <dt>

[**\_NCXBUTTONUP WM**](wm-ncxbuttonup.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input del mouse](mouse-input.md)
</dt> </dl>

 

