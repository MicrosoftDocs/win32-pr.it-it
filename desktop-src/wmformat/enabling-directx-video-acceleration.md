---
title: Attivazione dell'accelerazione video DirectX
description: Attivazione dell'accelerazione video DirectX
ms.assetid: 5cb2f564-88e3-4b60-bde3-6ccf69c97c48
keywords:
- Windows Media Format SDK, abilitazione di DXVA
- Windows Media Format SDK, accelerazione video DirectX (DXVA)
- Windows Media Format SDK, accelerazione video
- Formato Advanced Systems (ASF), abilitazione di DXVA
- ASF (Advanced Systems Format), abilitazione di DXVA
- Advanced Systems Format (ASF), accelerazione video DirectX (DXVA)
- ASF (Advanced Systems Format), accelerazione video DirectX (DXVA)
- ASF (Advanced Systems Format), accelerazione video
- ASF (Advanced Systems Format), accelerazione video
- Accelerazione video DirectX (DXVA), abilitazione
- DXVA (accelerazione video DirectX), abilitazione
- Accelerazione video DirectX (DXVA), ordine delle operazioni
- DXVA (accelerazione video DirectX), ordine delle operazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896147fe11b4b7f5fb91d8dc288e616b643bd5ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398550"
---
# <a name="enabling-directx-video-acceleration"></a>Attivazione dell'accelerazione video DirectX

Questa sezione descrive come abilitare Microsoft® DirectX® accelerazione video quando si riproduce contenuto trasmesso in un lettore personalizzato.

## <a name="background"></a>Sfondo

DirectX Video Acceleration (DirectX VA) è una specifica API per l'accelerazione hardware di operazioni di decodifica 2D. Consente ai decodificatori software di eseguire l'offload di alcune operazioni con utilizzo intensivo della CPU nella scheda grafica per l'elaborazione. Per gli utenti finali, questo rende possibile un video ad alta velocità, ad esempio la riproduzione di DVD a schermo intero in computer meno recenti dotati di schede grafiche compatibili con DirectX VA.

A partire da Windows Media Format 9 Series SDK, il filtro wrapper DMO supporta DirectX VA. Ciò significa che, per la riproduzione locale, le applicazioni possono usare il filtro per i lettori ASF WM per riprodurre contenuti basati su Windows Media e l'accelerazione hardware di DirectX VA richiamata automaticamente se la scheda grafica la supporta. Tuttavia, il filtro WM ASF Reader non supporta la riproduzione di contenuto trasmesso. Pertanto, se si desidera supportare DirectX VA quando si riproduce contenuto trasmesso in un lettore personalizzato, è necessario utilizzare un meccanismo alternativo, ovvero quello utilizzato da Windows Media Player a partire dalla serie Windows Media 9.

Poiché Windows Media Player è stato progettato prima dello sviluppo dei filtri QASF, Windows Media Player dispone di un proprio filtro di origine, basato su Windows Media Format SDK, per la riproduzione di contenuto basato su Windows Media. Il filtro origine Windows Media di WMP recapita i dati decompressi a valle direttamente ai renderer audio e video. Al contrario, il lettore WM ASF recapita contenuti compressi a valle di Windows Media Decoder DirectX Media Objects (DMOs), che sono ospitati all'interno del wrapper DMO. I diagrammi seguenti illustrano le differenze tra il lettore WM ASF e il filtro di origine Windows Media di WMP.

![il filtro di origine personalizzato genera esempi non compressi](images/wmp-dxva-graph.png)

![il filtro di origine qasf genera esempi compressi](images/qasf-dxva-graph.png)

Per abilitare DirectX VA per il contenuto trasmesso, è necessario creare un filtro di origine personalizzato come quello nel diagramma superiore. In sostanza, questo filtro userà Windows Media Format SDK per creare un'istanza di un oggetto WM Reader, decomprimere gli esempi e inviarli a valle sui pin di output. In questa discussione si presuppone che il filtro di origine sia già stato creato e che ora è possibile implementare il supporto di DirectX VA.

