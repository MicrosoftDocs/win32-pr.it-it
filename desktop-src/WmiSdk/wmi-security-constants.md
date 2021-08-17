---
description: WMI controlla i diritti di accesso per applicazioni e script.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Costanti di sicurezza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2f3a8ff4727852637fe6e4b808f0b8d3a74c958808cb3beb7bc9df32b0c995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739418"
---
# <a name="wmi-security-constants"></a>Costanti di sicurezza WMI

WMI controlla i diritti di accesso per applicazioni e script per oggetti quali spazi dei nomi WMI, stampante, servizi, applicazioni DCOM, file, condivisioni e altri oggetti a protezione diretta. L'accesso a questi oggetti a protezione diretta è controllato dalle voci di controllo di accesso (ACE). Ogni ACE contiene elenchi che specificano quali gruppi o utenti hanno accesso. Per altre informazioni sugli elenchi di sicurezza e controllo di accesso (ACL, DACL o SACL), vedere Elenchi di controllo di accesso [(ACL)](/windows/desktop/SecAuthZ/access-control-lists) e Descrittori [di sicurezza](/windows/desktop/SecAuthZ/security-descriptors).

Molti metodi provider in WMI che influiscono sugli oggetti a protezione diretta richiedono all'amministratore di abilitare determinati privilegi. La versione del privilegio utilizzata dipende dal linguaggio di programmazione, come illustrato in [**Costanti dei privilegi**](privilege-constants.md).

Le costanti di sicurezza sono definite negli argomenti seguenti:

-   [**Costanti di sicurezza degli eventi**](event-security-constants.md)
-   [**Costanti dei diritti di accesso a file e directory**](file-and-directory-access-rights-constants.md)
-   [**Costanti dei diritti di accesso allo spazio dei nomi**](namespace-access-rights-constants.md)
-   [**Costanti del flag ACE dello spazio dei nomi**](namespace-ace-flag-constants.md)
-   [**Costanti del tipo ACE dello spazio dei nomi**](namespace-ace-type-constants.md)
-   [**Costanti dei privilegi**](privilege-constants.md)

 

 
