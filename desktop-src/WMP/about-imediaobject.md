---
title: Informazioni su IMediaObject
description: Informazioni su IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- Plug-in DSP, interfacce
- interfacce, plug-in DSP
- Plug-in di Windows Media Player, interfaccia IMediaObject
- plug-in, interfaccia IMediaObject
- plug-in per l'elaborazione di segnali digitali, interfaccia IMediaObject
- Plug-in DSP, interfaccia IMediaObject
- Interfaccia IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708047"
---
# <a name="about-imediaobject"></a>Informazioni su IMediaObject

L'interfaccia **IMediaObject** è l'interfaccia necessaria per DMOS. **IMediaObject** contiene i metodi usati da un plug-in di Windows Media Player DSP per recuperare i dati da Windows Media Player, per elaborare i dati e per restituire i dati elaborati a Windows Media Player. Per la documentazione completa dell'interfaccia **IMediaObject** , vedere la sezione relativa a DirectShow del Windows SDK.

I metodi di **IMediaObject** possono essere categorizzati come segue:

## <a name="methods-that-handle-format-negotiation"></a>Metodi che gestiscono la negoziazione del formato

Questi sono i metodi che Windows Media Player chiama per ottenere informazioni sui formati di dati supportati dal plug-in. Questi metodi includono:

-   **GetInputMaxLatency**
-   **GetInputSizeInfo**
-   **GetInputStreamInfo**
-   **GetInputType**
-   **GetOutputSizeInfo**
-   **GetOutputStreamInfo**
-   **GetOutputType**
-   **GetStreamCount**
-   **SetInputMaxLatency**
-   **SetInputType**
-   **SetOutputType**

Molti di questi metodi, ad esempio **GetInputType** e **SetInputType**, usano la struttura del **\_ \_ tipo di supporto DMO** per descrivere il formato dei dati usati da un flusso. Quando Windows Media Player chiama questi metodi, fornisce un puntatore a una struttura **del \_ \_ tipo di supporto DMO** . Se un metodo come **SetInputType** specifica le informazioni sul tipo di supporto, il plug-in deve copiare la struttura del **\_ \_ tipo di supporto DMO** in una variabile membro ed esaminare i relativi membri dati per determinare il tipo di dati che Windows Media Player fornirà nel buffer di input. Se un metodo come **GetInputType** recupera le informazioni sul tipo di supporto, il plug-in deve copiare l'indirizzo della variabile membro contenente la struttura del **\_ \_ tipo di supporto DMO** nel puntatore fornito da Windows Media Player nell'elenco dei parametri.

Windows Media Player utilizza principalmente due membri della struttura **del \_ \_ tipo di supporto DMO** :

-   **majortype**: identificatore univoco globale (Guid) che specifica la categoria complessiva del supporto, ad esempio audio o video.
-   **sottotipo**: GUID che specifica una descrizione più dettagliata del supporto, ad esempio audio PCM.

Questi GUID sono disponibili nell'intestazione denominata UUIDs. h, inclusa nel Windows SDK.

I metodi come **GetInputSizeInfo** forniscono informazioni a Windows Media Player sulla quantità di memoria necessaria per allocare i buffer di elaborazione. I metodi come **GetStreamCount** e **GetOutputStreamInfo** forniscono informazioni a Windows Media Player sul numero e sul carattere dei flussi supportati dal plug-in DSP.

**GetInputMaxLatency** e **SetInputMaxLatency** sono implementati da DMOS in casi speciali. I plug-in di Windows Media Player DSP devono restituire E \_ NOTIMPL.

## <a name="methods-that-specify-or-retrieve-state-information"></a>Metodi che specificano o recuperano informazioni sullo stato

Questi sono i metodi che Windows Media Player chiama per ottenere o impostare i valori correlati allo stato corrente del plug-in. Questi metodi includono:

-   **GetInputCurrentType**
-   **GetInputStatus**
-   **GetOutputCurrentType**

**GetInputCurrentType** e **GetOutputCurrentType** usano la struttura del **\_ \_ tipo di supporto DMO** per restituire informazioni a Windows Media Player sui tipi di supporto impostati in precedenza per i flussi di input e di output. **GetInputStatus** restituisce un flag che indica a Windows Media Player se il plug-in DSP può accettare i dati di input.

## <a name="methods-that-handle-buffering-and-processing-data"></a>Metodi che gestiscono il buffering e l'elaborazione dei dati

Questi sono i metodi che Windows Media Player chiama per avviare i vari processi eseguiti dal plug-in per eseguire l'elaborazione del segnale digitale. Questi metodi includono:

-   **AllocateStreamingResources**
-   **Discontinuità**
-   **Svuotamento**
-   **FreeStreamingResources**
-   **Lock**
-   **ProcessInput**
-   **ProcessOutput**

Windows Media Player chiama **AllocateStreamingResources** e **FreeStreamingResources** per fornire al plug-in DSP la possibilità di configurare o rilasciare eventuali buffer aggiuntivi che il plug-in può richiedere per l'elaborazione interna.

Non è necessario che i plug-in Windows Media Player DSP usino il metodo di **discontinuità** DMO.

Windows Media Player chiama **Flush** per indirizzare il plug-in DSP allo scaricamento di tutti i dati memorizzati nel buffer internamente. Il plug-in deve rilasciare tutti i riferimenti alle interfacce **IMediaBuffer** , cancellare tutti i valori che specificano il timestamp o la lunghezza del campione per il buffer multimediale e reinizializzare gli Stati interni che dipendono dal contenuto dell'esempio multimediale.

Windows Media Player chiama ProcessInput per passare un puntatore a un'interfaccia **IMediaBuffer** al plug-in DSP. Questa interfaccia fornisce l'accesso al buffer di input allocato da Windows Media Player per fornire i dati al plug-in. Windows Media Player successivamente chiama **ProcessOutput** per passare un puntatore a un'interfaccia **IMediaBuffer** che fornisce l'accesso al buffer di output allocato da Windows Media Player per ricevere i dati elaborati dal plug-in DSP.

L'interfaccia **IMediaObject** include un metodo denominato **Lock**. Questo metodo è progettato per acquisire o rilasciare un blocco su DMO per lasciare serializzare DMO durante l'esecuzione di più operazioni. La versione di **IMediaObject:: Lock** nel codice della procedura guidata sostituisce l'implementazione ATL del **blocco**. Poiché Windows Media Player serializza le chiamate effettuate all'interfaccia DMO di un plug-in DSP, l'implementazione del **blocco** restituisce semplicemente S \_ OK. Per informazioni dettagliate su come creare un DMO multithread, vedere la sezione relativa a DirectShow del Windows SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfacce obbligatorie**](required-interfaces.md)
</dt> </dl>

 

 




