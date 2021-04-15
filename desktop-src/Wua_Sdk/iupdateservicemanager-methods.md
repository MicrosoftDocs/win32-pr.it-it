---
description: L'interfaccia IUpdateServiceManager definisce i metodi seguenti.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Metodi IUpdateServiceManager
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464b0b6e48d074dbc43f370f267fe7a526e8269b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525086"
---
# <a name="iupdateservicemanager-methods"></a>Metodi IUpdateServiceManager

L'interfaccia [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) definisce i metodi seguenti.



| Metodo                                                                           | Descrizione                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | Registra un pacchetto di analisi come servizio con Windows Update Agent (WUA) e quindi restituisce un'interfaccia [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) .    |
| [**AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | Registra un servizio con WUA.                                                                                                                    |
| [**RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | Registra un servizio con Aggiornamenti automatici.                                                                                                      |
| [**RemoveService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | Rimuove una registrazione del servizio da WUA.                                                                                                         |
| [**SetOption**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | Imposta le opzioni per l'oggetto che specifica l'ID del servizio e indica se visualizzare un avviso quando si modifica la registrazione del Aggiornamenti automatici. |
| [**UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | Annulla la registrazione di un servizio con Aggiornamenti automatici.                                                                                                    |



 

 

 



