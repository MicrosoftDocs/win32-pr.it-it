---
title: Comando MCI_SETVIDEO (mmsystem. h)
description: Il \_ comando MCI sevideo imposta i valori associati alla riproduzione video. I dispositivi Digital-video e VCR riconoscono questo comando.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- Comando MCI_SETVIDEO Windows Multimedia
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
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476882"
---
# <a name="mci_setvideo-command"></a>\_Comando MCI SEvideo

Il \_ comando MCI sevideo imposta i valori associati alla riproduzione video. I dispositivi Digital-video e VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

**MCI \_ NOTIFICA**, **MCI \_ wait** o **MCI \_ test**. Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Con il tipo di dispositivo "digitalvideo" vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ video \_ ALG
</dt> <dd>

Il membro **lpstrAlgorithm** della struttura identificata da *lpSetVideo* contiene un indirizzo di un buffer contenente il nome di un algoritmo di compressione video. L'algoritmo di compressione viene usato dai comandi di [ \_ riserva MCI](mci-reserve.md) o del [ \_ record MCI](mci-record.md) successivi. Gli algoritmi disponibili sono dipendenti dal dispositivo.

Se l'algoritmo specificato non è compatibile con il formato di file corrente, il formato del file viene modificato nel formato predefinito per l'algoritmo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>CLOCKTIME DGV di MCI- \_ \_ video \_
</dt> <dd>

Se usato con **MCI \_ DGV \_ video \_ over**, indica che l'ora è specificata in millisecondi ed è il tempo assoluto. Questa volta non è al passo con la riproduzione dell'area di lavoro.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>\_ \_ input video DGV MCI \_
</dt> <dd>

Modifica la **\_ \_ \_ luminosità del video MCI DGV**, **MCI \_ DGV \_ sevideo \_ color**, **MCI \_ DGV \_ sevideo \_ Contrast**, **MCI \_ DGV \_ \_** sevideo gamma, **MCI \_ DGV \_ sevideo \_ nitidity** o **MCI \_ DGV \_ sevideo \_ tinte** in modo che influisca sul segnale di input e modifichi gli elementi registrati. Se possibile, si tratta dell'impostazione predefinita durante il monitoraggio dell'input.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>\_elemento DGV del \_ video \_ MCI
</dt> <dd>

Una costante video viene specificata nel membro **dwItem** della struttura identificata da *lpSetVideo*. La costante identifica il valore che viene impostato. Con questo flag è possibile specificare le costanti seguenti:

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>\_procedura di \_ estrazione del \_ video \_ di MCI AVI
</dt> <dd>

Un nuovo indirizzo della procedura di disegno viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*. È possibile specificare una nuova procedura di disegno solo quando il dispositivo è inattivo. Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI. Non esiste alcun equivalente a questo flag nell'interfaccia del comando di stringa.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>\_ \_ \_ colore tavolozza video di MCI AVI \_
</dt> <dd>

Un nuovo colore della tavolozza viene specificato nei membri **dwOver** e **dwValue** della struttura identificata da *lpSetVideo*. Il membro **dwOver** specifica l'indice della tavolozza del colore da modificare e il membro **dwValue** specifica il nuovo colore come valore RGB. Quando si usa questa costante, è necessario specificare anche i flag di valore **\_ DGV \_ \_** di MCI DGV e i flag di **\_ \_ \_ valore video** di MCI con la **\_ \_ \_ voce MCI DGV** . Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>\_mezzitoni della \_ tavolozza del video MCI AVI \_ \_
</dt> <dd>

Indica che deve essere utilizzata la tavolozza dei mezzitoni, anziché la tavolozza predefinita. Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>BITSPERPEL DGV di MCI- \_ \_ video \_
</dt> <dd>

Il numero di bit per pixel è specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*. Il numero di bit per pixel viene usato per salvare i dati acquisiti o registrati

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>\_luminosità del \_ video DGV \_ MCI
</dt> <dd>

Il livello di luminosità del video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>\_colore del \_ video DGV \_ MCI
</dt> <dd>

Il livello di saturazione dei colori video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>\_contrasto del \_ video DGV \_ MCI
</dt> <dd>

Il livello di contrasto video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>\_ \_ \_ frequenza dei FOTOgrammi DGV \_ MCI
</dt> <dd>

Viene specificata una frequenza dei fotogrammi nel membro **dwValue** della struttura identificata da *lpSetVideo*. La frequenza viene specificata in unità di fotogrammi al secondo per 1000. Ad esempio, 29,97 frame al secondo viene specificato come 29970.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>\_gamma di \_ video DGV \_ MCI
</dt> <dd>

