---
title: Proprietà Role
description: La proprietà Role descrive l'elemento dell'interfaccia utente di un oggetto. Tutti gli oggetti supportano la proprietà Role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297902"
---
# <a name="role-property"></a><span data-ttu-id="19a33-104">Proprietà Role</span><span class="sxs-lookup"><span data-stu-id="19a33-104">Role Property</span></span>

<span data-ttu-id="19a33-105">La proprietà **Role** descrive l'elemento dell'interfaccia utente di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="19a33-105">The **Role** property describes an object's user interface element.</span></span> <span data-ttu-id="19a33-106">Tutti gli oggetti supportano la proprietà **Role** .</span><span class="sxs-lookup"><span data-stu-id="19a33-106">All objects support the **Role** property.</span></span>

<span data-ttu-id="19a33-107">In molti casi, il ruolo dell'oggetto è ovvio.</span><span class="sxs-lookup"><span data-stu-id="19a33-107">In many cases, the object's role is obvious.</span></span> <span data-ttu-id="19a33-108">Ad esempio, Windows ha il [**ruolo \_ \_ finestra del sistema ruolo**](object-roles.md) e i pulsanti di push hanno il ruolo [**\_ \_ pulsante sistema ruolo**](object-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="19a33-108">For example, windows have the [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) role and push buttons have the [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md) role.</span></span>

<span data-ttu-id="19a33-109">La proprietà **Role** viene recuperata chiamando [**IAccessible:: Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span><span class="sxs-lookup"><span data-stu-id="19a33-109">The **Role** property is retrieved by calling [**IAccessible::get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span></span>

## <a name="identifying-an-objects-role"></a><span data-ttu-id="19a33-110">Identificazione del ruolo di un oggetto</span><span class="sxs-lookup"><span data-stu-id="19a33-110">Identifying an Object's Role</span></span>

<span data-ttu-id="19a33-111">Microsoft Active Accessibility fornisce [costanti Role](object-roles.md), definite in oleacc. h, che identificano i ruoli comuni degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="19a33-111">Microsoft Active Accessibility provides [role constants](object-roles.md), defined in oleacc.h, that identify common object roles.</span></span> <span data-ttu-id="19a33-112">È consigliabile che gli sviluppatori di server usino questi valori di ruolo predefiniti.</span><span class="sxs-lookup"><span data-stu-id="19a33-112">It is recommended that server developers use these predefined role values.</span></span> <span data-ttu-id="19a33-113">Se viene restituita una costante di ruolo predefinita, i client usano la funzione [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) per recuperare una stringa localizzata che descrive il ruolo.</span><span class="sxs-lookup"><span data-stu-id="19a33-113">If a predefined role constant is returned, clients use the [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) function to retrieve a localized string that describes the role.</span></span>

<span data-ttu-id="19a33-114">Per i controlli di animazione, ad esempio il controllo dell'animazione visualizzato durante la copia dei file, usare l' [**\_ \_ animazione del sistema del ruolo**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="19a33-114">For animation controls, such as the animation control displayed when copying files, use [**ROLE\_SYSTEM\_ANIMATION**](object-roles.md).</span></span> <span data-ttu-id="19a33-115">Le immagini talvolta animate vengono descritte come [**\_ \_ Immagini del sistema di ruolo**](object-roles.md) con la proprietà [**stato**](state-property.md) impostata su [**stato del \_ sistema \_ animato**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="19a33-115">Graphics that are occasionally animated are described as [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md) with the [**State**](state-property.md) property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md).</span></span>

<span data-ttu-id="19a33-116">Si noti che alcuni ruoli non sono facili da descrivere.</span><span class="sxs-lookup"><span data-stu-id="19a33-116">Note that some roles are not easy to describe.</span></span> <span data-ttu-id="19a33-117">Ad esempio, la visualizzazione icone grandi di una cartella consente la disposizione arbitraria delle icone, quindi il suo ruolo può essere descritto come [**\_ \_ raggruppamento del sistema di ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="19a33-117">For example, a folder's large-icon view allows arbitrary arrangement of icons, so its role could be described as [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span> <span data-ttu-id="19a33-118">In alternativa, un controllo che fornisce elementi in righe e colonne fisse potrebbe avere il ruolo di [**\_ \_ tabella del sistema Role**](object-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="19a33-118">Or, a control that provides items in fixed rows and columns could have the [**ROLE\_SYSTEM\_TABLE**](object-roles.md) role.</span></span> <span data-ttu-id="19a33-119">Poiché un ruolo viene utilizzato per comunicare il modello di utilizzo a un utente finale, è importante utilizzare il ruolo appropriato.</span><span class="sxs-lookup"><span data-stu-id="19a33-119">Since a role is used to communicate the use model to an end user, it is important to use the appropriate role.</span></span> <span data-ttu-id="19a33-120">Ad esempio, se il controllo funziona come un pulsante, usare il pulsante del [**sistema di ruolo \_ \_**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="19a33-120">For example, if your control acts like a button, then use [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md).</span></span>

 

 




