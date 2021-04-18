---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297907"
---
# <a name="invalidrole"></a><span data-ttu-id="9caee-103">InvalidRole</span><span class="sxs-lookup"><span data-stu-id="9caee-103">InvalidRole</span></span>

## <a name="text"></a><span data-ttu-id="9caee-104">Testo</span><span class="sxs-lookup"><span data-stu-id="9caee-104">Text</span></span>

<span data-ttu-id="9caee-105">Il valore int restituito da Get \_ accRole non è una costante Role valida, ovvero un sistema di ruoli IE \_\_\*</span><span class="sxs-lookup"><span data-stu-id="9caee-105">The int returned from get\_accRole is not a valid role constant, ie ROLE\_SYSTEM\_\*</span></span>

## <a name="type"></a><span data-ttu-id="9caee-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="9caee-106">Type</span></span>

<span data-ttu-id="9caee-107">Errore</span><span class="sxs-lookup"><span data-stu-id="9caee-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="9caee-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9caee-108">Description</span></span>

<span data-ttu-id="9caee-109">Un elemento segnala un ruolo MSAA non valido.</span><span class="sxs-lookup"><span data-stu-id="9caee-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="9caee-110">Ad esempio, il metodo [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) restituisce un valore integer che non esegue il mapping a una costante del ruolo oggetto valida, ad esempio ListItem del sistema del ruolo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9caee-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method returns an integer value that does not map to a valid object role constant (such as ROLE\_SYSTEM\_LISTITEM).</span></span>

<span data-ttu-id="9caee-111">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché gli elementi potrebbero essere identificati erroneamente dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9caee-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="9caee-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="9caee-112">Possible causes</span></span>

<span data-ttu-id="9caee-113">Per l'elemento o per il relativo padre è impostato un ruolo MSAA in modo non appropriato.</span><span class="sxs-lookup"><span data-stu-id="9caee-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9caee-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9caee-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9caee-115">**IAccessible:: Get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="9caee-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="9caee-116">**Ruoli oggetto**</span><span class="sxs-lookup"><span data-stu-id="9caee-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




