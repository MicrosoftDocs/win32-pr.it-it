---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221441"
---
# <a name="variantnotint-checkstate"></a><span data-ttu-id="49f16-103">VariantNotInt (CheckState)</span><span class="sxs-lookup"><span data-stu-id="49f16-103">VariantNotInt (CheckState)</span></span>

## <a name="text"></a><span data-ttu-id="49f16-104">Testo</span><span class="sxs-lookup"><span data-stu-id="49f16-104">Text</span></span>

<span data-ttu-id="49f16-105">La variante restituita da {0} deve essere un oggetto {1} , ma è un oggetto {2} .</span><span class="sxs-lookup"><span data-stu-id="49f16-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="49f16-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="49f16-106">Type</span></span>

<span data-ttu-id="49f16-107">Errore</span><span class="sxs-lookup"><span data-stu-id="49f16-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="49f16-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49f16-108">Description</span></span>

<span data-ttu-id="49f16-109">Un elemento segnala uno stato MSAA non valido.</span><span class="sxs-lookup"><span data-stu-id="49f16-109">An element is reporting an invalid MSAA state.</span></span> <span data-ttu-id="49f16-110">Ad esempio, il metodo [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) usato per recuperare lo stato MSAA di un elemento deve restituire un valore integer che rappresenta una delle costanti di stato MSAA, ma restituisce invece un'altra variante.</span><span class="sxs-lookup"><span data-stu-id="49f16-110">For example, the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method used to retrieve the MSAA state of an element should return an integer value that represents one of the MSAA state constants, but is returning another variant instead.</span></span>

<span data-ttu-id="49f16-111">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché uno stato dell'elemento errato potrebbe essere segnalato all'utente.</span><span class="sxs-lookup"><span data-stu-id="49f16-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="49f16-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="49f16-112">Possible causes</span></span>

<span data-ttu-id="49f16-113">L'elemento o il relativo padre hanno uno stato MSAA impostato in modo non appropriato.</span><span class="sxs-lookup"><span data-stu-id="49f16-113">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49f16-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49f16-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49f16-115">**IAccessible:: Get \_ accState**</span><span class="sxs-lookup"><span data-stu-id="49f16-115">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="49f16-116">**Costanti di stato dell'oggetto**</span><span class="sxs-lookup"><span data-stu-id="49f16-116">**Object State Constants**</span></span>](object-state-constants.md)
</dt> </dl>

 

 




