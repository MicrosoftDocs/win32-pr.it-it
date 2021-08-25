---
title: Abilitazione dell'accelerazione video DirectX
description: Abilitazione dell'accelerazione video DirectX
ms.assetid: 5cb2f564-88e3-4b60-bde3-6ccf69c97c48
keywords:
- Windows Media Format SDK, abilitazione di DXVA
- Windows Media Format SDK,DirectX Video Acceleration (DXVA)
- Windows MEDIA Format SDK, accelerazione video
- Advanced Systems Format (ASF), abilitazione di DXVA
- ASF (Advanced Systems Format), abilitazione di DXVA
- Advanced Systems Format (ASF), DirectX Video Acceleration (DXVA)
- ASF (Advanced Systems Format),DirectX Video Acceleration (DXVA)
- Advanced Systems Format (ASF), accelerazione video
- ASF (Advanced Systems Format), accelerazione video
- Accelerazione video DirectX (DXVA), abilitazione
- DXVA (Accelerazione video DirectX), abilitazione
- Accelerazione video DirectX (DXVA), ordine delle operazioni
- DXVA (Accelerazione video DirectX), ordine delle operazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840549c9a148fdfe8cc67daf46645ffb0925369057fe71f0c17217bfd36823ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930761"
---
# <a name="enabling-directx-video-acceleration"></a>Abilitazione dell'accelerazione video DirectX

Questa sezione descrive come abilitare l'accelerazione video microsoft® DirectX® durante la riproduzione di contenuti trasmessi in streaming in un lettore personalizzato.

## <a name="background"></a>Sfondo

DirectX Video Acceleration (DirectX VA) è una specifica API per l'accelerazione hardware delle operazioni di decodifica 2D. Consente ai decodificatori software di eseguire l'offload di determinate operazioni a elevato utilizzo di CPU nella scheda grafica per l'elaborazione. Per gli utenti finali, ciò rende possibile la riproduzione di video a velocità in bit elevata, ad esempio la riproduzione di DVD a schermo intero in computer meno recenti dotati di schede grafiche compatibili con DirectX VA.

A partire da Windows Media Format 9 Series SDK, il filtro wrapper DMO supporta DirectX VA. Ciò significa che, per la riproduzione locale, le applicazioni possono usare il filtro lettore AS Windows F WM per riprodurre contenuto basato su supporti e l'accelerazione hardware DirectX VA verrà richiamata automaticamente se la scheda grafica lo supporta. Tuttavia, il filtro WM ASF Reader non supporta la riproduzione del contenuto trasmesso in streaming. Pertanto, se si vuole supportare DirectX VA durante la riproduzione di contenuto in streaming in un lettore personalizzato, è necessario usare un meccanismo alternativo, ovvero quello usato da Windows Media Player a partire da Windows Media 9 Series.

Poiché Windows Media Player è stato progettato prima dello sviluppo dei filtri QASF, Windows Media Player ha un proprio filtro di origine, basato su Windows Media Format SDK, per la riproduzione di contenuti basati su Windows Media. Il filtro Windows sorgente multimediale WMP recapita i dati decompressi a valle direttamente ai renderer audio e video. Al contrario, WM ASF Reader recapita il contenuto compresso a valle agli oggetti multimediali DirectX Media Objects (DMO) del decodificatore multimediale Windows, ospitati all'interno del wrapper DMO. I diagrammi seguenti illustrano le differenze tra WM ASF Reader e WMP Windows Media Source Filter.

![il filtro di origine personalizzato restituisce esempi non compressi](images/wmp-dxva-graph.png)

![qasf source filter outputs compressed samples (Esempi compressi del filtro di origine qasf)](images/qasf-dxva-graph.png)

Per abilitare DirectX VA per il contenuto trasmesso in streaming, è necessario creare un filtro di origine personalizzato come quello nel diagramma superiore. Fondamentalmente, questo filtro userà Windows Media Format SDK per creare un'istanza di un oggetto lettore WM, decomprimere gli esempi e inviarli a valle sui pin di output. Questa discussione presuppone che il filtro di origine sia già stato creato e che sia ora possibile implementare il supporto directx va.

Per abilitare DirectX VA, l'attività di base del filtro di origine è fornire al renderer video e al DMO del decodificatore WMV le interfacce necessarie per negoziare la connessione DirectX VA. Il filtro di origine non partecipa a tali negoziazioni. Dopo l'avvio dello streaming, l'unica attività correlata a DirectX VA che il filtro di origine può eseguire è quella di modificare i timestamp sugli esempi video prima che il decodificatore WMV li consegnerà al renderer video. Il motivo principale per questa operazione è fornire un controllo della sequenza temporale personalizzato oltre a ciò che le interfacce DirectShow® standard.

Sono definite tre interfacce per consentire le comunicazioni necessarie tra Windows Media Format SDK, il filtro di origine del lettore, il decodificatore video multimediale Windows DMO e il renderer di sovrapposizione Mixer o di combinazione video. Queste interfacce sono descritte nella tabella seguente.



| Interfaccia                                                        | Descrizione                                                                                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecAMVideoAccelerator**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator) | Esposto dal Windows Media Decoder DMO e chiamato dal filtro di origine di un lettore multimediale per configurare le varie connessioni necessarie per abilitare DirectX VA per la Windows contenuto video multimediale. |
| [**IWMPlayerTimestampHook**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook)         | Implementato nel filtro di origine del lettore. Consente al filtro di modificare i timestamp degli esempi video prima di recapitarli a valle.                                                 |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)             | Implementato nell'oggetto lettore WM. Viene chiamato da un filtro di origine del lettore per ottenere le interfacce dal DMO.                                                                             |



 

