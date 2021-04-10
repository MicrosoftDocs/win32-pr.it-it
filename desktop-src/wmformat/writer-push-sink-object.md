---
title: Oggetto sink push writer
description: Oggetto sink push writer
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows Media Format SDK, oggetti sink push writer
- ASF (Advanced Systems Format), oggetti sink push writer
- ASF (Advanced Systems Format), oggetti sink push writer
- oggetti, oggetti sink push writer
- oggetti sink push writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956181"
---
# <a name="writer-push-sink-object"></a>Oggetto sink push writer

L'oggetto sink push writer distribuisce i supporti digitali ai punti di pubblicazione. Ad esempio, un concerto Live può essere codificato da un singolo server e quindi recapitato, o *push*, a diversi altri server che eseguiranno effettivamente lo streaming del contenuto agli utenti.

Un oggetto sink push writer viene creato dalla funzione [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), che imposta un puntatore a un'interfaccia **IWMWriterPushSink** . Le altre interfacce supportate dall'oggetto, elencate nella tabella seguente, possono essere ottenute chiamando il metodo **QueryInterface** .



| Interfaccia                                          | Descrizione                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Consente all'applicazione di ottenere i messaggi di stato dall'oggetto.                                                  |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | Gestisce una sessione di distribuzione push.                                                                             |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Alloca memoria, determina se il sink funziona in tempo reale ed espone diverse funzioni di callback. |



 

L'interfaccia di callback seguente può essere implementata dall'applicazione per tenere traccia dello stato di avanzamento di un oggetto sink push writer.



| Interfaccia                                      | Descrizione                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Invio di dati ASF a un punto di pubblicazione**](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[**Utilizzo dei sink di writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




