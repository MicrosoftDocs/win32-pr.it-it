---
title: Uso di sink personalizzati
description: Uso di sink personalizzati
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- ASF (Advanced Systems Format), sink personalizzati
- ASF (formato avanzato dei sistemi), sink personalizzati
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- sink, sink personalizzati
- sink personalizzati, informazioni
- sink writer, sink personalizzati
- sink personalizzati, interfaccia IWMWriterSink
- IWMWriterSink
- sink writer, interfaccia IWMWriterSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723479"
---
# <a name="using-custom-sinks"></a>Uso di sink personalizzati

Se si ha una speciale necessità di scrittura, è possibile creare sink di writer personalizzati. Il writer gestisce una comunicazione unidirezionale con un sink effettuando chiamate ai metodi di [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink). Per creare un sink personalizzato, implementare l'interfaccia **IWMWriterSink** in una classe nell'applicazione. Questo processo è molto simile all'implementazione di qualsiasi altra interfaccia di callback utilizzata dagli oggetti di Windows Media Format SDK. Per ulteriori informazioni sui callback, vedere [utilizzo dei metodi di callback](using-the-callback-methods.md).

Il buffer ricevuto in [**IWMWriterSink:: Onheader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) deve essere scritto all'inizio del file e tutti i buffer ricevuti in [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) devono essere scritti in sequenza. **Onheader** verrà chiamato all'inizio, ma potrebbe essere chiamato anche in altri momenti. in tal caso, è necessario, se possibile, sovrascrivere l'intestazione originale. Se l'applicazione non è in grado di eseguire questa operazione per qualche motivo, è sufficiente ignorare le chiamate **Onheader** successive.

Il sink personalizzato deve comunicare lo stato all'applicazione di scrittura effettuando chiamate al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback. Se si implementa il sink come oggetto COM, potrebbe essere necessario esporre l'interfaccia [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) . Tuttavia, è possibile passare l'indirizzo del callback **OnStatus** al sink e impostare un contesto nel modo desiderato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo dei sink di writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




