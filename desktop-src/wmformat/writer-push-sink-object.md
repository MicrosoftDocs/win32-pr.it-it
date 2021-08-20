---
title: Oggetto sink push writer
description: Oggetto sink push writer
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows MEDIA Format SDK, writer di oggetti sink push
- Advanced Systems Format (ASF), oggetti sink push writer
- ASF (Advanced Systems Format), writer di oggetti sink push
- oggetti,oggetti sink push writer
- oggetti sink push writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859e4d2d5cf2530e655b74705b1d6f9ef93960d28f523c00e0da7a7336ab258d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006331"
---
# <a name="writer-push-sink-object"></a>Oggetto sink push writer

L'oggetto sink push writer distribuisce i supporti digitali ai punti di pubblicazione. Ad esempio, un live concert può essere codificato da un singolo server e quindi recapitato, o *push,* a diversi altri server che effettivamente trasmettere il contenuto agli utenti.

Un oggetto sink push writer viene creato dalla funzione [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), che imposta un puntatore a **un'interfaccia IWMWriterPushSink.** Le altre interfacce supportate dall'oggetto , elencate nella tabella seguente, possono essere ottenute chiamando il **metodo QueryInterface.**



| Interfaccia                                          | Descrizione                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Consente all'applicazione di ottenere messaggi di stato dall'oggetto .                                                  |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | Gestisce una sessione di distribuzione push.                                                                             |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Alloca memoria, determina se il sink funziona in tempo reale ed espone diverse funzioni di callback. |



 

L'interfaccia di callback seguente può essere implementata dall'applicazione per tenere traccia dello stato di avanzamento di un oggetto sink push del writer.



| Interfaccia                                      | Descrizione                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Invio di dati ASF a un punto di pubblicazione**](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[**Uso dei sink del writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




