---
title: Panoramica delle interfacce di rete
description: Panoramica delle interfacce di rete
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Media Format SDK, interfacce di rete
- Windows Media Format SDK, interfacce
- ASF (Advanced Systems Format), interfacce di rete
- ASF (formato avanzato dei sistemi), interfacce di rete
- ASF (Advanced Systems Format), elenco di interfacce per le funzionalità di rete
- ASF (Advanced Systems Format), elenco di interfacce per le funzionalità di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724132"
---
# <a name="overview-of-networking-interfaces"></a>Panoramica delle interfacce di rete

Le funzionalità di rete di questo SDK sono supportate tramite i metodi delle interfacce seguenti.



| Interfaccia                                                  | Descrizione                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | Ottiene informazioni sui client connessi a un sink di rete.                                                                                       |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | Fornisce un metodo per ottenere informazioni su un client collegato a un sink di rete del writer. Questa interfaccia estende l'interfaccia **IWMClientConnections** . |
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | Fornisce un metodo di callback per acquisire le credenziali utente quando si accede a un sito remoto.                                                                  |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | Fornisce metodi avanzati per l'oggetto Reader.                                                                                                       |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | Estende l'interfaccia **IWMReaderAdvanced2** .                                                                                                         |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | Estende l'interfaccia **IWMReaderAdvanced3** .                                                                                                         |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | Configura le impostazioni di rete nell'oggetto Reader.                                                                                                 |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | Configura impostazioni di rete aggiuntive nell'oggetto Reader. Questa interfaccia estende l'interfaccia **IWMReaderNetworkConfig** .                         |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | Configura l'oggetto sink di rete, utilizzato per scrivere supporti digitali in una rete.                                                                |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | Configura l'oggetto sink di push, usato per distribuire i supporti digitali nei punti di pubblicazione.                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione della funzionalità di rete**](implementing-network-functionality.md)
</dt> </dl>

 

 