## <a name="order-of-operations-in-directx-vaenabled-playback"></a>Ordine delle operazioni nella riproduzione abilitata per DirectX VA

Questa sezione descrive l'ordine generale delle operazioni in fase di esecuzione per un lettore abilitato per DirectX VA e il relativo filtro di origine. I componenti a cui si fa riferimento in questa sezione sono:

-   Lettore multimediale di terze parti, detto lettore.
-   Filtro di origine personalizzato, di cui viene creata un'istanza dal lettore, che usa Windows Media Format SDK per decomprimere Windows contenuto basato su supporti.
-   Il pin di output video del filtro di origine del lettore, detto pin di output.
-   Il DirectShow del filtro di riproduzione video, detto grafico.
-   Renderer di combinazione video, detto VMR.
-   Oggetto Windows lettore asincrono di Media Format SDK, detto lettore.
-   Oggetto Windows Media Video Decoder DirectX Media Object, detto DMO.

L'ordine delle operazioni è il seguente:

1.  Il lettore crea un'istanza del filtro di origine e di un oggetto lettore. Il lettore crea un decodificatore video DMO e imposta il tipo di input (compresso). Questo problema deve verificarsi prima che il lettore tenti di configurare il grafico di riproduzione video perché l'SDK e il DMO del decodificatore devono essere coinvolti nel processo di negoziazione con il grafo e il DMO deve conoscere il formato di input durante il passaggio 9.
2.  Il lettore chiama **IGraphBuilder::Render,** specificando il pin di output del filtro di origine video. A questo punto, il DirectShow del grafico del filtro cerca di connettere il vmr al filtro di origine video del lettore.
3.  Il gestore del grafico filtri chiama **IPin::Connessione** sul pin di output del filtro di origine video del lettore.

I passaggi da 4 a 10 si verificano all'interno di **IPin::Connessione**.

1.  Il filtro di origine ottiene l'interfaccia **IWMCodecAMVideoAccelerator** dal metodo **IWMReaderAccelerator::GetCodecInterface del** lettore. Se il codec non supporta DirectX VA, la chiamata a **GetCodecInterface** potrebbe non riuscire. In questo caso, la negoziazione procede come di consueto, senza il supporto di DirectX VA.
2.  Il filtro di origine passa il **puntatore IAMVideoAccelerator** dal pin passato **nel Connessione** al DMO del decodificatore tramite **IWMCodecAMVideoAccelerator::SetAcceleratorInterface**.
3.  Il filtro di origine delega quindi il resto **dell'operazione IPin::Connessione** al metodo **CBaseOutputPin::Connessione.** L'enumerazione del formato con l'SDK procede come oggi. Se il codec supporta DirectX VA per il contenuto connesso, il codec DMO presenta prima questi sottotipi directx va, prima dei tipi YUV e RGB supportati. Se è disponibile il supporto directx va, i passaggi da 7 a 11 vengono tentati nel contesto di un sottotipo DirectX VA. Il frammento di codice seguente illustra come identificare un sottotipo di supporto DirectX VA.
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

    

4.  L'implementazione di **CBaseOutputPin::Connessione** **chiama IPin::CompleteConnect** durante il passaggio 3. Se si considera un sottotipo directx va, viene tentata la negoziazione DirectX VA. Il pin di output chiama **IWMCodecAMVideoAccelerator::NegotiateConnection,** passando il tipo di supporto di output corrente.
5.  Il decodificatore DMO la negoziazione necessaria con il vmr tramite **l'interfaccia IAMVideoAccelerator** e restituisce il GUID del sottotipo video su cui i due hanno concordato. Il pin di output delega tutte le chiamate **IAMVideoAcceleratorNotify** ricevute durante questo processo all'interfaccia **IAMVideoAcceleratorNotify** del decodificatore DMO, che può essere ottenuta anche tramite il metodo **IWMReaderAccelerator::GetCodecInterface.**
6.  Se **NegotiateConnection** ha esito positivo, il pin di output chiama **IWMCodecAMVideoAccelerator::SetPlayerNotify** con **un'interfaccia IWMPlayerTimestampHook.** Questo hook consente al filtro di origine di aggiornare i timestamp sugli esempi prima che siano consegnati al renderer.
7.  Il filtro di origine chiama **IWMReaderAccelerator::Notify** con il tipo di supporto negoziato. Ciò consente al lettore di aggiornare le variabili interne ed eseguire il commit in DirectX VA. Questa è l'ultima posizione in cui il codec o il lettore può avere esito negativo. Se uno dei passaggi precedenti ha esito negativo, il filtro di origine deve tornare al passaggio 3 e provare il tipo successivo enumerato dal lettore.
8.  Viene avviata la riproduzione. Il lettore ignora i buffer di output dal decodificatore DMO se il tipo di output della connessione è DirectX VA.
9.  Quando **si verifica IPin::D isconnect,** il filtro di origine chiama **IWMCodecAMVideoAccelerator::SetAcceleratorInterface** con **null.** Ciò interrompe la connessione DirectX VA tra il codec e il renderer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> </dl>

 

 




