---
title: WM_APPCOMMAND messaggio (Winuser.h)
description: Notifica a una finestra che l'utente ha generato un evento di comando dell'applicazione, ad esempio facendo clic su un pulsante di comando dell'applicazione usando il mouse o digitando un tasto di comando dell'applicazione sulla tastiera.
ms.assetid: ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c
keywords:
- WM_APPCOMMAND messaggio Input tastiera e mouse
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
ms.openlocfilehash: 667b2974015edd8b8d3ac0505f4eb4d6c64d1da5b82737ec7d9bb89cc3e8776e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248005"
---
# <a name="wm_appcommand-message"></a>Messaggio \_ DI WM APPCOMMAND

Notifica a una finestra che l'utente ha generato un evento di comando dell'applicazione, ad esempio facendo clic su un pulsante di comando dell'applicazione usando il mouse o digitando un tasto di comando dell'applicazione sulla tastiera.


```C++
#define WM_APPCOMMAND                   0x0319
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra in cui l'utente ha fatto clic sul pulsante o ha premuto il tasto . Può trattarsi di una finestra figlio della finestra che riceve il messaggio. Per altre informazioni sull'elaborazione di questo messaggio, vedere la sezione Osservazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Usare il codice seguente per ottenere le informazioni contenute nel *parametro lParam.*


```
cmd  = GET_APPCOMMAND_LPARAM(lParam);

uDevice = GET_DEVICE_LPARAM(lParam);

