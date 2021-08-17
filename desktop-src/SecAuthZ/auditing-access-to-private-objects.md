---
description: Un server protetto può utilizzare le funzioni seguenti per generare report di controllo nel registro eventi di sicurezza.
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: Controllo dell'accesso agli oggetti privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac3a38a9f0af292a77a539491e0cea5f1faf40b570f34a35371ad43a7abe757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784592"
---
# <a name="auditing-access-to-private-objects"></a>Controllo dell'accesso agli oggetti privati

Un server protetto può utilizzare le funzioni seguenti per generare report di controllo nel registro eventi di sicurezza.



| Funzione                                                                                                     | Descrizione                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)                                                 | Uguale alla funzione [**AccessCheck,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) ad eccezione del fatto che può generare messaggi di controllo per i tentativi di accesso non riusciti o riusciti.                                                                            |
| [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)                                     | Uguale alla funzione [**AccessCheckByType,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) ad eccezione del fatto che può generare messaggi di controllo per i tentativi di accesso non riusciti o riusciti.                                                                |
| [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)                 | Uguale alla funzione [**AccessCheckByTypeResultList,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) ad eccezione del fatto che può generare messaggi di controllo per i tentativi di accesso non riusciti o riusciti.                                            |
| [**AccessCheckByTypeResultListAndAuditAlarmByHandle**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea) | Uguale alla funzione [**AccessCheckByTypeResultListAndAuditAlarm,**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) ad eccezione del fatto che consente al thread chiamante di eseguire il controllo di accesso prima di rappresentare il client. |
| [**ObjectCloseAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectcloseauditalarma)                                                       | Genera un messaggio di controllo per indicare che un client ha tentato di chiudere un oggetto privato.                                                                                                                                   |
| [**ObjectDeleteAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                       | Genera un messaggio di controllo per indicare che un client ha tentato di eliminare un oggetto privato.                                                                                                                                  |
| [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                         | Genera un messaggio di controllo per indicare che un client ha tentato di aprire o creare un oggetto privato.                                                                                                                          |
| [**ObjectPrivilegeAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectprivilegeauditalarma)                                               | Genera un messaggio di controllo per indicare che un client ha tentato di utilizzare un set specificato di privilegi insieme a un tentativo di accedere a un oggetto privato.                                                              |
| [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)                                           | Genera un messaggio di controllo per indicare che un client ha tentato di utilizzare un set specificato di privilegi.                                                                                                                        |



 

 

 
