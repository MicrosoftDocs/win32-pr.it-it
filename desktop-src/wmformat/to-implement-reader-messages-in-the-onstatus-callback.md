---
title: Per implementare i messaggi del lettore nel callback OnStatus
description: Per implementare i messaggi del lettore nel callback OnStatus
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- ASF (Advanced Systems Format), implementazione di messaggi Reader
- ASF (Advanced Systems Format), implementazione di messaggi Reader
- ASF (Advanced Systems Format), callback di OnStatus
- ASF (formato avanzato dei sistemi), callback OnStatus
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Reader asincroni, implementazione di messaggi Reader
- Metodo di callback OnStatus, implementazione dei messaggi del lettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046296"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a>Per implementare i messaggi del lettore nel callback OnStatus

Per utilizzare il Reader asincrono per recapitare contenuto da un file ASF, è necessario implementare almeno due metodi di callback, [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) e [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). In questa sezione viene descritto come implementare **IWMStatusCallback:: OnStatus** per ricevere e rispondere ai messaggi di stato inviati dal lettore. **OnStatus** viene usato da altri oggetti in Windows Media Format SDK. Per informazioni generali su **OnStatus**, vedere [utilizzo del callback OnStatus](using-the-onstatus-callback.md).

Quando si usa il Reader asincrono, è necessario intercettare i messaggi seguenti in **IWMStatusCallback:: OnStatus**.



| Messaggio di stato | Descrizione                                     |
|----------------|-------------------------------------------------|
| WMT \_ aperto    | Inviato al completamento delle operazioni di apertura del file. |
| WMT \_ chiuso    | Inviato al completamento delle operazioni di chiusura del file. |



 

È necessario usare i messaggi di stato elencati sopra per controllare l'esecuzione dell'applicazione di lettura. Ad esempio, è necessario attendere fino a quando non si riceve il messaggio **WMT \_ aperto** per avviare il Reader o chiamare altri metodi che richiedono che il lettore disponga di un file pronto. Spesso, le applicazioni compilate con il Reader asincrono utilizzano un evento per segnalare il completamento delle chiamate asincrone e continuare l'elaborazione. Per altre informazioni sull'uso di eventi per la segnalazione del completamento delle operazioni, vedere [uso di eventi con chiamate asincrone](using-events-with-asynchronous-calls.md).

Molti altri messaggi vengono inviati a **OnStatus** dall'oggetto Reader per consentire all'applicazione di rispondere allo stato delle operazioni di lettura. I valori dei messaggi di stato possibili sono definiti nel tipo di enumerazione [**\_ dello stato WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Uso del callback di OnStatus**](using-the-onstatus-callback.md)
</dt> </dl>

 

 