Per abilitare DirectX VA, l'attività di base del filtro di origine è fornire il renderer video e il decodificatore WMV DMO con le interfacce necessarie per negoziare la connessione DirectX VA. Il filtro di origine non partecipa a tali negoziazioni. Dopo l'avvio del flusso, l'unica attività correlata a DirectX che può essere eseguita dal filtro di origine consiste nel modificare i timestamp degli esempi video prima che il decodificatore WMV li recapita al renderer video. Il motivo principale è quello di fornire un controllo della sequenza temporale personalizzato oltre a quello abilitato dalle interfacce di® DirectShow standard.

Sono state definite tre interfacce per abilitare le comunicazioni necessarie tra Windows Media Format SDK, il filtro di origine del lettore, il decodificatore Windows Media Video DMO e il renderer di mixer o video mixing. Queste interfacce sono descritte nella tabella seguente.



| Interfaccia                                                        | Descrizione                                                                                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecAMVideoAccelerator**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator) | Esposto da Windows Media Decoder DMO e chiamato dal filtro di origine di un Media Player per configurare le varie connessioni necessarie per abilitare DirectX VA per la decodifica del contenuto Windows Media Video. |
| [**IWMPlayerTimestampHook**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook)         | Implementato nel filtro di origine del lettore. Consente al filtro di modificare i timestamp degli esempi video prima di distribuirli a valle.                                                 |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)             | Implementato nell'oggetto WM Reader. Viene chiamato da un filtro di origine del lettore per ottenere le interfacce dal decodificatore DMO.                                                                             |



 

## <a name="order-of-operations-in-directx-vaenabled-playback"></a>Ordine delle operazioni in DirectX VA-abilitata la riproduzione

In questa sezione viene descritto l'ordine generale delle operazioni in fase di esecuzione per un lettore DirectX abilitata e il relativo filtro di origine. I componenti a cui si fa riferimento in questa sezione sono:

-   Un lettore multimediale di terze parti, indicato come lettore.
-   Filtro di origine personalizzato, di cui è stata creata un'istanza dal lettore, che usa Windows Media Format SDK per decomprimere il contenuto basato su Windows Media.
-   Pin di output del video del filtro di origine del lettore, denominato PIN di output.
-   Il grafico del filtro per la riproduzione video DirectShow, denominato grafico.
-   Renderer di mixaggio video, denominato VMR.
-   Oggetto Reader asincrono di Windows Media Format SDK, denominato Reader.
-   Oggetto multimediale DirectX decodificatore Windows Media Video, denominato DMO del decodificatore.

L'ordine delle operazioni è il seguente:

1.  Il lettore crea un'istanza del filtro di origine e di un oggetto Reader. Il lettore crea un decodificatore video DMO e imposta il tipo di input (compresso) su di esso. Questa operazione deve verificarsi prima che il giocatore tenti di configurare il grafico di riproduzione video perché l'SDK e il decodificatore DMO devono essere interessati nel processo di negoziazione con il grafo e DMO deve essere in grado di rilevare il formato di input durante il passaggio 9.
2.  Il lettore chiama **IGraphBuilder:: Render**, specificando il pin di output del filtro origine video. A questo punto, la gestione del grafo del filtro DirectShow tenta di connettere il VMR al filtro di origine video del lettore.
3.  Filter Graph Manager chiama **Ipin:: Connect** sul pin di output del filtro di origine video del lettore.

I passaggi da 4 a 10 si verificano all'interno di **Ipin:: Connect**.

