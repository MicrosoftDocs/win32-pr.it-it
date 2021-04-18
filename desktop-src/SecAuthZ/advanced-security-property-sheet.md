---
description: La finestra delle proprietà sicurezza avanzata consente all'utente di eseguire operazioni di modifica che non sono disponibili nella pagina delle proprietà sicurezza di base di un editor di controllo di accesso.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Finestra delle proprietà sicurezza avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c8fe19b9336434c789d5e61a295cf7784afbf3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319403"
---
# <a name="advanced-security-property-sheet"></a>Finestra delle proprietà sicurezza avanzata

La finestra delle proprietà sicurezza avanzata consente all'utente di eseguire operazioni di modifica che non sono disponibili nella [pagina delle proprietà sicurezza di base](basic-security-property-page.md) di un editor di controllo di accesso. La finestra delle proprietà può includere le pagine delle proprietà seguenti:

-   Pagina delle proprietà [delle autorizzazioni](permissions-property-page.md) per la modifica avanzata dell' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) dell'oggetto, ad esempio la modifica di [ACE specifiche dell'oggetto](object-specific-aces.md) o il controllo dell' [ereditarietà Ace](ace-inheritance.md).
-   Pagina delle proprietà di [controllo](auditing-property-page.md) per la visualizzazione e la modifica dell' [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) dell'oggetto.
-   Pagina delle proprietà di un [proprietario](owner-property-page.md) per modificare il proprietario dell'oggetto.

L'utente può visualizzare la finestra delle proprietà sicurezza avanzata facendo clic sul pulsante **Avanzate** nella pagina delle proprietà sicurezza di base. Per visualizzare il pulsante **Avanzate** , impostare il \_ flag si Advanced nella struttura di [**\_ \_ informazioni sull'oggetto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) restituito dall'implementazione di [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 
