---
title: Requisiti di sicurezza delle funzioni di gestione di rete
description: La chiamata di alcune funzioni di gestione della rete non richiede l'appartenenza speciale al gruppo.
ms.assetid: 846a5b81-d5bf-4275-a898-38e6ba308b8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b0987509294f03b8737aae5e721abf5dbdd90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517037"
---
# <a name="network-management-function-security-requirements"></a>Requisiti di sicurezza delle funzioni di gestione di rete

La chiamata di alcune funzioni di gestione della rete non richiede l'appartenenza speciale al gruppo. Per le altre funzioni è necessario che gli utenti dispongano di un livello di privilegio specifico per l'esecuzione corretta. Quando applicabile, la sezione Note nella pagina di riferimento di una funzione indica il livello di privilegio che un utente deve avere per eseguire la funzione specifica.

I requisiti di sicurezza che si applicano ai controller di dominio Active Directory possono essere diversi da quelli che si applicano ai server e alle workstation.

Per ulteriori informazioni e per un elenco delle funzioni interessate, vedere gli argomenti seguenti:

-   [Requisiti per le funzioni di gestione della rete nei controller di dominio Active Directory](requirements-for-network-management-functions-on-active-directory-domain-controllers.md)
-   [Requisiti per le funzioni di gestione della rete su server e workstation](requirements-for-network-management-functions-on-servers-and-workstations.md)

Per ulteriori informazioni sul controllo dell'accesso agli oggetti a protezione diretta, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control), [privilegi](/windows/desktop/SecAuthZ/privileges)e [oggetti a protezione diretta](/windows/desktop/SecAuthZ/securable-objects).

Per ulteriori informazioni sui descrittori di sicurezza specifici utilizzati durante i controlli di accesso, vedere la pagina di riferimento per le singole funzioni. Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).

 

 