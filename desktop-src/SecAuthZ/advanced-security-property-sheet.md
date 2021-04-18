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
# <a name="advanced-security-property-sheet"></a><span data-ttu-id="d330a-103">Finestra delle proprietà sicurezza avanzata</span><span class="sxs-lookup"><span data-stu-id="d330a-103">Advanced Security Property Sheet</span></span>

<span data-ttu-id="d330a-104">La finestra delle proprietà sicurezza avanzata consente all'utente di eseguire operazioni di modifica che non sono disponibili nella [pagina delle proprietà sicurezza di base](basic-security-property-page.md) di un editor di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="d330a-104">The advanced security property sheet enables the user to perform editing operations that are not available on the [basic security property page](basic-security-property-page.md) of an access control editor.</span></span> <span data-ttu-id="d330a-105">La finestra delle proprietà può includere le pagine delle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="d330a-105">The property sheet can include the following property pages:</span></span>

-   <span data-ttu-id="d330a-106">Pagina delle proprietà [delle autorizzazioni](permissions-property-page.md) per la modifica avanzata dell' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) dell'oggetto, ad esempio la modifica di [ACE specifiche dell'oggetto](object-specific-aces.md) o il controllo dell' [ereditarietà Ace](ace-inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="d330a-106">A [Permissions](permissions-property-page.md) property page for advanced editing of the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), such as editing [object-specific ACEs](object-specific-aces.md) or controlling [ACE inheritance](ace-inheritance.md).</span></span>
-   <span data-ttu-id="d330a-107">Pagina delle proprietà di [controllo](auditing-property-page.md) per la visualizzazione e la modifica dell' [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d330a-107">An [Auditing](auditing-property-page.md) property page for viewing and editing the object's [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span>
-   <span data-ttu-id="d330a-108">Pagina delle proprietà di un [proprietario](owner-property-page.md) per modificare il proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d330a-108">An [Owner](owner-property-page.md) property page for changing the object's owner.</span></span>

<span data-ttu-id="d330a-109">L'utente può visualizzare la finestra delle proprietà sicurezza avanzata facendo clic sul pulsante **Avanzate** nella pagina delle proprietà sicurezza di base.</span><span class="sxs-lookup"><span data-stu-id="d330a-109">The user can display the advanced security property sheet by clicking the **Advanced** button on the basic security property page.</span></span> <span data-ttu-id="d330a-110">Per visualizzare il pulsante **Avanzate** , impostare il \_ flag si Advanced nella struttura di [**\_ \_ informazioni sull'oggetto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) restituito dall'implementazione di [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="d330a-110">To display the **Advanced** button, set the SI\_ADVANCED flag in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
