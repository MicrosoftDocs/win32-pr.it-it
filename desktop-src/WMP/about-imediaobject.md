---
title: Informazioni su IMediaObject
description: Informazioni su IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Windows Media Player plug-in, interfacce
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- plug-in DSP, interfacce
- interfacce, plug-in DSP
- Windows Media Player plug-in, interfaccia IMediaObject
- plug-in, interfaccia IMediaObject
- plug-in di elaborazione dei segnali digitali, interfaccia IMediaObject
- Plug-in DSP, interfaccia IMediaObject
- Interfaccia IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dbf44a527d61d924045a4bcceded5d90bb174fef608e3b7667338e99aa1efe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583908"
---
# <a name="about-imediaobject"></a>Informazioni su IMediaObject

**L'interfaccia IMediaObject** è l'interfaccia necessaria per gli oggetti DMO. **IMediaObject** contiene i metodi utilizzati da un plug-in DSP Windows Media Player per ottenere dati da Windows Media Player, per elaborare i dati e per restituire i dati elaborati Windows Media Player. Per la documentazione completa **dell'interfaccia IMediaObject,** vedere la sezione DirectShow di Windows SDK.

I metodi di **IMediaObject** possono essere classificati come segue:

## <a name="methods-that-handle-format-negotiation"></a>Metodi che gestiscono la negoziazione del formato

Questi sono i metodi Windows Media Player chiamate per ottenere informazioni sui formati di dati supportati dal plug-in. Questi metodi includono:

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

Molti di questi metodi, ad esempio **GetInputType** e **SetInputType,** usano la **struttura MEDIA \_ \_ TYPE DMO** per descrivere il formato dei dati usati da un flusso. Quando Windows Media Player chiama questi metodi, fornisce un puntatore a una **DMO \_ MEDIA \_ TYPE.** Se un metodo come **SetInputType** specifica le informazioni sul tipo di supporto, il plug-in deve copiare la struttura **DMO MEDIA \_ \_ TYPE in** una variabile membro ed esaminare i relativi membri dati per determinare il tipo di dati che Windows Media Player fornirà nel buffer di input. Se un metodo come **GetInputType** recupera le informazioni sul tipo di supporto, il plug-in deve copiare l'indirizzo della variabile membro contenente la struttura **MEDIA \_ \_ TYPE di DMO** nel puntatore fornito da Windows Media Player nell'elenco di parametri.

Windows Media Player usa principalmente due membri della **DMO \_ MEDIA \_ TYPE:**

-   **majortype:** identificatore univoco globale (GUID) che specifica la categoria complessiva dei supporti, ad esempio audio o video.
-   **subtype**: GUID che specifica una descrizione più dettagliata del supporto, ad esempio l'audio PCM.

Questi GUID sono disponibili nell'intestazione denominata uuids.h, inclusa in Windows SDK.

Metodi come **GetInputSizeInfo** forniscono informazioni Windows Media Player sulla quantità di memoria necessaria per allocare i buffer di elaborazione. Metodi come **GetStreamCount** e **GetOutputStreamInfo** forniscono informazioni Windows Media Player sul numero e sul carattere dei flussi supportati dal plug-in DSP.

**GetInputMaxLatency e** **SetInputMaxLatency** vengono implementati da DMO in casi speciali. Windows Media Player I plug-in DSP devono restituire \_ NOTIMPL E.

## <a name="methods-that-specify-or-retrieve-state-information"></a>Metodi che specificano o recuperano informazioni sullo stato

Questi sono i metodi che Windows Media Player chiamate per ottenere o impostare valori correlati allo stato corrente del plug-in. Questi metodi includono:

-   **GetInputCurrentType**
-   **GetInputStatus**
-   **GetOutputCurrentType**

**GetInputCurrentType** e **GetOutputCurrentType** usano la struttura **MEDIA \_ \_ TYPE** DMO per restituire informazioni Windows Media Player sui tipi di supporti impostati in precedenza per i flussi di input e output. **GetInputStatus** restituisce un flag che indica Windows Media Player se il plug-in DSP può accettare dati di input.

## <a name="methods-that-handle-buffering-and-processing-data"></a>Metodi che gestiscono la memorizzazione nel buffer e l'elaborazione dei dati

Questi sono i metodi che Windows Media Player per avviare i vari processi eseguono il plug-in per eseguire l'elaborazione del segnale digitale. Questi metodi includono:

-   **AllocateStreamingResources**
-   **Discontinuità**
-   **Svuotamento**
-   **FreeStreamingResources**
-   **Lock**
-   **ProcessInput**
-   **ProcessOutput**

Windows Media Player chiama **AllocateStreamingResources** e **FreeStreamingResources** per fornire al plug-in DSP la possibilità di configurare o rilasciare eventuali buffer aggiuntivi che il plug-in potrebbe richiedere per l'elaborazione interna.

Windows Media Player Non è necessario che i plug-in DSP usino DMO **metodo Discontinuity.**

Windows Media Player chiama **Flush per** indirizzare il plug-in DSP in modo da scaricare tutti i dati memorizzati nel buffer interno. Il plug-in deve rilasciare tutti i riferimenti alle interfacce **IMediaBuffer,** cancellare tutti i valori che specificano il timestamp o la lunghezza del campione per il buffer multimediale e reinizializzare gli stati interni che dipendono dal contenuto del campione multimediale.

Windows Media Player chiama ProcessInput per passare un puntatore a **un'interfaccia IMediaBuffer** al plug-in DSP. Questa interfaccia fornisce l'accesso al buffer di input allocato Windows Media Player per fornire dati al plug-in. Windows Media Player successivamente chiama **ProcessOutput** per passare un puntatore a un'interfaccia **IMediaBuffer** che fornisce l'accesso al buffer di output allocato da Windows Media Player per ricevere i dati elaborati dal plug-in DSP.

**L'interfaccia IMediaObject** include un metodo denominato **Lock**. Questo metodo è progettato per acquisire o rilasciare un blocco sul DMO per mantenere la DMO serializzata quando si eseguono più operazioni. La versione di **IMediaObject::Lock nel** codice della procedura guidata esegue l'override dell'implementazione ATL di **Lock.** Poiché Windows Media Player serializza le chiamate effettuate all'interfaccia DMO di un plug-in DSP, l'implementazione di **Lock** restituisce semplicemente S \_ OK. Per informazioni dettagliate su come creare un DMO multithreading, vedere la sezione DirectShow dell'SDK Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfacce obbligatorie**](required-interfaces.md)
</dt> </dl>

 

 