dwKeys = GET_KEYSTATE_LPARAM(lParam);
```



Il comando dell'applicazione *è cmd*, che può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPCOMMAND_BASS_BOOST"></span><span id="appcommand_bass_boost"></span><dl> <dt>**APPCOMMAND \_ BASS \_ BOOST**</dt> <dt>20</dt> </dl>                                                                         | Attivare e disattivare la boost dei bassi.<br/>                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BASS_DOWN"></span><span id="appcommand_bass_down"></span><dl> <dt>**APPCOMMAND \_ BASSO \_ 19**</dt> <dt></dt> </dl>                                                                            | Ridurre i bassi.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BASS_UP"></span><span id="appcommand_bass_up"></span><dl> <dt>**APPCOMMAND \_ BASS \_ UP**</dt> <dt>21</dt> </dl>                                                                                  | Aumentare il basso.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_BACKWARD"></span><span id="appcommand_browser_backward"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ INDIETRO**</dt> <dt>1</dt> </dl>                                                        | Spostarsi all'indietro.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_FAVORITES"></span><span id="appcommand_browser_favorites"></span><dl> <dt>**APPCOMMAND \_ PREFERITI \_ DEL BROWSER**</dt> <dt>6</dt> </dl>                                                     | Aprire i Preferiti.<br/>                                                                                                                                                                                                                                                                 |
| <span id="APPCOMMAND_BROWSER_FORWARD"></span><span id="appcommand_browser_forward"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ FORWARD**</dt> <dt>2</dt> </dl>                                                           | Passare in avanti.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BROWSER_HOME"></span><span id="appcommand_browser_home"></span><dl> <dt>**APPCOMMAND \_ HOME \_ PAGE DEL BROWSER**</dt> <dt>7</dt> </dl>                                                                    | Passare alla home page.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_BROWSER_REFRESH"></span><span id="appcommand_browser_refresh"></span><dl> <dt>**APPCOMMAND \_ AGGIORNAMENTO \_ DEL BROWSER**</dt> <dt>3</dt> </dl>                                                           | Pagina Di aggiornamento.<br/>                                                                                                                                                                                                                                                                   |
| <span id="APPCOMMAND_BROWSER_SEARCH"></span><span id="appcommand_browser_search"></span><dl> <dt>**APPCOMMAND \_ RICERCA \_ NEL BROWSER**</dt> <dt>5</dt> </dl>                                                              | Aprire la ricerca.<br/>                                                                                                                                                                                                                                                                    |
| <span id="APPCOMMAND_BROWSER_STOP"></span><span id="appcommand_browser_stop"></span><dl> <dt>**APPCOMMAND \_ ARRESTO \_ DEL BROWSER**</dt> <dt>4</dt> </dl>                                                                    | Arrestare il download.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_CLOSE"></span><span id="appcommand_close"></span><dl> <dt>**APPCOMMAND \_ CLOSE**</dt> <dt>31</dt> </dl>                                                                                         | Chiudere la finestra (non l'applicazione).<br/>                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_COPY"></span><span id="appcommand_copy"></span><dl> <dt>**APPCOMMAND \_ COPIA**</dt> <dt>36</dt> </dl>                                                                                            | Copiare la selezione.<br/>                                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_CORRECTION_LIST"></span><span id="appcommand_correction_list"></span><dl> <dt>**APPCOMMAND \_ ELENCO \_ CORREZIONI**</dt> <dt>45</dt> </dl>                                                          | Apre l'elenco di correzioni quando una parola viene identificata in modo non corretto durante l'input vocale. <br/>                                                                                                                                                                                       |
| <span id="APPCOMMAND_CUT"></span><span id="appcommand_cut"></span><dl> <dt>**APPCOMMAND \_ CUT**</dt> <dt>37</dt> </dl>                                                                                               | Tagliare la selezione.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_DICTATE_OR_COMMAND_CONTROL_TOGGLE"></span><span id="appcommand_dictate_or_command_control_toggle"></span><dl> <dt>**APPCOMMAND \_ ATTIVARE \_ O \_ \_ DISATTIVARE IL CONTROLLO \_ DETTATO O COMANDO**</dt> <dt>43</dt> </dl> | Alterna due modalità di input vocale: dettatura e comando/controllo (invio di comandi a un'applicazione o accesso ai menu). <br/>                                                                                                                                               |
| <span id="APPCOMMAND_FIND"></span><span id="appcommand_find"></span><dl> <dt>**APPCOMMAND \_ TROVA**</dt> <dt>28</dt> </dl>                                                                                            | Aprire la **finestra di dialogo** Trova.<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_FORWARD_MAIL"></span><span id="appcommand_forward_mail"></span><dl> <dt>**APPCOMMAND \_ INOLTRA \_ POSTA**</dt> <dt>40</dt> </dl>                                                                   | Inoltrare un messaggio di posta elettronica.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_HELP"></span><span id="appcommand_help"></span><dl> <dt>**APPCOMMAND \_ HELP**</dt> <dt>27</dt> </dl>                                                                                            | Aprire la **finestra di dialogo** Guida.<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_LAUNCH_APP1"></span><span id="appcommand_launch_app1"></span><dl> <dt>**APPCOMMAND \_ AVVIARE \_ L'APP 1**</dt> <dt>17</dt> </dl>                                                                      | Avviare App1.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_APP2"></span><span id="appcommand_launch_app2"></span><dl> <dt>**APPCOMMAND \_ AVVIARE \_ L'APP 2**</dt> <dt>18</dt> </dl>                                                                      | Avviare App2.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_MAIL"></span><span id="appcommand_launch_mail"></span><dl> <dt>**APPCOMMAND \_ AVVIARE \_ MAIL**</dt> <dt>15</dt> </dl>                                                                      | Aprire la posta elettronica.<br/>                                                                                                                                                                                                                                                                      |
| <span id="APPCOMMAND_LAUNCH_MEDIA_SELECT"></span><span id="appcommand_launch_media_select"></span><dl> <dt>**APPCOMMAND \_ AVVIARE \_ MEDIA \_ SELECT**</dt> <dt>16</dt> </dl>                                             | Passare alla modalità Media Select (Selezione supporti).<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_MEDIA_CHANNEL_DOWN"></span><span id="appcommand_media_channel_down"></span><dl> <dt>**APPCOMMAND \_ CANALE \_ \_ MULTIMEDIALE IN BASSO**</dt> <dt>52</dt> </dl>                                                | Decrementare il valore del canale, ad esempio per un sintonizzatore TV o radio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_CHANNEL_UP"></span><span id="appcommand_media_channel_up"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ CHANNEL \_ UP**</dt> <dt>51</dt> </dl>                                                      | Incrementare il valore del canale, ad esempio, per un sintonizzatore TV o radio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_FAST_FORWARD"></span><span id="appcommand_media_fast_forward"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ FAST \_ FORWARD**</dt> <dt>49</dt> </dl>                                                | Aumentare la velocità di riproduzione del flusso. Questo può essere implementato in molti modi, ad esempio usando una velocità fissa o passando attraverso una serie di velocità crescenti. <br/>                                                                                                               |
| <span id="APPCOMMAND_MEDIA_NEXTTRACK"></span><span id="appcommand_media_nexttrack"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ NEXTTRACK**</dt> <dt>11</dt> </dl>                                                          | Passare alla traccia successiva.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_MEDIA_PAUSE"></span><span id="appcommand_media_pause"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PAUSE**</dt> <dt>47</dt> </dl>                                                                      | Sospendi. Se è già stato sospeso, non eseguire altre azioni. Si tratta di un comando PAUSE diretto senza stato. Se sono presenti pulsanti Play e Pause discreti, le applicazioni devono intervenire su questo comando e **su APPCOMMAND \_ MEDIA PLAY \_ \_ PAUSE**. <br/>                               |
| <span id="APPCOMMAND_MEDIA_PLAY"></span><span id="appcommand_media_play"></span><dl> <dt>**APPCOMMAND \_ RIPRODUZIONE \_ MULTIMEDIALE**</dt> <dt>46</dt> </dl>                                                                         | Iniziare a riprodurre nella posizione corrente. Se è già stata sospesa, verrà ripresa. Si tratta di un comando PLAY diretto senza stato. Se sono presenti pulsanti **Play** e **Pause** discreti, le applicazioni devono intervenire su questo comando e **su APPCOMMAND MEDIA PLAY \_ \_ \_ PAUSE**.<br/> |
| <span id="APPCOMMAND_MEDIA_PLAY_PAUSE"></span><span id="appcommand_media_play_pause"></span><dl> <dt>**APPCOMMAND \_ RIPRODUZIONE \_ \_ MULTIMEDIALE PAUSE**</dt> <dt>14</dt> </dl>                                                      | Riprodurre o sospendere la riproduzione. Se sono presenti pulsanti **Play** e **Pause** discreti, le applicazioni devono intervenire su questo comando, nonché **APPCOMMAND \_ MEDIA \_ PLAY** e **APPCOMMAND MEDIA \_ \_ PAUSE**.<br/>                                                                          |
| <span id="APPCOMMAND_MEDIA_PREVIOUSTRACK"></span><span id="appcommand_media_previoustrack"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PREVIOUSTRACK**</dt> <dt>12</dt> </dl>                                              | Passare alla traccia precedente.<br/>                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_MEDIA_RECORD"></span><span id="appcommand_media_record"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ RECORD**</dt> <dt>48</dt> </dl>                                                                   | Iniziare a registrare il flusso corrente.<br/>                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_REWIND"></span><span id="appcommand_media_rewind"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ REWIND**</dt> <dt>50</dt> </dl>                                                                   | Tornare indietro in un flusso a una velocità maggiore. Questo può essere implementato in molti modi, ad esempio usando una velocità fissa o passando attraverso una serie di velocità crescenti. <br/>                                                                                                   |
| <span id="APPCOMMAND_MEDIA_STOP"></span><span id="appcommand_media_stop"></span><dl> <dt>**APPCOMMAND \_ ARRESTO \_ MULTIMEDIALE**</dt> <dt>13</dt> </dl>                                                                         | Arrestare la riproduzione.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_MIC_ON_OFF_TOGGLE"></span><span id="appcommand_mic_on_off_toggle"></span><dl> <dt>**APPCOMMAND \_ MIC \_ ON \_ OFF \_ TOGGLE**</dt> <dt>44</dt> </dl>                                                  | Attivare/disattivare il microfono.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_DOWN"></span><span id="appcommand_microphone_volume_down"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ \_ MICROFONO IN BASSO**</dt> <dt>25</dt> </dl>                                    | Ridurre il volume del microfono.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_MUTE"></span><span id="appcommand_microphone_volume_mute"></span><dl> <dt>**APPCOMMAND \_ AUDIO \_ VOLUME \_ MICROFONO**</dt> <dt>24</dt> </dl>                                    | Disattivare l'audio del microfono.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_UP"></span><span id="appcommand_microphone_volume_up"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ DEL \_ MICROFONO 26**</dt> <dt></dt> </dl>                                          | Aumentare il volume del microfono.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_NEW"></span><span id="appcommand_new"></span><dl> <dt>**APPCOMMAND \_ NUOVO**</dt> <dt>29</dt> </dl>                                                                                               | Creare una nuova finestra.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_OPEN"></span><span id="appcommand_open"></span><dl> <dt>**APPCOMMAND \_ OPEN**</dt> <dt>30</dt> </dl>                                                                                            | Aprire una finestra.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_PASTE"></span><span id="appcommand_paste"></span><dl> <dt>**APPCOMMAND \_ INCOLLA**</dt> <dt>38</dt> </dl>                                                                                         | Incolla<br/>                                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_PRINT"></span><span id="appcommand_print"></span><dl> <dt>**APPCOMMAND \_ PRINT**</dt> <dt>33</dt> </dl>                                                                                         | Stampare il documento corrente.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_REDO"></span><span id="appcommand_redo"></span><dl> <dt>**APPCOMMAND \_ REDO**</dt> <dt>35</dt> </dl>                                                                                            | Ripetere l'ultima azione.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_REPLY_TO_MAIL"></span><span id="appcommand_reply_to_mail"></span><dl> <dt>**APPCOMMAND \_ RISPONDI \_ AL \_ MESSAGGIO**</dt> <dt>39</dt> </dl>                                                               | Rispondere a un messaggio di posta elettronica.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_SAVE"></span><span id="appcommand_save"></span><dl> <dt>**APPCOMMAND \_ SAVE**</dt> <dt>32</dt> </dl>                                                                                            | Salvare il documento corrente.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_SEND_MAIL"></span><span id="appcommand_send_mail"></span><dl> <dt>**APPCOMMAND \_ SEND \_ MAIL**</dt> <dt>41</dt> </dl>                                                                            | Inviare un messaggio di posta elettronica.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_SPELL_CHECK"></span><span id="appcommand_spell_check"></span><dl> <dt>**APPCOMMAND \_ CONTROLLO \_ ORTOGRAFICO**</dt> <dt>42</dt> </dl>                                                                      | Avviare un controllo ortografico.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_TREBLE_DOWN"></span><span id="appcommand_treble_down"></span><dl> <dt>**APPCOMMAND \_ TREBLE \_ DOWN**</dt> <dt>22</dt> </dl>                                                                      | Ridurre l'acuto.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_TREBLE_UP"></span><span id="appcommand_treble_up"></span><dl> <dt>**APPCOMMAND \_ TREBLE \_ UP**</dt> <dt>23</dt> </dl>                                                                            | Aumentare l'acuto.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_UNDO"></span><span id="appcommand_undo"></span><dl> <dt>**APPCOMMAND \_ UNDO**</dt> <dt>34</dt> </dl>                                                                                            | Annullare l'ultima azione.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_DOWN"></span><span id="appcommand_volume_down"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ IN BASSO**</dt> <dt>9</dt> </dl>                                                                       | Ridurre il volume.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_MUTE"></span><span id="appcommand_volume_mute"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ MUTE**</dt> <dt>8</dt> </dl>                                                                       | Disattivare l'audio del volume.<br/>                                                                                                                                                                                                                                                                |
| <span id="APPCOMMAND_VOLUME_UP"></span><span id="appcommand_volume_up"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ FINO**</dt> <dt>A 10</dt> </dl>                                                                            | Aumentare il volume.<br/>                                                                                                                                                                                                                                                               |



 

Il *componente uDevice* indica il dispositivo di input che ha generato l'evento di input e può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                 | Significato                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="FAPPCOMMAND_KEY"></span><span id="fappcommand_key"></span><dl> <dt>**FAPPCOMMAND \_ CHIAVE**</dt> <dt>0</dt> </dl>            | L'utente ha premuto un tasto.<br/>                                                                           |
| <span id="FAPPCOMMAND_MOUSE"></span><span id="fappcommand_mouse"></span><dl> <dt>**FAPPCOMMAND \_ Mouse**</dt> <dt>0x8000</dt> </dl> | L'utente ha fatto clic su un pulsante del mouse.<br/>                                                                  |
| <span id="FAPPCOMMAND_OEM"></span><span id="fappcommand_oem"></span><dl> <dt>**FAPPCOMMAND \_ OEM**</dt> <dt>0x1000</dt> </dl>       | Un'origine hardware non identificata ha generato l'evento. Può trattarsi di un evento del mouse o della tastiera.<br/> |



 

Il *componente dwKeys* indica se varie chiavi virtuali sono in stato di insiere e possono essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                               | Significato                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Controllo**</dt> <dt>0x0008</dt> </dl>    | Il tasto CTRL è premuto.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | Il pulsante sinistro del mouse è in basso.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | Il pulsante centrale del mouse è in basso.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | Il pulsante destro del mouse è in basso.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt> </dl>          | Il tasto MAIUSC è premuto.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | Il primo pulsante X è in basso.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Il secondo pulsante X è in basso.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire **TRUE.** Per altre informazioni sull'elaborazione del valore restituito, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera il messaggio **\_ WM APPCOMMAND** quando elabora il messaggio [**WM \_ XBUTTONUP**](wm-xbuttonup.md) o [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md) o quando l'utente digitare un tasto di comando dell'applicazione.

Se una finestra figlio non elabora questo messaggio e chiama [**invece DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) **DefWindowProc** invierà il messaggio alla finestra padre. Se una finestra di primo livello non elabora questo messaggio e chiama **invece DefWindowProc,** **DefWindowProc** chiamerà un hook della shell con il codice hook uguale a **HSHELL \_ APPCOMMAND**.

Per ottenere le coordinate del cursore se il messaggio è stato generato da un clic del mouse, l'applicazione può [**chiamare GetMessagePos.**](/windows/desktop/api/winuser/nf-winuser-getmessagepos) Un'applicazione può verificare se il messaggio è stato generato dal mouse controllando se *lParam* contiene **FAPPCOMMAND \_ MOUSE.**

A differenza di altri messaggi di Windows, un'applicazione deve restituire **TRUE** da questo messaggio se viene elaborata. In questo modo il software che simula questo messaggio nei sistemi Windows precedenti a Windows 2000 sarà in grado di determinare se la procedura finestra ha elaborato il messaggio o ha chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ APPCOMMAND \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_appcommand_lparam)
</dt> <dt>

[**GET \_ DEVICE \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_device_lparam)
</dt> <dt>

[**GET \_ KEYSTATE \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_lparam)
</dt> <dt>

[**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
</dt> <dt>

[**WM \_ XBUTTONUP**](wm-xbuttonup.md)
</dt> <dt>

[**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Mouse Input](mouse-input.md)
</dt> </dl>

 

