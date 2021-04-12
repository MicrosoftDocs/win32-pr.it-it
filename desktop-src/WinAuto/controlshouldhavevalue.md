---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221593"
---
# <a name="controlshouldhavevalue"></a><span data-ttu-id="ba930-103">ControlShouldHaveValue</span><span class="sxs-lookup"><span data-stu-id="ba930-103">ControlShouldHaveValue</span></span>

## <a name="text"></a><span data-ttu-id="ba930-104">Testo</span><span class="sxs-lookup"><span data-stu-id="ba930-104">Text</span></span>

<span data-ttu-id="ba930-105">Un controllo con ruolo {0} deve avere un valore ma Get \_ accValue non è implementato</span><span class="sxs-lookup"><span data-stu-id="ba930-105">A control with role of {0} should have a value but get\_accValue is not implemented</span></span>

## <a name="type"></a><span data-ttu-id="ba930-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ba930-106">Type</span></span>

<span data-ttu-id="ba930-107">Errore</span><span class="sxs-lookup"><span data-stu-id="ba930-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="ba930-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba930-108">Description</span></span>

<span data-ttu-id="ba930-109">Un elemento non fornisce un valore come previsto in base al ruolo MSAA assegnato, a indicare che l'elemento non ha implementato il metodo [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) .</span><span class="sxs-lookup"><span data-stu-id="ba930-109">An element does not supply a value as expected based on the assigned MSAA role, implying that the element does not have the [**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) method implemented.</span></span> <span data-ttu-id="ba930-110">I ruoli MSAA seguenti, ad esempio, devono fornire un valore.</span><span class="sxs-lookup"><span data-stu-id="ba930-110">For example, the following MSAA roles should all supply a value.</span></span>

-   <span data-ttu-id="ba930-111">\_ \_ casella combinata sistema ruolo</span><span class="sxs-lookup"><span data-stu-id="ba930-111">ROLE\_SYSTEM\_COMBOBOX</span></span>
-   <span data-ttu-id="ba930-112">\_IPAddress sistema \_ ruolo</span><span class="sxs-lookup"><span data-stu-id="ba930-112">ROLE\_SYSTEM\_IPADDRESS</span></span>
-   <span data-ttu-id="ba930-113">\_collegamento del sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="ba930-113">ROLE\_SYSTEM\_LINK</span></span>
-   <span data-ttu-id="ba930-114">\_OUTLINEITEM di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="ba930-114">ROLE\_SYSTEM\_OUTLINEITEM</span></span>
-   <span data-ttu-id="ba930-115">\_PROGRESSBAR del sistema di ruolo \_</span><span class="sxs-lookup"><span data-stu-id="ba930-115">ROLE\_SYSTEM\_PROGRESSBAR</span></span>
-   <span data-ttu-id="ba930-116">\_dispositivo di \_ scorrimento sistema ruolo</span><span class="sxs-lookup"><span data-stu-id="ba930-116">ROLE\_SYSTEM\_SLIDER</span></span>
-   <span data-ttu-id="ba930-117">\_SPINBUTTON di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="ba930-117">ROLE\_SYSTEM\_SPINBUTTON</span></span>
-   <span data-ttu-id="ba930-118">\_barra di \_ scorrimento sistema ruolo</span><span class="sxs-lookup"><span data-stu-id="ba930-118">ROLE\_SYSTEM\_SCROLLBAR</span></span>
-   <span data-ttu-id="ba930-119">\_testo del sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="ba930-119">ROLE\_SYSTEM\_TEXT</span></span>

<span data-ttu-id="ba930-120">Questo problema rappresenta un problema per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché un elemento con un valore intrinseco deve essere in grado di segnalare tale valore a un utente.</span><span class="sxs-lookup"><span data-stu-id="ba930-120">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because an element that has an intrinsic value must be able to report that value to a user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ba930-121">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="ba930-121">Possible causes</span></span>

<span data-ttu-id="ba930-122">Per l'elemento o per il relativo padre è impostato un ruolo MSAA in modo non appropriato.</span><span class="sxs-lookup"><span data-stu-id="ba930-122">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba930-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba930-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba930-124">**IAccessible:: Get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="ba930-124">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="ba930-125">**Ruoli oggetto**</span><span class="sxs-lookup"><span data-stu-id="ba930-125">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




