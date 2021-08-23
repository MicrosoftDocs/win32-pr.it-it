---
description: Viene illustrato come modificare i privilegi in un token usando le funzioni AdjustTokenPrivileges e CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Modifica dei privilegi in un token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c511ca66c5d4739057f5ea75cae589ee97e849f659002a612e7d22fd6be8eecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622751"
---
# <a name="changing-privileges-in-a-token"></a>Modifica dei privilegi in un token

È possibile modificare i privilegi in un token di rappresentazione o primario in due modi:

-   Abilitare o disabilitare i privilegi usando la [**funzione AdjustTokenPrivileges.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges)
-   Limitare o rimuovere privilegi usando la [**funzione CreateRestrictedToken.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken)

[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) non può aggiungere o rimuovere privilegi dal token. Può abilitare solo i privilegi esistenti attualmente disabilitati o disabilitare quelli esistenti attualmente abilitati. Per esempi, vedere [Abilitazione e disabilitazione dei privilegi in C++.](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--)

Per assegnare privilegi a un account utente, vedere [Assegnazione di privilegi a un account](assigning-privileges-to-an-account.md).

[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) ha funzionalità più estese, come indicato di seguito:

-   Rimozione di un privilegio. Si noti che la rimozione di un privilegio non corrisponde alla disabilitazione di un privilegio. Dopo che un privilegio è stato rimosso da un token, non può essere riessto.
-   Collegamento dell'attributo di sola negazione ai SID nel token. Ciò ha l'effetto di non consentire l'accesso a gruppi o account specifici, ad esempio negando l'accesso a un determinato file da parte del gruppo Everyone. Per altre informazioni sulla limitazione dei SID, vedere [Attributi SID in un token di accesso](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).
-   Specifica di un elenco di SID di limitazione nel token. Per informazioni sulla limitazione dei SID, vedere [Token con restrizioni](/windows/desktop/SecAuthZ/restricted-tokens).

 

 
