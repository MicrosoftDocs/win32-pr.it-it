---
description: Il riferimento all'API di scripting per WMI descrive ogni oggetto di script usando una sintassi specifica. Per una spiegazione di questa sintassi, vedere convenzioni dei documenti per l'API di scripting.
ms.assetid: 91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26
ms.tgt_platform: multiple
title: Oggetti API di scripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30d3269b137686472f54cdb8cf53720b4aad978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226824"
---
# <a name="scripting-api-objects"></a>Oggetti API di scripting

Il riferimento all'API di scripting per WMI descrive ogni oggetto di script usando una sintassi specifica. Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Nella tabella seguente sono elencati gli oggetti di scripting WMI e il modo in cui vengono utilizzati.



| Oggetto                                               | Descrizione                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)               | Costruisce e analizza i valori [DateTime](date-and-time-format.md) CIM.                                                                                                                                                                                 |
| [**SWbemEventSource**](swbemeventsource.md)         | Recupera gli eventi in combinazione con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).                                                                                                                               |
| [**SWbemLastError**](swbemlasterror.md)             | Fornisce informazioni estese sugli errori quando si verifica un errore.                                                                                                                                                                                              |
| [**SWbemLocator**](swbemlocator.md)                 | Ottiene un oggetto [**SWbemServices**](swbemservices.md) che può ottenere l'accesso a WMI in un determinato computer host.                                                                                                                                     |
| [**SWbemMethod**](swbemmethod.md)                   | Contiene una singola definizione di metodo WMI.                                                                                                                                                                                                               |
| [**SWbemMethodSet**](swbemmethodset.md)             | Ottiene una raccolta di oggetti [**SWbemMethod**](swbemmethod.md) .                                                                                                                                                                                       |
| [**SWbemNamedValue**](swbemnamedvalue.md)           | Contiene un singolo valore denominato.                                                                                                                                                                                                                         |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md)     | Ottiene l'accesso a una raccolta di oggetti [**SWbemNamedValue**](swbemnamedvalue.md) .                                                                                                                                                                     |
| [**SWbemObject**](swbemobject.md)                   | Contiene e modifica una singola classe o istanza di oggetto WMI.                                                                                                                                                                                        |
| [**SWbemObjectEx**](swbemobjectex.md)               | Estende la funzionalità di [**SWbemObject**](swbemobject.md). Questo oggetto aggiunge il metodo [**Refresh**](swbemrefresher-refresh.md) per gli oggetti [**SWbemRefresher**](swbemrefresher.md) .                                                           |
| [**SWbemObjectPath**](swbemobjectpath.md)           | Genera e convalida un percorso dell'oggetto.                                                                                                                                                                                                                |
| [**SWbemObjectSet**](swbemobjectset.md)             | Ottiene l'accesso a una raccolta di oggetti [**SWbemObject**](swbemobject.md) .                                                                                                                                                                             |
| [**SWbemPrivilege**](swbemprivilege.md)             | Imposta o cancella un privilegio.                                                                                                                                                                                                                            |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)       | Ottiene l'accesso a una raccolta di oggetti [**SWbemPrivilege**](swbemprivilege.md) .                                                                                                                                                                       |
| [**SWbemProperty**](swbemproperty.md)               | Contiene una singola proprietà WMI.                                                                                                                                                                                                                        |
| [**SWbemPropertySet**](swbempropertyset.md)         | Ottiene l'accesso a una raccolta di oggetti [**SWbemProperty**](swbemproperty.md) .                                                                                                                                                                         |
| [**Oggetto SWbemQualifier**](swbemqualifier.md)             | Contiene un solo qualificatore di proprietà.                                                                                                                                                                                                                  |
| [**Dell'SWbemQualifierSet**](swbemqualifierset.md)       | Ottiene l'accesso a una raccolta di oggetti [**oggetto SWbemQualifier**](swbemqualifier.md) .                                                                                                                                                                       |
| [**SWbemRefresher**](swbemrefresher.md)             | Raccoglie e aggiorna i valori delle proprietà dell'oggetto in un'unica operazione.                                                                                                                                                                                          |
| [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Rappresenta un singolo elemento aggiornabile in un oggetto [**SWbemRefresher**](swbemrefresher.md) , ad esempio una proprietà.                                                                                                                                     |
| [**SWbemSecurity**](swbemsecurity.md)               | Gestisce le impostazioni di sicurezza, ad esempio i [**privilegi**](swbemsecurity-privileges.md)Component Object Model (com), [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)e [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md).   |
| [**SWbemServices**](swbemservices.md)               | Consente di creare, aggiornare e recuperare istanze o classi.                                                                                                                                                                                                  |
| [**SWbemServicesEx**](swbemservicesex.md)           | Estende la funzionalità di [**SWbemServices**](swbemservices.md). Questo oggetto aggiunge i metodi [**put**](swbemservicesex-put.md) e [**PutAsync**](swbemservicesex-putasync.md) per consentire il salvataggio di una classe o di un'istanza in più spazi dei nomi. |
| [**SWbemSink**](swbemsink.md)                       | Riceve i risultati delle operazioni asincrone e delle notifiche degli eventi, utilizzate dalle applicazioni client.                                                                                                                                        |



 

 

 



