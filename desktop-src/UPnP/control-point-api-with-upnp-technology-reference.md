---
title: Informazioni di riferimento sulle API del punto di controllo
description: Le interfacce seguenti fanno parte dell'API Punto di controllo con tecnologia UPnP. L'API Punto di controllo supporta Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic e C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b3dab16874ebeb7b43ef1e8cf28def13d3ef1d7169a5aae4836b39da66636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058119"
---
# <a name="control-point-api-reference"></a>Informazioni di riferimento sulle API del punto di controllo

Le interfacce seguenti fanno parte dell'API Punto di controllo con tecnologia UPnP. L'API Punto di controllo supporta Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic e C++.



| Interfaccia                                                                                      | Descrizione                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPAddressFamilyControl**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | Consente a un'applicazione di accedere al flag della famiglia di indirizzi dell'oggetto Device Finder.                                                                                                                                          |
| [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | Consente a un'applicazione di caricare una descrizione del dispositivo. Questa interfaccia è sicura per gli script.                                                                                                                                     |
| [**IUPnPDescriptionDocumentCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | Consente a un'applicazione di ricevere i risultati di un'operazione di caricamento asincrona.                                                                                                                                               |
| [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | Consente a un'applicazione di recuperare informazioni su un dispositivo specifico.                                                                                                                                                        |
| [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | Consente a un'applicazione di ottenere l'URL di un documento di descrizione del dispositivo.                                                                                                                                                     |
| [**IUPnPDeviceDocumentAccessEx**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | Fornisce un metodo per ottenere l'intero documento di descrizione del dispositivo XML per un dispositivo specifico.                                                                                                                                  |
| [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | Consente a un'applicazione di trovare un dispositivo.                                                                                                                                                                                       |
| [**IUPnPDeviceFinderAddCallbackWithInterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | Consente a un'applicazione di ricevere risultati di ricerca asincroni dal framework UPnP insieme al GUID della scheda di rete tramite cui è stato visualizzato l'annuncio del dispositivo.                                                  |
| [**IUPnPDeviceFinderCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | Consente a un'applicazione di ricevere risultati di ricerca asincroni dal framework UPnP.                                                                                                                                         |
| [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | Enumera una raccolta di dispositivi.                                                                                                                                                                                            |
| [**IUPnPHttpHeaderControl**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | Consente a un'applicazione di impostare le intestazioni HTTP "User Agent" dalle istanze della classe che implementano le interfacce [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) o [**IUPnPDescriptionDocument.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) |
| [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | Consente a un'applicazione di recuperare informazioni sullo stato e richiamare azioni per un servizio.                                                                                                                                         |
| [**IUPnPServiceAsync**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | Eseguire una query asincrona sulle variabili di stato e richiamare azioni su un'istanza di un servizio.                                                                                                                                           |
| [**IUPnPServiceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | Consente a un'applicazione di ricevere notifiche dal framework UPnP quando si verificano eventi.                                                                                                                                      |
| [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | Enumera una raccolta di servizi.                                                                                                                                                                                           |



 

 

 




