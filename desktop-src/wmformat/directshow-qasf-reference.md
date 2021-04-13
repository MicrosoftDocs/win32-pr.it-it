---
title: Informazioni di riferimento su DirectShow QASF
description: Informazioni di riferimento su DirectShow QASF
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows Media Format SDK, QASF
- Windows Media Format SDK, DirectShow
- DirectShow, riferimento QASF
- Filtri QASF, riferimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399344"
---
# <a name="directshow-qasf-reference"></a>Informazioni di riferimento su DirectShow QASF

Questa sezione contiene i riferimenti di programmazione per i filtri, le interfacce e le enumerazioni di DirectShow QASF seguenti. La documentazione di DirectShow SDK contiene i materiali di riferimento e guida alla programmazione per interfacce generiche aggiuntive esposte da questi filtri, ad esempio **IBaseFilter** e **Ipin**, e per le versioni precedenti dei componenti qasf.

Per una spiegazione del nome del QASF, vedere [informazioni su DirectShow](about-directshow.md).

Con i componenti di QASF DirectShow sono inclusi i filtri seguenti.



| Filtra                                           | Descrizione                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [Filtro di lettura ASF WM](wm-asf-reader-filter.md) | Legge e analizza i file ASF locali o remoti.                      |
| [Filtro writer ASF WM](wm-asf-writer-filter.md) | Crea file ASF da flussi di input compressi o non compressi. |



 

Le interfacce seguenti sono definite per l'uso con i componenti DirectShow QASF.



| Interfaccia                                                  | Descrizione                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | Fornisce un metodo che consente alle applicazioni di eseguire la registrazione per i callback dai pin di input del [writer ASF WM](wm-asf-writer-filter.md) o dei pin di output del filtro [WM ASF Reader](wm-asf-reader-filter.md) . Usato nell'indicizzazione e quando si aggiungono estensioni di unità dati. |
| [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | Implementato dalle applicazioni e chiamato dai filtri. Le applicazioni usano il metodo One su questa interfaccia per ottenere informazioni sui singoli esempi nel flusso. Usato nell'indicizzazione e quando si aggiungono estensioni di unità dati.                                                 |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))               | Implementato nel writer ASF WM. Utilizzato dalle applicazioni per specificare i profili e i parametri di indicizzazione per il file.                                                                                                                                                              |
| [**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))             | Fornisce funzioni di configurazione aggiuntive sul writer ASF WM.                                                                                                                                                                                                             |



 

L'enumerazione, la struttura e gli eventi seguenti vengono definiti per l'uso con i componenti DirectShow QASF.



| Enumerazione                                                               | Descrizione                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_\_param ASFWRITERCONFIG \_](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) | Definisce i parametri di configurazione del filtro utilizzati nei metodi [**IConfigAsfWriter2:: Getparat**](iconfigasfwriter2-getparam.md) e [**separar**](iconfigasfwriter2-setparam.md) . |



 



| Struttura                                         | Descrizione                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ dati evento WMT \_**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | Contiene informazioni relative a un evento [**di \_ stato WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) e al codice di stato associato restituito da Windows Media Format SDK. |



 



| Event                                           | Descrizione                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [\_evento WMT \_ EC](ec-wmt-event.md)              | Evento inviato da Windows Media Format SDK.                                                              |
| [\_evento di \_ indice \_ WMT EC](ec-wmt-index-event.md) | Inviato quando un'applicazione usa il [writer ASF WM](wm-asf-writer-filter.md) per indicizzare i file di Windows Media video. |



 

 

 