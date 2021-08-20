---
title: Uso di sink personalizzati
description: Uso di sink personalizzati
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- Advanced Systems Format (ASF), sink personalizzati
- ASF (Advanced Systems Format), sink personalizzati
- Advanced Systems Format (ASF), sink
- ASF (Advanced Systems Format), sink
- sink, sink personalizzati
- sink personalizzati, informazioni
- sink writer, sink personalizzati
- sink personalizzati,interfaccia IWMWriterSink
- IWMWriterSink
- sink writer,interfaccia IWMWriterSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95733581e9599c22a81fa6750f3f9cacfd51a6f8a807888815db3778eb913a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118028515"
---
# <a name="using-custom-sinks"></a>Uso di sink personalizzati

Se si ha una particolare necessità di scrittura, è possibile creare sink di writer personalizzati. Il writer mantiene la comunicazione unidirezionale con un sink effettuando chiamate ai metodi di [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink). Per creare un sink personalizzato, implementare **l'interfaccia IWMWriterSink** in una classe nell'applicazione. Questo processo è molto simile all'implementazione di qualsiasi altra interfaccia di callback usata dagli oggetti di Windows Media Format SDK. Per altre informazioni sui callback, vedere [Uso dei metodi di callback](using-the-callback-methods.md).

Il buffer ricevuto in [**IWMWriterSink::OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) deve essere scritto all'inizio del file e tutti i buffer ricevuti in [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) devono essere scritti in sequenza. **OnHeader** verrà chiamato all'inizio, ma potrebbe essere chiamato anche in altri momenti e, se possibile, sovrascrivere l'intestazione originale. Se l'applicazione non è in grado di eseguire questa operazione per qualche motivo, ignorare semplicemente le chiamate **OnHeader** successive.

Il sink personalizzato deve comunicare lo stato all'applicazione di scrittura effettuando chiamate al metodo di callback [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Se si implementa il sink come oggetto COM, è possibile esporre [**l'interfaccia IWMRegisterCallback.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) Tuttavia, è possibile passare l'indirizzo del callback **OnStatus** al sink e impostare un contesto nel modo che si desidera.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei sink del writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




