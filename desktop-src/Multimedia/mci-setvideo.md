---
title: MCI_SETVIDEO comando (Mmsystem.h)
description: Il comando MCI \_ SETVIDEO imposta i valori associati alla riproduzione video. I dispositivi video e videoregistratori digitali riconoscono questo comando.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- MCI_SETVIDEO comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23206d169ad5e273927ead247c44194660c8d6b201c725e1b4d4ab24fd5e1544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803378"
---
# <a name="mci_setvideo-command"></a>Comando MCI \_ SETVIDEO

Il comando MCI \_ SETVIDEO imposta i valori associati alla riproduzione video. I dispositivi video e videoregistratori digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

**MCI \_ NOTIFY,** **MCI \_ WAIT** o **MCI \_ TEST**. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*
</dt> <dd>

Puntatore a [**una struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti vengono usati con il tipo di dispositivo "digitalvideo":

<dl> <dt>

<span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ SETVIDEO \_ ALG
</dt> <dd>

Il **membro lpstrAlgorithm** della struttura identificata da *lpSetVideo* contiene un indirizzo di un buffer contenente il nome di un algoritmo di compressione video. L'algoritmo di compressione viene usato dai comandi [MCI \_ RESERVE](mci-reserve.md) o [MCI \_ RECORD successivi.](mci-record.md) Gli algoritmi disponibili dipendono dal dispositivo.

Se l'algoritmo specificato non è compatibile con il formato di file corrente, il formato di file viene modificato nel formato predefinito per l'algoritmo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ SETVIDEO \_ CLOCKTIME
</dt> <dd>

Se usato con **MCI \_ DGV \_ SETVIDEO \_ OVER,** indica che il tempo è specificato in millisecondi ed è il tempo assoluto. Questa volta non è in esecuzione la riproduzione dell'area di lavoro.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI \_ DGV \_ SETVIDEO \_ INPUT
</dt> <dd>

Modifica **MCI \_ DGV \_ SETVIDEO \_ BRIGHTNESS,** **MCI \_ DGV \_ SETVIDEO \_ COLOR,** **MCI \_ DGV \_ SETVIDEO \_ CONTRAST,** **MCI \_ DGV \_ SETVIDEO \_ GAMMA,** **MCI \_ DGV \_ SETVIDEO \_ SHARPNESS** o **MCI \_ DGV \_ SETVIDEO \_ TINT** in modo che influisca sul segnale di input e modifichi ciò che viene registrato. Se possibile, si tratta dell'impostazione predefinita quando si monitora l'input.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>ELEMENTO MCI \_ DGV \_ SETVIDEO \_
</dt> <dd>

Una costante video viene specificata nel **membro dwItem** della struttura identificata da *lpSetVideo*. La costante identifica il valore impostato. Con questo flag è possibile specificare le costanti seguenti:

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>PROCEDURA DI DISEGNO DI MCI \_ AVI \_ SETVIDEO \_ \_
</dt> <dd>

Nel membro **dwValue** della struttura identificata da *lpSetVideo* viene specificato un nuovo indirizzo della procedura di disegno. È possibile specificare una nuova procedura di disegno solo quando il dispositivo è inattivo. Questo flag è riconosciuto solo dal driver video digitale MCIAVI. Non esiste alcun equivalente a questo flag nell'interfaccia di comando della stringa.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI \_ AVI \_ SETVIDEO \_ PALETTE \_ COLOR
</dt> <dd>

Un nuovo colore della tavolozza viene specificato nei **membri dwOver** e **dwValue** della struttura identificata da *lpSetVideo*. Il **membro dwOver** specifica l'indice della tavolozza del colore da modificare e il membro **dwValue** specifica il nuovo colore, come valore RGB. È inoltre necessario specificare i flag **MCI \_ DGV \_ SETVIDEO \_ OVER** e **MCI \_ DGV \_ SETVIDEO \_ VALUE** con **MCI \_ DGV \_ SETVIDEO \_ ITEM** quando si usa questa costante. Questo flag è riconosciuto solo dal driver video digitale MCIAVI.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI \_ AVI \_ SETVIDEO \_ PALETTE \_ HALFTONE
</dt> <dd>

Indica che deve essere usata la tavolozza dei mezzitoni anziché quella predefinita. Questo flag è riconosciuto solo dal driver video digitale MCIAVI.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ SETVIDEO \_ BITSPERPEL
</dt> <dd>

Il numero di bit per pixel è specificato nel **membro dwValue** della struttura identificata da *lpSetVideo*. Il numero di bit per pixel viene usato per salvare i dati acquisiti o registrati

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI \_ DGV \_ SETVIDEO \_ BRIGHTNESS
</dt> <dd>

Il livello di luminosità video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI \_ DGV \_ SETVIDEO \_ COLOR
</dt> <dd>

Il livello di saturazione del colore video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI \_ DGV \_ SETVIDEO \_ CONTRAST
</dt> <dd>

Il livello di contrasto video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI \_ DGV \_ SETVIDEO \_ FRAME \_ RATE
</dt> <dd>

Nel membro **dwValue** della struttura identificata da *lpSetVideo* viene specificata una frequenza dei fotogrammi. La frequenza è specificata in unità di fotogrammi al secondo per 1000. Ad esempio, 29,97 fotogrammi al secondo viene specificato come 29970.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI \_ DGV \_ SETVIDEO \_ GAMMA
</dt> <dd>

Un valore esponente della correzione gamma viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*. Correzione gamma regola il mapping tra l'intensità codificata nell'origine della presentazione e la luminosità visualizzata. Il valore è l'esponente moltiplicato per 1000. Ad esempio, 2200 indica un esponente di 2.2. Il valore 1000 indica un esponente di 1, che non applica alcuna correzione gamma.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI \_ DGV \_ SETVIDEO \_ KEY \_ COLOR
</dt> <dd>

Un colore della chiave viene specificato nel **membro dwValue** della struttura identificata da *lpSetVideo*. Il colore della chiave è un valore RGB.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI \_ DGV \_ SETVIDEO \_ KEY \_ INDEX
</dt> <dd>

Un valore di indice della chiave viene specificato nel **membro dwValue** della struttura identificata da *lpSetVideo*. Il parametro index è un indice del riquadro fisico.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ SETVIDEO \_ PALHANDLE
</dt> <dd>

Un handle del riquadro viene specificato nel **membro dwValue** della struttura identificata da *lpSetVideo*. L'handle del riquadro è contenuto nella parola di ordine basso. I dispositivi digital-video non devono liberare la tavolozza passata con questo comando. Le applicazioni devono liberarlo dopo la chiusura del dispositivo. Questo flag è supportato solo dai dispositivi che usano i palette. Se l'handle del riquadro specificato è zero, viene usato il riquadro predefinito.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI \_ DGV \_ SETVIDEO \_ SHARPNESS
</dt> <dd>

Un valore di nitidezza video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>ORIGINE MCI \_ DGV \_ SETVIDEO \_
</dt> <dd>

Una costante che specifica l'origine dell'input video viene specificata nel membro **dwValue** della struttura identificata da *lpSetVideo*. Sono definite le costanti seguenti:

-   **MCI \_ DGV \_ SETVIDEO \_ SRC \_ NTSC:** NTSC tv.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ PAL: PAL tv.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB: video RGB.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM: SECAM tv.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO: S-Video.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI \_ DGV \_ SETVIDEO \_ STREAM
</dt> <dd>

Un flusso video viene specificato nel **membro dwValue** della struttura identificata da *lpSetVideo*. Il valore intero specifica il flusso video riprodotto dall'area di lavoro. Se il flusso non viene specificato e il formato di file non definisce un flusso predefinito, viene riprodotto il primo flusso video con interfoliazione fisica.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI \_ DGV \_ SETVIDEO \_ TINT
</dt> <dd>

Un valore di tinta video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*. In genere, questa regolazione viene modellata in base al controllo della tinta di molti set televisivi a colori, con 250 definiti come verde, 750 definiti come rosso e 0 (o 1000) definiti come blu. Il valore nominale è sempre 500.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>OUTPUT DI MCI \_ DGV \_ SETVIDEO \_
</dt> <dd>

IL FLAG **MCI \_ DGV \_ SETVIDEO \_ BRIGHTNESS,** **MCI \_ DGV \_ SETVIDEO \_ COLOR,** **MCI \_ DGV \_ SETVIDEO \_ CONTRAST,** **MCI \_ DGV \_ SETVIDEO \_ GAMMA,** **MCI \_ DGV \_ SETVIDEO \_ SHARPNESS** o **MCI \_ DGV \_ SETVIDEO \_ TINT** flag viene modificato in modo che influisca solo sul segnale visualizzato e non su ciò che viene registrato. Se possibile, questa è l'impostazione predefinita quando si monitora un file.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ SETVIDEO \_ OVER
</dt> <dd>

Un parametro di lunghezza della transizione è incluso nel **membro dwOver** della struttura identificata da *lpSetVideo*. La lunghezza della transizione specifica il tempo necessario (nel formato dell'ora corrente) per apportare una modifica. Se questo flag non viene utilizzato, la modifica viene eseguita immediatamente.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI \_ DGV \_ SETVIDEO \_ QUALITY
</dt> <dd>

Il **membro lpstrQuality** della struttura identificata da *lpSetVideo* contiene un indirizzo di un buffer che descrive la qualità del video. Una stringa di testo nel buffer specifica le caratteristiche dell'algoritmo di compressione video.

Il flag **MCI \_ DGV \_ SETVIDEO \_ ALG** può essere usato per selezionare un descrittore di qualità per l'algoritmo specificato. Se questo flag viene omesso, viene usato l'algoritmo corrente.

Gli algoritmi e i nomi dei descrittori disponibili dipendono dal dispositivo. Ogni dispositivo fornisce la documentazione per gli algoritmi disponibili e una descrizione dei nomi dei descrittori applicabili. Il [comando MCI \_ QUALITY](mci-quality.md) può definire nomi di descrittori aggiuntivi. Tutti i dispositivi supportano i descrittori "low", "medium" e "high". Il valore predefinito è specifico del driver.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI \_ DGV \_ SETVIDEO \_ RECORD
</dt> <dd>

Specifica se la registrazione include o esclude i dati video. In combinazione **con MCI \_ SET \_ ON,** vengono registrati i dati video. In combinazione **con MCI \_ SET \_ OFF,** i dati video vengono esclusi. L'impostazione predefinita include i dati video.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI \_ DGV \_ SETVIDEO \_ SRC \_ NUMBER
</dt> <dd>

Un numero per l'origine video è specificato nel **membro dwSourceNumber** della struttura identificata da *lpSetVideo*. Se è presente più di un input del tipo specificato da **MCI \_ DGV \_ SETVIDEO \_ VALUE,** il valore seleziona l'input. Questo flag deve essere sempre utilizzato con **MCI \_ DGV \_ SETVIDEO \_ SOURCE**. Se **si omette MCI \_ DGV \_ SETVIDEO \_ VALUE,** tuttavia, il numero di origine specificato indica l'origine assoluta da usare come specificato nel [comando MCI \_ LIST.](mci-list.md)

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI \_ DGV \_ SETVIDEO \_ STILL
</dt> <dd>

Il nome dell'algoritmo o il valore di qualità specificato si applica alle immagini fisse.

Ogni driver di dispositivo deve supportare un algoritmo "none", ovvero nessuna compressione. Questo è il valore predefinito. In questo caso, i dispositivi video digitali salvano le immagini fisse come bitmap RGB indipendenti dal dispositivo (DIB).

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI \_ DGV \_ SETVIDEO \_ VALUE
</dt> <dd>

Un valore è incluso nel **membro dwValue** della struttura identificata da *lpSetVideo*. Il significato del valore viene specificato dal flag **MCI \_ DGV \_ SETVIDEO \_ ITEM.**

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Disabilita l'output video. Per i dispositivi video digitali, la disabilitazione del video imposta i pixel nel rettangolo di destinazione definito dal comando [MCI \_ PUT](mci-put.md) (o l'area client predefinita della finestra corrente) su un colore a tinta unita, ma non ha alcun effetto sul buffer dei fotogrammi. Se si desidera, è possibile nascondere la finestra con il [ \_ comando MCI WINDOW.](mci-window.md) L'origine del video, che si tratta dell'area di lavoro o di un input esterno, potrebbe continuare a archiviare nuove immagini nel buffer dei fotogrammi, ma non vengono visualizzate fino a quando il video non viene abilitato. Anche se le applicazioni devono usare il comando MCI SETVIDEO per controllare questa funzione, i dispositivi \_ video digitali devono ancora supportare questo flag. Il valore predefinito dopo un'apertura è on.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Abilita l'output video.

</dd> </dl>

Per i dispositivi video digitali, il *parametro lpSetVideo* punta a una [**struttura \_ MCI DGV \_ SETVIDEO \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa)

I flag aggiuntivi seguenti vengono usati con il tipo di dispositivo "vcr":

<dl> <dt>

<span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI \_ VCR \_ SETVIDEO \_ RECORD
</dt> <dd>

Imposta la registrazione video su on o off. Usato in combinazione con uno dei flag seguenti:

-   **McI \_ SET \_ ON**. Registrazione video.
-   **McI \_ SET \_ OFF**. Registrazione video disattivata. Potrebbe essere necessario disattivare la registrazione di assemblaggio (usando il comando [MCI \_ SET](mci-set.md) con il flag **MCI \_ VCR \_ SET ASSEMBLE \_ \_ RECORD** impostato su off) prima di disattivare la registrazione video.

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>MCI \_ TRACK
</dt> <dd>

Il **membro dwTrack** della struttura identificata da *lpSetVideo* specifica quale traccia è interessata dal comando.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI \_ VCR \_ SETVIDEO \_ SOURCE
</dt> <dd>

Imposta l'origine video e deve essere usata con il flag **\_ MCI VCR \_ SETVIDEO \_ TO.**

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI \_ VCR \_ SETVIDEO \_ MONITOR
</dt> <dd>

Imposta il monitor di origine video e deve essere usato con il \_ flag MCI VCR \_ SETVIDEO \_ TO.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI \_ VCR \_ SETVIDEO \_ SU
</dt> <dd>

Il **membro dwTo** della struttura identificata da *lpSetVideo* contiene una delle costanti seguenti:

<dl> <dd>**SINER \_ DI TIPO MCI VCR \_ SRC \_ \_**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ LINE**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ AUX**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ GENERIC**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ MUTE**</dd> <dd>**OUTPUT DEL TIPO \_ SRC DEL VCR MCI \_ \_ \_**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ RGB**</dd> <dd>**MCI \_ VCR \_ SETVIDEO \_ NUMBER**</dd> </dl>

Il **membro dwNumber** della struttura identificata da *lpSetVideo* contiene l'input video (del tipo specificato nel **membro dwTo)** da usare.

</dd> </dl>

Per i dispositivi VCR, *il parametro lpSetVideo* punta a una [**struttura \_ MCI VCR \_ SETVIDEO \_ PARMS.**](mci-vcr-setvideo-parms.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandi MCI](mci-commands.md)
</dt> </dl>

 