Un valore dell'esponente di correzione gamma viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*. La correzione gamma regola il mapping tra l'intensità codificata nell'origine della presentazione e la luminosità visualizzata. Il valore è l'esponente moltiplicato per 1000. 2200, ad esempio, indica un esponente di 2,2. Il valore 1000 indica un esponente di 1, che non applica alcuna correzione gamma.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>\_colore della \_ chiave DGV del video MCI \_ \_
</dt> <dd>

Il colore della chiave viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*. Il colore della chiave è un valore RGB.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>\_ \_ \_ indice chiave video DGV MCI \_
</dt> <dd>

Il valore di indice della chiave viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*. Il parametro di indice è un indice della tavolozza fisica.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>PALHANDLE DGV di MCI- \_ \_ video \_
</dt> <dd>

Un handle della tavolozza viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*. L'handle della tavolozza è contenuto nella parola di ordine inferiore. I dispositivi digitali video non devono liberare la tavolozza passata con questo comando. Le applicazioni devono liberarsi dopo la chiusura del dispositivo. Questo flag è supportato solo dai dispositivi che utilizzano tavolozze. Se questo handle della tavolozza specificato è zero, viene utilizzata la tavolozza predefinita.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>\_ \_ nitidezza video MCI \_ DGV
</dt> <dd>

Un valore di nitidezza del video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>\_ \_ origine video DGV MCI \_
</dt> <dd>

Una costante che specifica l'origine dell'input video è specificata nel membro **dwValue** della struttura identificata da *lpSetVideo*. Sono definite le costanti seguenti:

-   **MCI \_ DGV \_ video \_ src \_ NTSC**: NTSC Television.
-   MCI \_ DGV \_ video \_ src \_ PAL: PAL Television.
-   MCI \_ DGV video \_ \_ src \_ RGB: video RGB.
-   MCI \_ DGV \_ video \_ src \_ SECAM: SECAM Television.
-   MCI \_ DGV video \_ \_ src \_ SVIDEO: S-video.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>\_flusso DGV del \_ video \_ MCI
</dt> <dd>

Un flusso video viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*. Il valore integer specifica il flusso video riprodotto dall'area di lavoro. Se il flusso non è specificato e il formato del file non definisce un flusso predefinito, viene riprodotto il primo flusso video con interfoliazione fisico.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>\_ \_ tinta del video DGV MCI \_
</dt> <dd>

Un valore di tinta video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*. In genere, questa regolazione viene modellata dopo il controllo della tinta di molti set di televisori dei colori, con 250 definito come verde, 750 definito come rosso e 0 (o 1000) definito come blu. Il valore nominale è sempre 500.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>\_output del \_ video DGV \_ MCI
</dt> <dd>

La **\_ \_ \_ luminosità del video MCI DGV**, **MCI \_ DGV \_ sevideo \_ color**, **MCI \_ DGV \_ sevideo \_ Contrast**, **MCI \_ DGV \_ \_** sevideo gamma, **MCI \_ DGV \_ sevideo \_ nitidity** o **MCI \_ DGV \_ sevideo \_ tinte** flag viene modificato in modo che influisca solo sul segnale visualizzato e non su ciò che viene registrato. Se possibile, si tratta dell'impostazione predefinita durante il monitoraggio di un file.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>DGV di MCI \_ \_ \_
</dt> <dd>

