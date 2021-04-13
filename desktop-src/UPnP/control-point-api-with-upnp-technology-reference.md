---
title: Riferimento all'API del punto di controllo
description: Le interfacce seguenti fanno parte dell'API del punto di controllo con la tecnologia UPnP. L'API del punto di controllo supporta Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic e C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691a0d764f612d957ac11b3b052859f081bc7285
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329311"
---
# <a name="control-point-api-reference"></a>Riferimento all'API del punto di controllo

Le interfacce seguenti fanno parte dell'API del punto di controllo con la tecnologia UPnP. L'API del punto di controllo supporta Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic e C++.



| Interfaccia                                                                                      | Descrizione                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPAddressFamilyControl**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | Consente a un'applicazione di accedere al flag della famiglia di indirizzi dell'oggetto Finder del dispositivo.                                                                                                                                          |
| [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | Consente a un'applicazione di caricare una descrizione del dispositivo. Questa interfaccia è sicura per lo scripting.                                                                                                                                     |
| [**IUPnPDescriptionDocumentCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | Consente a un'applicazione di ricevere i risultati di un'operazione di caricamento asincrona.                                                                                                                                               |
| [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | Consente a un'applicazione di recuperare informazioni su un dispositivo specifico.                                                                                                                                                        |
| [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | Consente a un'applicazione di ottenere l'URL di un documento di descrizione del dispositivo.                                                                                                                                                     |
| [**IUPnPDeviceDocumentAccessEx**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | Fornisce un metodo per ottenere l'intero documento di descrizione del dispositivo XML per un dispositivo specifico.                                                                                                                                  |
| [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | Consente a un'applicazione di trovare un dispositivo.                                                                                                                                                                                       |
| [**IUPnPDeviceFinderAddCallbackWithInterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | Consente a un'applicazione di ricevere i risultati della ricerca asincrona dal framework UPnP insieme al GUID della scheda di rete attraverso cui è arrivato l'annuncio del dispositivo.                                                  |
| [**IUPnPDeviceFinderCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | Consente a un'applicazione di ricevere i risultati della ricerca asincrona dal framework UPnP.                                                                                                                                         |
| [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | Enumera una raccolta di dispositivi.                                                                                                                                                                                            |
| [**IUPnPHttpHeaderControl**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | Consente a un'applicazione di impostare le intestazioni HTTP "agente utente" dalle istanze della classe che implementano le interfacce [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) o [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . |
| [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | Consente a un'applicazione di recuperare le informazioni sullo stato e richiamare le azioni per un servizio.                                                                                                                                         |
| [**IUPnPServiceAsync**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | Eseguire query in modo asincrono sulle variabili di stato e richiamare le azioni su un'istanza di un servizio.                                                                                                                                           |
| [**IUPnPServiceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | Consente a un'applicazione di ricevere notifiche dal framework UPnP quando si verificano gli eventi.                                                                                                                                      |
| [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | Enumera una raccolta di servizi.                                                                                                                                                                                           |



 

 

 




