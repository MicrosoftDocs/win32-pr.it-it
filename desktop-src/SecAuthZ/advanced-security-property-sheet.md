---
description: La finestra delle proprietà sicurezza avanzata consente all'utente di eseguire operazioni di modifica che non sono disponibili nella pagina delle proprietà di sicurezza di base di un editor di controllo di accesso.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Finestra delle proprietà Sicurezza avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808eaefaa481e828504eb55b3ecc3b70d487c03af82b296c3b8bc02da2b354d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914347"
---
# <a name="advanced-security-property-sheet"></a>Finestra delle proprietà Sicurezza avanzata

La finestra delle proprietà sicurezza avanzata consente all'utente di eseguire operazioni di modifica che non sono disponibili nella pagina delle proprietà di sicurezza [di base](basic-security-property-page.md) di un editor di controllo di accesso. La finestra delle proprietà può includere le pagine delle proprietà seguenti:

-   Pagina [delle proprietà](permissions-property-page.md) Autorizzazioni per la modifica avanzata dell'elenco di controllo [](object-specific-aces.md) di accesso discrezionale (DACL) dell'oggetto, ad esempio la modifica di ACE specifiche dell'oggetto o il controllo dell'ereditarietà [](/windows/desktop/SecGloss/d-gly) [ACE.](ace-inheritance.md)
-   Pagina [delle proprietà Controllo](auditing-property-page.md) per la visualizzazione e la modifica dell'elenco di controllo di accesso di sistema (SACL) dell'oggetto. [](/windows/desktop/SecGloss/s-gly)
-   Pagina [delle proprietà](owner-property-page.md) Owner per la modifica del proprietario dell'oggetto.

L'utente può visualizzare la finestra delle proprietà di sicurezza avanzata facendo clic sul **pulsante** Avanzate nella pagina delle proprietà di sicurezza di base. Per visualizzare il **pulsante Avanzate,** impostare il flag SI ADVANCED nella struttura \_ SI OBJECT [**\_ \_ INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) restituita dall'implementazione [**di ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation)

 

 
