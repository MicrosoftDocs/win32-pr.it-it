---
description: Il \_ \_ diritto di accesso di sicurezza del sistema Access controlla la possibilità di ottenere o impostare l'elenco SACL in un descrittore di sicurezza degli oggetti. Il sistema concede questo diritto di accesso se il \_ \_ privilegio per il nome di sicurezza se è abilitato nel token di accesso del thread richiedente.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Accesso SACL a destra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308138"
---
# <a name="sacl-access-right"></a>Accesso SACL a destra

Il \_ \_ diritto di accesso di sicurezza del sistema Access controlla la possibilità di ottenere o impostare l'elenco SACL nel [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)di un oggetto. Il sistema concede questo diritto di accesso solo se il \_ \_ privilegio del nome di sicurezza se è abilitato nel [*token di accesso*](/windows/desktop/SecGloss/a-gly) del thread richiedente.

**Per accedere al SACL di un oggetto**

1.  Chiamare la funzione [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per abilitare il \_ privilegio se \_ nome di sicurezza.
2.  \_ \_ Quando si apre un handle per l'oggetto, richiedere il diritto di accesso di sicurezza del sistema di accesso.
3.  Ottenere o impostare il SACL dell'oggetto utilizzando una funzione quale [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).
4.  Chiamare [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per disabilitare il privilegio se il \_ nome di sicurezza \_ .

Per accedere a un SACL usando le funzioni [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) o [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , abilitare il \_ \_ privilegio se nome sicurezza. La funzione richiede internamente il diritto di accesso.

Il \_ diritto di \_ accesso di sicurezza del sistema di accesso non è valido in un DACL perché gli elenchi DACL non controllano l'accesso a un SACL. Tuttavia, è possibile usare il \_ diritto di accesso di sicurezza del sistema di accesso \_ in un SACL per controllare i tentativi di usare il diritto di accesso.

 

 
