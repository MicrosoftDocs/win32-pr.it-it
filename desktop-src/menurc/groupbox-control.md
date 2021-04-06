---
title: Controllo GROUPBOX (menu e altre risorse)
description: Definisce un controllo casella di gruppo. Il controllo è un rettangolo che raggruppa altri controlli. I controlli sono raggruppati disegnando un bordo intorno a essi e visualizzando il testo specificato nell'angolo superiore sinistro.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Menu di controllo GROUPBOX e altre risorse
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104046053"
---
# <a name="groupbox-control"></a><span data-ttu-id="19d0d-106">Controllo GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="19d0d-106">GROUPBOX control</span></span>

<span data-ttu-id="19d0d-107">Definisce un controllo casella di gruppo.</span><span class="sxs-lookup"><span data-stu-id="19d0d-107">Defines a group box control.</span></span> <span data-ttu-id="19d0d-108">Il controllo è un rettangolo che raggruppa altri controlli.</span><span class="sxs-lookup"><span data-stu-id="19d0d-108">The control is a rectangle that groups other controls together.</span></span> <span data-ttu-id="19d0d-109">I controlli sono raggruppati disegnando un bordo intorno a essi e visualizzando il testo specificato nell'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="19d0d-109">The controls are grouped by drawing a border around them and displaying the given text in the upper-left corner.</span></span>

<span data-ttu-id="19d0d-110">L'istruzione **GroupBox** , che può essere utilizzata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) , definisce il testo, l'identificatore, le dimensioni e gli attributi di una finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="19d0d-110">The **GROUPBOX** statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="19d0d-111"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="19d0d-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="19d0d-112">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="19d0d-112">Control styles.</span></span> <span data-ttu-id="19d0d-113">Questo valore può essere una combinazione dello stile della classe Button **BS \_ GroupBox** e degli stili **WS \_ TABSTOP** e **WS \_ disabled** .</span><span class="sxs-lookup"><span data-stu-id="19d0d-113">This value can be a combination of the button class style **BS\_GROUPBOX** and the **WS\_TABSTOP** and **WS\_DISABLED** styles.</span></span>

<span data-ttu-id="19d0d-114">Se non si specifica uno stile, lo stile predefinito è **BS \_ GroupBox**.</span><span class="sxs-lookup"><span data-stu-id="19d0d-114">If you do not specify a style, the default style is **BS\_GROUPBOX**.</span></span>

</dd> </dl>

<span data-ttu-id="19d0d-115">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="19d0d-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="19d0d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="19d0d-116">Remarks</span></span>

<span data-ttu-id="19d0d-117">Quando lo stile contiene **WS \_ TABSTOP** o il testo specifica un tasto di scelta rapida, la tabulazione o la pressione del tasto di scelta rapida Sposta lo stato attivo sul primo controllo all'interno del gruppo.</span><span class="sxs-lookup"><span data-stu-id="19d0d-117">When the style contains **WS\_TABSTOP** or the text specifies an accelerator, tabbing or pressing the accelerator key moves the focus to the first control within the group.</span></span>

## <a name="examples"></a><span data-ttu-id="19d0d-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="19d0d-118">Examples</span></span>

<span data-ttu-id="19d0d-119">Questo esempio definisce un controllo casella di gruppo con etichetta opzioni:</span><span class="sxs-lookup"><span data-stu-id="19d0d-119">This example defines a group-box control that is labeled Options:</span></span>

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="19d0d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19d0d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d0d-121">Caselle di gruppo</span><span class="sxs-lookup"><span data-stu-id="19d0d-121">Group Boxes</span></span>](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