Un parametro della lunghezza della transizione è incluso nel membro **dwOver** della struttura identificata da *lpSetVideo*. La lunghezza della transizione specifica la durata (nel formato dell'ora corrente) che deve essere necessaria per apportare una modifica. Se questo flag non viene utilizzato, la modifica viene eseguita immediatamente.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>\_qualità del \_ video DGV \_ MCI
</dt> <dd>

Il membro **lpstrQuality** della struttura identificata da *lpSetVideo* contiene un indirizzo di un buffer che descrive la qualità del video. Una stringa di testo nel buffer specifica le caratteristiche dell'algoritmo di compressione video.

Per selezionare un descrittore di qualità per l'algoritmo specificato, è possibile usare il flag **MCI \_ DGV \_ sevideo \_ ALG** . Se questo flag viene omesso, viene utilizzato l'algoritmo corrente.

Gli algoritmi e i nomi dei descrittori disponibili dipendono dal dispositivo. Ogni dispositivo fornisce la documentazione per gli algoritmi disponibili e una descrizione dei nomi di descrittori applicabili. Il comando [MCI \_ Quality](mci-quality.md) può definire nomi di descrittori aggiuntivi. Tutti i dispositivi supportano i descrittori "low", "medium" e "High". Il valore predefinito è specifico del driver.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>\_ \_ record video DGV MCI \_
</dt> <dd>

Specifica se la registrazione include o esclude i dati video. In combinazione con **MCI \_ impostato \_ su**, i dati video vengono registrati. Se combinato con **MCI \_ impostato su \_ disattivato**, i dati video vengono esclusi. Il valore predefinito include i dati video.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>\_ \_ numero src del video \_ DGV \_ di MCI
</dt> <dd>

Un numero per l'origine video viene specificato nel membro **dwSourceNumber** della struttura identificata da *lpSetVideo*. Se è presente più di un input del tipo specificato dal **\_ \_ \_ valore DGV di MCI**, il valore seleziona l'input. Questo flag deve essere sempre utilizzato con **l' \_ \_ \_ origine DGV di MCI**. Se **il \_ \_ \_ valore DGV di MCI** viene omesso, tuttavia, il numero di origine specificato indica l'origine assoluta da usare come specificato nel [comando \_ elenco MCI](mci-list.md) .

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>DGV di MCI- \_ \_ video \_ ancora
</dt> <dd>

Il nome dell'algoritmo o il valore di qualità specificato si applica alle immagini ancora.

Ogni driver di dispositivo deve supportare un algoritmo di "None", che significa nessuna compressione. Questo è il valore predefinito. In questo caso, i dispositivi digitali video salvano le immagini ancora come bitmap indipendenti dal dispositivo RGB.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>\_ \_ valore video DGV MCI \_
</dt> <dd>

Un valore è incluso nel membro **dwValue** della struttura identificata da *lpSetVideo*. Il significato del valore è specificato dal flag dell' **\_ \_ \_ elemento DGV di MCI** .

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato
</dt> <dd>

Disabilita l'output del video. Per i dispositivi digitali video, la disabilitazione del video imposta i pixel nel rettangolo di destinazione definito dal comando [MCI \_ put](mci-put.md) (o il relativo valore predefinito, l'area client della finestra corrente) su un colore a tinta unita, ma non ha alcun effetto sul buffer del frame. Se lo si desidera, è possibile nascondere la finestra con il comando della [ \_ finestra MCI](mci-window.md) . L'origine del video, sia che si tratti di un'area di lavoro o di un input esterno, potrebbe continuare a archiviare nuove immagini nel buffer frame, ma non vengono visualizzate finché il video non è abilitato. Sebbene le applicazioni usino il \_ comando MCI sevideo per controllare questa funzione, i dispositivi video digitali devono ancora supportare questo flag. Il valore predefinito dopo l'apertura è on.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su
</dt> <dd>

Abilita l'output del video.

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpSetVideo* punta a una [**struttura \_ DGV \_ \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) .

Con il tipo di dispositivo "VCR" vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>\_ \_ record video MCI VCR \_
</dt> <dd>

Imposta la registrazione video su on o off. Usato insieme a uno dei flag seguenti:

-   **MCI \_ IMPOSTA \_ su**. Registrazione video su.
-   **MCI \_ IMPOSTARE \_ disattivato**. Registrazione video disattivata. Prima di disattivare la registrazione video, potrebbe essere necessario disattivare la registrazione di assemblaggio (usando il comando [MCI \_ set](mci-set.md) con il flag **MCI \_ \_ set \_ assembla \_ record** impostato su OFF).

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>\_traccia MCI
</dt> <dd>

Il membro **dwTrack** della struttura identificata da *lpSetVideo* specifica la traccia interessata dal comando.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>\_ \_ origine video VCR MCI \_
</dt> <dd>

Imposta l'origine video e deve essere usata con il **\_ \_ sevideo MCI VCR \_ per** contrassegnare.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>\_ \_ monitoraggio video VCR MCI \_
</dt> <dd>

Imposta il monitoraggio origine video e deve essere usato con il \_ \_ sevideo MCI VCR \_ per contrassegnare.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>\_video MCI VCR \_ \_ in
</dt> <dd>

Il membro **dwTo** della struttura identificata da *lpSetVideo* contiene una delle costanti seguenti:

<dl> <dd>**\_Tuner di \_ \_ tipo src VCR di \_ MCI**</dd> <dd>**\_ \_ \_ riga tipo src VCR \_ MCI**</dd> <dd>**\_ \_ tipo src VCR \_ MCI \_ aux**</dd> <dd>**\_ \_ tipo src VCR \_ MCI \_ generico**</dd> <dd>**\_silenziamento del \_ \_ tipo src del VCR \_ MCI**</dd> <dd>**\_ \_ \_ output tipo src VCR \_ MCI**</dd> <dd>**\_tipo src del VCR MCI \_ \_ \_ RGB**</dd> <dd>**\_numero di \_ video VCR \_ MCI**</dd> </dl>

Il membro **dwNumber** della struttura identificata da *lpSetVideo* contiene l'input video, del tipo specificato nel membro **dwTo** , da usare.

</dd> </dl>

Per i dispositivi VCR, il parametro *lpSetVideo* punta a una struttura [**\_ \_ \_ parametri del videoregistratore MCI**](mci-vcr-setvideo-parms.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandi MCI](mci-commands.md)
</dt> </dl>

 

