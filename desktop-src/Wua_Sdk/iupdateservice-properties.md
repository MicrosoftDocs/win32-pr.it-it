---
description: L'interfaccia IUpdateService definisce le proprietà seguenti.
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: Proprietà di IUpdateService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485132"
---
# <a name="iupdateservice-properties"></a>Proprietà di IUpdateService

L'interfaccia [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) definisce le proprietà seguenti.



| Proprietà                                                              | Descrizione                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CanRegisterWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | Ottiene un valore booleano che indica se il servizio può eseguire la registrazione con Aggiornamenti automatici.    |
| [**ContentValidationCert**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | Ottiene un hash SHA-1 del certificato utilizzato per firmare il contenuto del servizio.         |
| [**ExpirationDate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | Ottiene la data di scadenza del file CAB di autorizzazione.                                  |
| [**IsManaged**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | Ottiene un valore booleano che indica se un servizio è un servizio gestito.                     |
| [**IsRegisteredWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | Ottiene un valore booleano che indica se un servizio è registrato con Aggiornamenti automatici.     |
| [**IsScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | Ottiene un valore booleano che indica se un servizio è basato su un pacchetto di analisi.               |
| [**IssueDate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | Ottiene la data in cui è stato emesso il file CAB di autorizzazione.                               |
| [**Nome**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | Ottiene il nome del servizio.                                                                   |
| [**OffersWindowsUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | Ottiene un valore booleano che indica se il servizio corrente offre aggiornamenti da aggiornamenti di Windows. |
| [**RedirectUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | Ottiene l'URL per il file CAB del redirector.                                                   |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | Ottiene l'identificatore per un servizio.                                                              |
| [**ServiceUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | Ottiene l'URL per il servizio.                                                                   |
| [**SetupPrefix**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | Ottiene il prefisso per i file di installazione.                                                            |



 

 

 



