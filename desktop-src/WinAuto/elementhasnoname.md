---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332660"
---
# <a name="elementhasnoname"></a><span data-ttu-id="93267-103">ElementHasNoName</span><span class="sxs-lookup"><span data-stu-id="93267-103">ElementHasNoName</span></span>

## <a name="text"></a><span data-ttu-id="93267-104">Testo</span><span class="sxs-lookup"><span data-stu-id="93267-104">Text</span></span>

<span data-ttu-id="93267-105">Elemento senza nome</span><span class="sxs-lookup"><span data-stu-id="93267-105">Element has no name</span></span>

## <a name="type"></a><span data-ttu-id="93267-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="93267-106">Type</span></span>

<span data-ttu-id="93267-107">Errore</span><span class="sxs-lookup"><span data-stu-id="93267-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="93267-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93267-108">Description</span></span>

<span data-ttu-id="93267-109">Un elemento non ha un nome.</span><span class="sxs-lookup"><span data-stu-id="93267-109">An element does not have a name.</span></span> <span data-ttu-id="93267-110">Ad esempio, l'elemento non dispone di accName implementato e viene restituita una stringa vuota quando viene usato il metodo [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) per recuperare il nome MSAA dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="93267-110">For example, the element does not have accName implemented and an empty string is returned when the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method is used to retrieve the MSAA name of the element.</span></span>

<span data-ttu-id="93267-111">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché un elemento potrebbe essere identificato erroneamente dall'utente.</span><span class="sxs-lookup"><span data-stu-id="93267-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="93267-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="93267-112">Possible causes</span></span>

-   <span data-ttu-id="93267-113">L'elemento o il relativo elemento padre non dispone di un nome o di un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="93267-113">The element or its parent has no name or label.</span></span>
-   <span data-ttu-id="93267-114">All'elemento viene assegnato un [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) che suggerisce che l'elemento ha un nome.</span><span class="sxs-lookup"><span data-stu-id="93267-114">The element is assigned an [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) that suggests the element have a name.</span></span>
-   <span data-ttu-id="93267-115">L'elemento con lo stato attivo non deve ricevere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="93267-115">The element that has focus should not receive focus.</span></span> <span data-ttu-id="93267-116">Ad esempio, un'etichetta o un controllo disabilitato.</span><span class="sxs-lookup"><span data-stu-id="93267-116">For example, a label or a disabled control.</span></span>
-   <span data-ttu-id="93267-117">Un controllo invisibile ha ricevuto lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="93267-117">An invisible control has received focus.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93267-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="93267-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93267-119">**IAccessible:: Get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="93267-119">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="93267-120">Proprietà Name</span><span class="sxs-lookup"><span data-stu-id="93267-120">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




