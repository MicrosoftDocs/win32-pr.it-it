---
description: WMI controlla i diritti di accesso per le applicazioni e gli script.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Costanti di sicurezza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233669"
---
# <a name="wmi-security-constants"></a>Costanti di sicurezza WMI

WMI verifica i diritti di accesso per le applicazioni e gli script per oggetti quali gli spazi dei nomi WMI, le stampanti, i servizi, le applicazioni DCOM, i file, le condivisioni e altri oggetti a protezione diretta. L'accesso a tali oggetti a protezione diretta è controllato dalle voci di controllo di accesso (ACE). Ogni voce ACE contiene elenchi che definiscono i gruppi o gli utenti che hanno accesso. Per ulteriori informazioni sugli elenchi di controllo di accesso e sicurezza (ACL, elenchi DACL o SACL), vedere [elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e [descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors).

Molti metodi del provider in WMI che interessano gli oggetti a protezione diretta richiedono che l'amministratore abiliti determinati privilegi. La versione del privilegio da usare dipende dal linguaggio di programmazione, come illustrato in [**costanti Privilege**](privilege-constants.md).

Le costanti di sicurezza sono definite negli argomenti seguenti:

-   [**Costanti di sicurezza degli eventi**](event-security-constants.md)
-   [**Costanti dei diritti di accesso a file e directory**](file-and-directory-access-rights-constants.md)
-   [**Costanti dei diritti di accesso allo spazio dei nomi**](namespace-access-rights-constants.md)
-   [**Costanti del flag ACE dello spazio dei nomi**](namespace-ace-flag-constants.md)
-   [**Costanti di tipo ACE dello spazio dei nomi**](namespace-ace-type-constants.md)
-   [**Costanti Privilege**](privilege-constants.md)

 

 
