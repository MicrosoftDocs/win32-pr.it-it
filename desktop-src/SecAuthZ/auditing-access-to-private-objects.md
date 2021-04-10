---
description: Un server protetto può utilizzare le funzioni seguenti per generare i report di controllo nel registro eventi di protezione.
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: Controllo dell'accesso a oggetti privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3669841714fe9c24f6346404bc8634222bc4557e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968666"
---
# <a name="auditing-access-to-private-objects"></a>Controllo dell'accesso a oggetti privati

Un server protetto può utilizzare le funzioni seguenti per generare i report di controllo nel registro eventi di protezione.



| Funzione                                                                                                     | Descrizione                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)                                                 | Uguale alla funzione [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) con la differenza che può generare messaggi di controllo per tentativi di accesso non riusciti o riusciti.                                                                            |
| [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)                                     | Uguale alla funzione [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) con la differenza che può generare messaggi di controllo per tentativi di accesso non riusciti o riusciti.                                                                |
| [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)                 | Uguale alla funzione [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) con la differenza che può generare messaggi di controllo per tentativi di accesso non riusciti o riusciti.                                            |
| [**AccessCheckByTypeResultListAndAuditAlarmByHandle**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea) | Uguale alla funzione [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) con la differenza che consente al thread chiamante di eseguire il controllo di accesso prima di rappresentare il client. |
| [**ObjectCloseAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectcloseauditalarma)                                                       | Genera un messaggio di controllo per indicare che un client ha tentato di chiudere un oggetto privato.                                                                                                                                   |
| [**ObjectDeleteAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                       | Genera un messaggio di controllo per indicare che un client ha tentato di eliminare un oggetto privato.                                                                                                                                  |
| [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                         | Genera un messaggio di controllo per indicare che un client ha tentato di aprire o creare un oggetto privato.                                                                                                                          |
| [**ObjectPrivilegeAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectprivilegeauditalarma)                                               | Genera un messaggio di controllo per indicare che un client ha tentato di utilizzare un set di privilegi specificato insieme a un tentativo di accesso a un oggetto privato.                                                              |
| [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)                                           | Genera un messaggio di controllo per indicare che un client ha tentato di utilizzare un set di privilegi specificato.                                                                                                                        |



 

 

 
