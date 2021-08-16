---
title: Writer Network Sink Object
description: Writer Network Sink Object
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows MEDIA Format SDK, writer di oggetti sink di rete
- Advanced Systems Format (ASF), writer di oggetti sink di rete
- ASF (Advanced Systems Format), writer di oggetti sink di rete
- oggetti,writer di oggetti sink di rete
- writer di oggetti sink di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2011fd161fc4ac5e1cd03d955f06259e6499e343970cc309b1e8c41db051a32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843726"
---
# <a name="writer-network-sink-object"></a>Writer Network Sink Object

L'oggetto sink di rete writer viene usato per scrivere supporti digitali in una rete.

L'oggetto sink di rete writer viene creato dalla funzione [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), che imposta un puntatore a **un'interfaccia IWMWriterNetworkSink.** Le altre interfacce dell'oggetto sink di rete writer possono essere ottenute chiamando il **metodo QueryInterface.**



| Interfaccia                                              | Descrizione                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | Raccoglie informazioni sui client connessi.                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | Recupera informazioni avanzate sul client.                                                                                                                                                                          |
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | Consente all'applicazione di ottenere messaggi di stato dall'oggetto .                                                                                                                                                 |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | Apre e chiude le porte, imposta e recupera il numero massimo di client che possono connettersi all'oggetto sink, imposta il protocollo di rete che deve essere usato dall'oggetto writer ed esegue altre funzioni avanzate. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | Alloca memoria, determina se il sink funziona in tempo reale e gestisce diverse funzioni di callback.                                                                                                |



 

L'interfaccia di callback seguente può essere implementata dall'applicazione per tenere traccia dello stato di un oggetto sink di rete writer.



| Interfaccia                                      | Descrizione                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Trasmissione di dati ASF**](broadcasting-asf-data.md)
</dt> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Uso dei sink del writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




