---
title: Oggetto file sink del writer
description: Oggetto file sink del writer
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows Media Format SDK, oggetti sink di file del writer
- ASF (Advanced Systems Format), oggetti sink di file writer
- ASF (Advanced Systems Format), oggetti sink di file writer
- oggetti, oggetti sink di file writer
- oggetti sink di file writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046442"
---
# <a name="writer-file-sink-object"></a>Oggetto file sink del writer

L'oggetto sink di file del writer viene usato durante la scrittura dell'output di Windows Media in un file.

L'oggetto sink di file del writer viene creato dalla funzione [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), che imposta un puntatore a un'interfaccia **IWMWriterFileSink** . Le altre interfacce dell'oggetto sink di file del writer possono essere ottenute chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate dall'oggetto sink di file del writer.



| Interfaccia                                          | Descrizione                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Consente all'applicazione di ottenere i messaggi di stato dall'oggetto.                                                                 |
| [**IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | Apre un file in cui l'oggetto writer può scrivere i dati.                                                                         |
| [**IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | Fornisce la gestione estesa di un oggetto sink di file. Eredita tutti i metodi di **IWMWriterFileSink**.                       |
| [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | Fornisce opzioni aggiuntive per la scrittura di file. Eredita tutti i metodi di **IWMWriterFileSink** e **IWMWriterFileSink2**. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Alloca memoria, determina se il sink funziona in tempo reale e gestisce diverse funzioni di callback.                |



 

L'interfaccia di callback seguente deve essere implementata dall'applicazione per tenere traccia dello stato di avanzamento di un oggetto sink di file del writer.



| Interfaccia                                      | Descrizione                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Utilizzo dei sink di writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




