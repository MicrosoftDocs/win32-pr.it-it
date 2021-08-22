---
description: Le informazioni di riferimento sull'API di scripting per WMI descrivono ogni oggetto di scripting usando una sintassi specifica. Per una spiegazione di questa sintassi, vedere Convenzioni dei documenti per l'API di scripting.
ms.assetid: 91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26
ms.tgt_platform: multiple
title: Scripting di oggetti API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd639e1b1ca482a2b1aa95a4e0a6a26672480660440af290c043814ce5f8e965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050309"
---
# <a name="scripting-api-objects"></a>Scripting di oggetti API

Le informazioni di riferimento sull'API di scripting per WMI descrivono ogni oggetto di scripting usando una sintassi specifica. Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Nella tabella seguente sono elencati gli oggetti di scripting WMI e il modo in cui vengono usati.



| Oggetto                                               | Descrizione                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)               | Costruisce e analizza i valori [datetime](date-and-time-format.md) CIM.                                                                                                                                                                                 |
| [**SWbemEventSource**](swbemeventsource.md)         | Recupera gli eventi in combinazione con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).                                                                                                                               |
| [**SWbemLastError**](swbemlasterror.md)             | Fornisce informazioni estese sugli errori quando si verifica un errore.                                                                                                                                                                                              |
| [**SWbemLocator**](swbemlocator.md)                 | Ottiene un oggetto [**SWbemServices**](swbemservices.md) che può ottenere l'accesso a WMI in un computer host specifico.                                                                                                                                     |
| [**SWbemMethod**](swbemmethod.md)                   | Contiene una singola definizione di metodo WMI.                                                                                                                                                                                                               |
| [**SWbemMethodSet**](swbemmethodset.md)             | Ottiene una raccolta di [**oggetti SWbemMethod.**](swbemmethod.md)                                                                                                                                                                                       |
| [**SWbemNamedValue**](swbemnamedvalue.md)           | Contiene un singolo valore denominato.                                                                                                                                                                                                                         |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md)     | Ottiene l'accesso a una raccolta [**di oggetti SWbemNamedValue.**](swbemnamedvalue.md)                                                                                                                                                                     |
| [**SWbemObject**](swbemobject.md)                   | Contiene e modifica una singola classe o istanza di oggetto WMI.                                                                                                                                                                                        |
| [**SWbemObjectEx**](swbemobjectex.md)               | Estende la funzionalità di [**SWbemObject**](swbemobject.md). Questo oggetto aggiunge il [**metodo Refresh**](swbemrefresher-refresh.md) per gli [**oggetti SWbemRefresher.**](swbemrefresher.md)                                                           |
| [**SWbemObjectPath**](swbemobjectpath.md)           | Genera e convalida il percorso di un oggetto.                                                                                                                                                                                                                |
| [**SWbemObjectSet**](swbemobjectset.md)             | Ottiene l'accesso a una raccolta [**di oggetti SWbemObject.**](swbemobject.md)                                                                                                                                                                             |
| [**SWbemPrivilege**](swbemprivilege.md)             | Imposta o cancella un privilegio.                                                                                                                                                                                                                            |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)       | Ottiene l'accesso a una raccolta [**di oggetti SWbemPrivilege.**](swbemprivilege.md)                                                                                                                                                                       |
| [**Proprietà SWbemProperty**](swbemproperty.md)               | Contiene una singola proprietà WMI.                                                                                                                                                                                                                        |
| [**SWbemPropertySet**](swbempropertyset.md)         | Ottiene l'accesso a una raccolta [**di oggetti SWbemProperty.**](swbemproperty.md)                                                                                                                                                                         |
| [**SWbemQualifier**](swbemqualifier.md)             | Contiene un singolo qualificatore di proprietà.                                                                                                                                                                                                                  |
| [**SWbemQualifierSet**](swbemqualifierset.md)       | Ottiene l'accesso a una raccolta [**di oggetti SWbemQualifier.**](swbemqualifier.md)                                                                                                                                                                       |
| [**SWbemRefresher**](swbemrefresher.md)             | Raccoglie e aggiorna i valori delle proprietà dell'oggetto in un'unica operazione.                                                                                                                                                                                          |
| [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Rappresenta un singolo elemento aggiornabile in [**un oggetto SWbemRefresher,**](swbemrefresher.md) ad esempio una proprietà .                                                                                                                                     |
| [**SWbemSecurity**](swbemsecurity.md)               | Gestisce le impostazioni di sicurezza, ad [](swbemsecurity-privileges.md)esempio Component Object Model (COM), [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)e [**ImpersonationLevel.**](swbemsecurity-impersonationlevel.md)   |
| [**SWbemServices**](swbemservices.md)               | Crea, aggiorna e recupera istanze o classi.                                                                                                                                                                                                  |
| [**SWbemServicesEx**](swbemservicesex.md)           | Estende la funzionalità di [**SWbemServices**](swbemservices.md). Questo oggetto aggiunge i [**metodi Put**](swbemservicesex-put.md) e [**PutAsync**](swbemservicesex-putasync.md) per consentire il salvataggio di una classe o di un'istanza in più spazi dei nomi. |
| [**SWbemSink**](swbemsink.md)                       | Riceve i risultati delle operazioni asincrone e delle notifiche degli eventi, usati dalle applicazioni client.                                                                                                                                        |



 

 

 



