---
title: Proprietà Value
description: La proprietà Value fornisce una rappresentazione testuale delle informazioni visive contenute in un oggetto. Non tutti gli oggetti supportano la proprietà Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330223"
---
# <a name="value-property"></a><span data-ttu-id="44a95-104">Proprietà Value</span><span class="sxs-lookup"><span data-stu-id="44a95-104">Value Property</span></span>

<span data-ttu-id="44a95-105">La proprietà **value** fornisce una rappresentazione testuale delle informazioni visive contenute in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="44a95-105">The **Value** property provides a textual representation of the visual information contained in an object.</span></span> <span data-ttu-id="44a95-106">Non tutti gli oggetti supportano la proprietà **value** .</span><span class="sxs-lookup"><span data-stu-id="44a95-106">Not all objects support the **Value** property.</span></span>

<span data-ttu-id="44a95-107">La proprietà **value** viene recuperata chiamando [**IAccessible:: Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span><span class="sxs-lookup"><span data-stu-id="44a95-107">The **Value** property is retrieved by calling [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="44a95-108">La proprietà **value** indica al client le informazioni visive contenute in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="44a95-108">The **Value** property tells the client about the visual information contained in an object.</span></span> <span data-ttu-id="44a95-109">Ad esempio, il valore di un controllo di modifica è il testo che contiene, mentre una voce di menu non contiene alcun valore.</span><span class="sxs-lookup"><span data-stu-id="44a95-109">For example, an edit control's value is the text it contains, whereas a menu item has no value.</span></span>

## <a name="providing-hierarchical-information"></a><span data-ttu-id="44a95-110">Fornire informazioni gerarchiche</span><span class="sxs-lookup"><span data-stu-id="44a95-110">Providing Hierarchical Information</span></span>

<span data-ttu-id="44a95-111">La proprietà **value** fornisce informazioni gerarchiche nei casi, ad esempio un controllo di visualizzazione ad albero.</span><span class="sxs-lookup"><span data-stu-id="44a95-111">The **Value** property provides hierarchical information in cases such as a tree view control.</span></span> <span data-ttu-id="44a95-112">Sebbene l'oggetto padre nel controllo di visualizzazione albero non fornisca informazioni nella proprietà **value** , ogni elemento all'interno del controllo ha un valore in base zero che rappresenta il livello all'interno della gerarchia.</span><span class="sxs-lookup"><span data-stu-id="44a95-112">Although the parent object in the tree view control does not provide information in the **Value** property, each item within the control has a zero-based value that represents its level within the hierarchy.</span></span> <span data-ttu-id="44a95-113">Gli elementi di primo livello hanno un valore pari a zero, gli elementi di secondo livello hanno un valore pari a uno e così via.</span><span class="sxs-lookup"><span data-stu-id="44a95-113">Top-level items have a value of zero, second-level items have a value of one, and so on.</span></span>

 

 




