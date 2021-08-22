---
title: Oggetto file sink del writer
description: Oggetto file sink del writer
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows MEDIA Format SDK, oggetti sink di file writer
- Advanced Systems Format (ASF), oggetti sink di file writer
- ASF (Advanced Systems Format), oggetti sink di file writer
- oggetti,oggetti sink di file writer
- oggetti sink di file writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08efb5c404a822b0c30747864bdc01f57cb1a0618eed3f7ad26bd92f158ba625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083645"
---
# <a name="writer-file-sink-object"></a>Oggetto file sink del writer

L'oggetto sink del file writer viene usato durante la scrittura Windows output multimediale in un file.

L'oggetto sink del file writer viene creato dalla funzione [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), che imposta un puntatore a **un'interfaccia IWMWriterFileSink.** Le altre interfacce dell'oggetto sink del file writer possono essere ottenute chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate dall'oggetto sink del file writer.



| Interfaccia                                          | Descrizione                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Consente all'applicazione di ottenere messaggi di stato dall'oggetto .                                                                 |
| [**IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | Apre un file in cui l'oggetto writer può scrivere dati.                                                                         |
| [**IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | Fornisce la gestione estesa di un oggetto sink di file. Eredita tutti i metodi di **IWMWriterFileSink.**                       |
| [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | Fornisce opzioni aggiuntive per la scrittura di file. Eredita tutti i metodi di **IWMWriterFileSink** e **IWMWriterFileSink2.** |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Alloca memoria, determina se il sink funziona in tempo reale e gestisce diverse funzioni di callback.                |



 

L'interfaccia di callback seguente deve essere implementata dall'applicazione per tenere traccia dello stato di avanzamento di un oggetto sink del file writer.



| Interfaccia                                      | Descrizione                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Uso dei sink del writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