1.  Il filtro di origine Ottiene l'interfaccia **IWMCodecAMVideoAccelerator** dal metodo **IWMReaderAccelerator:: GetCodecInterface** del Reader. Se il codec non supporta DirectX VA, la chiamata a **GetCodecInterface** potrebbe non riuscire. In questo caso, la negoziazione procede come di consueto, senza il supporto di DirectX VA.
2.  Il filtro di origine passa il puntatore **IAMVideoAccelerator** dal pin passato in **Connect** al decodificatore DMO tramite **IWMCodecAMVideoAccelerator:: SetAcceleratorInterface**.
3.  Il filtro di origine delega quindi il resto dell'operazione **Ipin:: Connect** al metodo **CBaseOutputPin:: Connect** . L'enumerazione del formato con l'SDK continua come attualmente. Se il codec supporta DirectX VA per il contenuto connesso, il codec DMO presenta prima i sottotipi DirectX VA, prima dei tipi YUV e RGB supportati. Se è disponibile il supporto per DirectX VA, si tentano i passaggi da 7 a 11 nel contesto di un sottotipo di DirectX VA. Il frammento di codice seguente mostra come identificare un sottotipo di supporto DirectX VA.
    ```C++
    bool IsDXVASubtype( AM_MEDIA_TYPE * pmt )
    {
        // All DXVA types have the same last 3 DWORDs.
        // guidDXVA is the base GUID for all DXVA subtypes.

        GUID guidDXVA = { 0x00000000, 0xa0c7, 0x11d3, { 0xb9,0x84,0x00,0xc0,0x4f,0x2e,0x73,0xc5 } };

        unsigned long const * plguid;
        unsigned long const * plguidDXVA;
        plguid = (unsigned long const *)&pmt->subtype;
        plguidDXVA = (unsigned long *)&guidDXVA;

        if( ( plguid[1] == plguidDXVA[1] ) &&
            ( plguid[2] == plguidDXVA[2] ) &&
            ( plguid[3] == plguidDXVA[3] ) )
        {
            return true;
        }

        return false;
    }
    
    ```

    

4.  L'implementazione di **CBaseOutputPin:: Connect** chiama **Ipin:: CompleteConnect** durante il passaggio 3. Se viene considerato un sottotipo di DirectX VA, viene tentata la negoziazione di DirectX VA. Il pin di output chiama **IWMCodecAMVideoAccelerator:: NegotiateConnection**, passando il tipo di supporto di output corrente.
5.  Il decodificatore DMO esegue la negoziazione richiesta con VMR tramite l'interfaccia **IAMVideoAccelerator** e restituisce il GUID del sottotipo video che i due hanno concordato. Il pin di output delega tutte le chiamate **IAMVideoAcceleratorNotify** ricevute durante questo processo all'interfaccia **IAMVideoAcceleratorNotify** del decodificatore DMO, che può essere ottenuta anche tramite il metodo **IWMReaderAccelerator:: GetCodecInterface** .
6.  Se **NegotiateConnection** ha esito positivo, il pin di output chiama **IWMCodecAMVideoAccelerator:: SetPlayerNotify** con un'interfaccia **IWMPlayerTimestampHook** . Questo hook consente al filtro di origine di aggiornare i timestamp sugli esempi prima che vengano passati al renderer.
7.  Il filtro di origine chiama **IWMReaderAccelerator:: Notify** con il tipo di supporto negoziato. Ciò consente al lettore di aggiornare le variabili interne e di eseguire il commit in DirectX VA. Questa è l'ultima posizione in cui il codec o il lettore può avere esito negativo. Se uno dei passaggi precedenti ha esito negativo, il filtro di origine deve tornare al passaggio 3 e provare il tipo successivo enumerato dal lettore.
8.  La riproduzione viene avviata. Il lettore ignora i buffer di output dal decodificatore DMO se il tipo di output della connessione è DirectX VA.
9.  Quando **Ipin::D** si verifica la connessione, il filtro di origine chiama **IWMCodecAMVideoAccelerator:: SetAcceleratorInterface** con un **valore null**. Questa operazione interrompe la connessione di DirectX VA tra il codec e il renderer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> </dl>

 

 




