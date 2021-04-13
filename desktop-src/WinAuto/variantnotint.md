---
title: VariantNotInt (CheckRole)
description: VariantNotInt (CheckRole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330220"
---
# <a name="variantnotint-checkrole"></a><span data-ttu-id="04120-103">VariantNotInt (CheckRole)</span><span class="sxs-lookup"><span data-stu-id="04120-103">VariantNotInt (CheckRole)</span></span>

## <a name="text"></a><span data-ttu-id="04120-104">Testo</span><span class="sxs-lookup"><span data-stu-id="04120-104">Text</span></span>

<span data-ttu-id="04120-105">La variante restituita da {0} deve essere un oggetto {1} , ma è un oggetto {2} .</span><span class="sxs-lookup"><span data-stu-id="04120-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="04120-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="04120-106">Type</span></span>

<span data-ttu-id="04120-107">Errore</span><span class="sxs-lookup"><span data-stu-id="04120-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="04120-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04120-108">Description</span></span>

<span data-ttu-id="04120-109">Un elemento segnala un ruolo MSAA non valido.</span><span class="sxs-lookup"><span data-stu-id="04120-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="04120-110">Ad esempio, il metodo [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) usato per recuperare il ruolo MSAA di un elemento deve restituire un valore integer che rappresenta una delle costanti del ruolo MSAA, ma restituisce invece un'altra variante.</span><span class="sxs-lookup"><span data-stu-id="04120-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method used to retrieve the MSAA role of an element should return an integer value that represents one of the MSAA role constants, but is returning another variant instead.</span></span>

<span data-ttu-id="04120-111">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché gli elementi potrebbero essere identificati erroneamente dall'utente.</span><span class="sxs-lookup"><span data-stu-id="04120-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="04120-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="04120-112">Possible causes</span></span>

<span data-ttu-id="04120-113">Per l'elemento o per il relativo padre è impostato un ruolo MSAA in modo non appropriato.</span><span class="sxs-lookup"><span data-stu-id="04120-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04120-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04120-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04120-115">**IAccessible:: Get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="04120-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="04120-116">**Ruoli oggetto**</span><span class="sxs-lookup"><span data-stu-id="04120-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




