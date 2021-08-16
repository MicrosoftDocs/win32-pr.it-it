---
description: Il diritto di accesso ACCESS \_ SYSTEM SECURITY controlla la possibilità di ottenere o impostare l'elenco \_ sacl in un descrittore di sicurezza degli oggetti. Il sistema concede questo diritto di accesso se edizione Standard il privilegio SECURITY NAME è abilitato nel token di \_ \_ accesso del thread richiedente.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Diritto di accesso SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88256664db25c6e906f3b4ca0459217a29d0cc7c0e2dd544c1cf198bc24fff5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780516"
---
# <a name="sacl-access-right"></a>Diritto di accesso SACL

Il diritto di accesso ACCESS \_ SYSTEM SECURITY controlla la possibilità di ottenere o impostare \_ l'elenco sacl nel descrittore di sicurezza [*di un oggetto*](/windows/desktop/SecGloss/s-gly). Il sistema concede questo diritto di accesso solo se edizione Standard il privilegio SECURITY NAME è abilitato nel token di \_ \_ accesso del thread richiedente. [](/windows/desktop/SecGloss/a-gly)

**Per accedere all'elenco SACL di un oggetto**

1.  Chiamare la [**funzione AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per abilitare il edizione Standard \_ SECURITY \_ NAME.
2.  Richiedere il diritto di accesso ACCESS \_ SYSTEM SECURITY quando si apre un handle per \_ l'oggetto.
3.  Ottenere o impostare l'elenco SACL dell'oggetto usando una funzione come [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).
4.  Chiamare [**AdjustTokenPrivileges per**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) disabilitare il edizione Standard \_ SECURITY \_ NAME.

Per accedere a un SACL usando [**le funzioni GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) o [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) abilitare il edizione Standard \_ SECURITY \_ NAME. La funzione richiede internamente il diritto di accesso.

Il diritto di accesso ACCESS SYSTEM SECURITY non è valido in un elenco DACL perché gli daCL non \_ \_ controllano l'accesso a un SACL. Tuttavia, è possibile usare il diritto di accesso ACCESS SYSTEM SECURITY in un SACL per controllare i \_ \_ tentativi di utilizzo del diritto di accesso.

 

 
