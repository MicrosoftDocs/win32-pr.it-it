---
description: Rende disponibili le interfacce dell'API di scripting per WMI ai programmatori C/C++, al posto delle versioni dell'API COM.
ms.assetid: 18f6cc70-9df1-4d43-a2e0-af03e2f9e2c5
ms.tgt_platform: multiple
title: Interfacce di automazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652e9a1fb35a66bddb9f0aebe543770e89e6e2ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316577"
---
# <a name="automation-interfaces"></a>Interfacce di automazione

L'API di automazione rende disponibili le interfacce dell'API di scripting per WMI ai programmatori C/C++, al posto delle versioni dell'API COM.

La tabella seguente elenca gli oggetti WMI e il modo in cui vengono usati nell'API di automazione. Il collegamento tra riferimenti alla documentazione dell'interfaccia per l'API di scripting per gli equivalenti WMI.



| Oggetto di automazione                                 | Descrizione                                                                                                                 |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**ISWbemEventSource**](swbemeventsource.md)     | Recupera gli eventi in combinazione con [**ISWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).   |
| [**ISWbemLastError**](swbemlasterror.md)         | Fornisce informazioni estese sugli errori quando si verifica un errore.                                                                   |
| [**ISWbemLocator**](swbemlocator.md)             | Ottiene un riferimento a un oggetto [**ISWbemServices**](swbemservices.md) che può accedere a WMI in un determinato computer host. |
| [**ISWbemMethod**](swbemmethod.md)               | Contiene una singola definizione di metodo.                                                                                        |
| [**ISWbemMethodSet**](swbemmethodset.md)         | Ottiene l'accesso a una raccolta di oggetti [**ISWbemMethod**](swbemmethod.md) .                                                 |
| [**ISWbemNamedValue**](swbemnamedvalue.md)       | Contiene un singolo valore denominato.                                                                                              |
| [**ISWbemNamedValueSet**](swbemnamedvalueset.md) | Ottiene l'accesso a una raccolta di oggetti [**ISWbemNamedValue**](swbemnamedvalue.md) .                                         |
| [**ISWbemObject**](swbemobject.md)               | Contiene e modifica un'istanza o una classe di oggetti Common Information Model (CIM) singolo.                                  |
| [**ISWbemObjectPath**](swbemobjectpath.md)       | Genera e convalida un percorso dell'oggetto.                                                                                     |
| [**ISWbemObjectSet**](swbemobjectset.md)         | Ottiene l'accesso a una raccolta di oggetti [**ISWbemObject**](swbemobject.md) .                                                 |
| [**ISWbemPrivilege**](swbemprivilege.md)         | Imposta o cancella un privilegio.                                                                                                 |
| [**ISWbemPrivilegeSet**](swbemprivilegeset.md)   | Ottiene l'accesso a una raccolta di oggetti [**ISWbemPrivilege**](swbemprivilege.md) .                                           |
| [**ISWbemProperty**](swbemproperty.md)           | Utilizzato per contenere una singola proprietà CIM.                                                                                      |
| [**ISWbemPropertySet**](swbempropertyset.md)     | Ottenere l'accesso a una raccolta di oggetti [**ISWbemProperty**](swbemproperty.md) .                                              |
| [**ISWbemQualifier**](swbemqualifier.md)         | Contiene un qualificatore di classe singola.                                                                                          |
| [**ISWbemQualifierSet**](swbemqualifierset.md)   | Ottiene l'accesso a una raccolta di oggetti [**ISWbemQualifier**](swbemqualifier.md) .                                           |
| [**ISWbemSecurity**](swbemsecurity.md)           | Gestisce le impostazioni di sicurezza, ad esempio Component Object Model (COM) Privilege, AuthenticationLevel e ImpersonationLevel.      |
| [**ISWbemServices**](swbemservices.md)           | Consente di creare, aggiornare e recuperare istanze o classi.                                                                       |
| [**ISWbemSink**](swbemsink.md)                   | Riceve i risultati delle operazioni asincrone dell'applicazione client e delle notifiche degli eventi.                                 |



 

 

 



