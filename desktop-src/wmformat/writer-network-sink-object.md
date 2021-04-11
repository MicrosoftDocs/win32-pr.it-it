---
title: Oggetto sink di rete writer
description: Oggetto sink di rete writer
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows Media Format SDK, oggetti sink di rete writer
- ASF (Advanced Systems Format), oggetti sink di rete writer
- ASF (formato avanzato dei sistemi), oggetti sink di rete writer
- oggetti, oggetti sink di rete writer
- oggetti sink di rete writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117462"
---
# <a name="writer-network-sink-object"></a>Oggetto sink di rete writer

L'oggetto sink di rete writer viene utilizzato per scrivere supporti digitali in una rete.

L'oggetto sink di rete writer viene creato dalla funzione [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), che imposta un puntatore a un'interfaccia **IWMWriterNetworkSink** . Le altre interfacce dell'oggetto sink di rete del writer possono essere ottenute chiamando il metodo **QueryInterface** .



| Interfaccia                                              | Descrizione                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | Raccoglie informazioni sui client connessi.                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | Recupera informazioni client avanzate.                                                                                                                                                                          |
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | Consente all'applicazione di ottenere i messaggi di stato dall'oggetto.                                                                                                                                                 |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | Apre e chiude le porte, imposta e recupera il numero massimo di client che è in grado di connettersi all'oggetto sink, imposta il protocollo di rete che deve essere utilizzato dall'oggetto writer ed esegue altre funzioni avanzate. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | Alloca memoria, determina se il sink funziona in tempo reale e gestisce diverse funzioni di callback.                                                                                                |



 

L'interfaccia di callback seguente può essere implementata dall'applicazione per tenere traccia dello stato di avanzamento di un oggetto sink di rete del writer.



| Interfaccia                                      | Descrizione                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Trasmissione di dati ASF**](broadcasting-asf-data.md)
</dt> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Utilizzo dei sink di writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




