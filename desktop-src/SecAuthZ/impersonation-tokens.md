---
description: Viene illustrato l'utilizzo dei token di rappresentazione nel controllo di accesso.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Token di rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67acf48a1f274703850fc8bfc2167014708124c46743f416591510b6c9ab559b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908141"
---
# <a name="impersonation-tokens"></a>Token di rappresentazione

Un thread di rappresentazione ha due [*token di accesso:*](/windows/desktop/SecGloss/a-gly)

-   Token [*di accesso primario*](/windows/desktop/SecGloss/p-gly) che descrive il contesto [*di*](/windows/desktop/SecGloss/s-gly) sicurezza del server. Per ottenere un handle per questo token, chiamare la [**funzione OpenProcessToken.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)
-   Token di accesso di rappresentazione che descrive il contesto di sicurezza del client rappresentato. Per ottenere un handle per questo token, chiamare la [**funzione OpenThreadToken.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)

Un server può utilizzare il [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly) nelle funzioni seguenti:

-   Nelle funzioni [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)e [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) per determinare se un descrittore di sicurezza consente al client un set di diritti di accesso. [](/windows/desktop/SecGloss/s-gly)
-   Nella [**funzione AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) abilitare o disabilitare i privilegi del client.
-   Nella funzione [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) per determinare se un set di privilegi è abilitato nel token del client.
-   Nelle funzioni che generano voci nel registro eventi di sicurezza, ad esempio [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) [**o PrivilegedServiceAuditAlarm.**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma) Queste funzioni usano un token di rappresentazione per ottenere informazioni sul client per la voce di log.

 

 
