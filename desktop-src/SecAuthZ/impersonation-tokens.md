---
description: Viene illustrato l'utilizzo dei token di rappresentazione nel controllo di accesso.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Token di rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317046"
---
# <a name="impersonation-tokens"></a>Token di rappresentazione

Un thread di rappresentazione ha due [*token di accesso*](/windows/desktop/SecGloss/a-gly):

-   Un [*token di accesso primario*](/windows/desktop/SecGloss/p-gly) che descrive il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) del server. Per ottenere un handle per questo token, chiamare la funzione [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .
-   Un token di accesso di rappresentazione che descrive il contesto di sicurezza del client rappresentato. Per ottenere un handle per questo token, chiamare la funzione [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) .

Un server può utilizzare il [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly) nelle funzioni seguenti:

-   Nelle funzioni [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)e [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) per determinare se un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) consente al client un set di diritti di accesso.
-   Nella funzione [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per abilitare o disabilitare i privilegi del client.
-   Nella funzione [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) per determinare se un set di privilegi è abilitato nel token del client.
-   In funzioni che generano voci nel registro eventi di sicurezza, ad esempio [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) o [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma). Queste funzioni usano un token di rappresentazione per ottenere informazioni sul client per la voce di log.

 

 
