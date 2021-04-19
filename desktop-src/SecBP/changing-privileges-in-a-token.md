---
description: Viene illustrato come modificare i privilegi in un token usando le funzioni AdjustTokenPrivileges e CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Modifica dei privilegi in un token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317741"
---
# <a name="changing-privileges-in-a-token"></a>Modifica dei privilegi in un token

È possibile modificare i privilegi in un token primario o di rappresentazione in due modi:

-   Abilitare o disabilitare i privilegi tramite la funzione [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .
-   Limitare o rimuovere i privilegi tramite la funzione [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) .

[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) non è in grado di aggiungere o rimuovere privilegi dal token. Può abilitare solo i privilegi esistenti attualmente disabilitati o disabilitare i privilegi esistenti attualmente abilitati. Per esempi, vedere [Abilitazione e disabilitazione dei privilegi in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

Per assegnare privilegi a un account utente, vedere [assegnazione di privilegi a un account](assigning-privileges-to-an-account.md).

[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) offre funzionalità più estese come segue:

-   Rimozione di un privilegio. Si noti che la rimozione di un privilegio non corrisponde alla disabilitazione di una. Una volta rimosso un privilegio da un token, non è possibile ripristinarlo.
-   Associazione dell'attributo di sola negazione ai SID nel token. Ciò comporta la disattivazione di gruppi o account specifici, ad esempio negando al gruppo Everyone l'accesso DELETE a un determinato file. Per altre informazioni sulla restrizione dei SID, vedere [attributi SID in un token di accesso](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).
-   Specificando un elenco di SID di restrizione nel token. Per informazioni sulla restrizione dei SID, vedere [token con restrizioni](/windows/desktop/SecAuthZ/restricted-tokens).

 

 
