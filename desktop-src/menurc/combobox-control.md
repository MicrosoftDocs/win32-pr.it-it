---
title: Controllo COMBOBOX (menu e altre risorse)
description: Definisce un controllo casella combinata (casella combinata).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menu di controllo COMBOBOX e altre risorse
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398917"
---
# <a name="combobox-control"></a><span data-ttu-id="25a05-104">Controllo COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="25a05-104">COMBOBOX control</span></span>

<span data-ttu-id="25a05-105">Definisce un controllo casella combinata (casella combinata).</span><span class="sxs-lookup"><span data-stu-id="25a05-105">Defines a combination box control (a combo box).</span></span> <span data-ttu-id="25a05-106">Una casella combinata è costituita da una casella di testo statica o da una casella di modifica combinata con una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="25a05-106">A combo box consists of either a static text box or an edit box combined with a list box.</span></span> <span data-ttu-id="25a05-107">La casella di riepilogo può essere visualizzata sempre o spostata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="25a05-107">The list box can be displayed at all times or pulled down by the user.</span></span> <span data-ttu-id="25a05-108">Se la casella combinata contiene una casella di testo statica, nella casella di testo viene sempre visualizzata la selezione, se presente, nella casella combinata della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="25a05-108">If the combo box contains a static text box, the text box always displays the selection (if any) in the list box portion of the combo box.</span></span> <span data-ttu-id="25a05-109">Se usa una casella di modifica, l'utente può digitare la selezione desiderata; nella casella di riepilogo viene evidenziato il primo elemento, se presente, che corrisponde a quello immesso dall'utente nella casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="25a05-109">If it uses an edit box, the user can type in the desired selection; the list box highlights the first item (if any) that matches what the user has entered in the edit box.</span></span> <span data-ttu-id="25a05-110">L'utente può quindi selezionare l'elemento evidenziato nella casella di riepilogo per completare la scelta.</span><span class="sxs-lookup"><span data-stu-id="25a05-110">The user can then select the item highlighted in the list box to complete the choice.</span></span> <span data-ttu-id="25a05-111">Inoltre, la casella combinata può essere disegnata dal proprietario e di altezza fissa o variabile.</span><span class="sxs-lookup"><span data-stu-id="25a05-111">In addition, the combo box can be owner-drawn and of fixed or variable height.</span></span>

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="25a05-112"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="25a05-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="25a05-113">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="25a05-113">Control styles.</span></span> <span data-ttu-id="25a05-114">Questo valore può essere una combinazione degli stili della classe COMBOBOX e di uno degli stili seguenti: **WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL** e **WS \_ disabled**.</span><span class="sxs-lookup"><span data-stu-id="25a05-114">This value can be a combination of the COMBOBOX class styles and any of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="25a05-115">Se non si specifica uno stile, lo stile predefinito è `CBS_SIMPLE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="25a05-115">If you do not specify a style, the default style is `CBS_SIMPLE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="25a05-116">Il parametro *Height* si applica all'altezza di una casella combinata con un elenco a discesa completamente espanso.</span><span class="sxs-lookup"><span data-stu-id="25a05-116">The *height* parameter applies to the height of a combo box with a drop-down list fully expanded.</span></span>

<span data-ttu-id="25a05-117">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="25a05-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="25a05-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="25a05-118">Examples</span></span>

<span data-ttu-id="25a05-119">Questo esempio definisce un controllo casella combinata con una barra di scorrimento verticale:</span><span class="sxs-lookup"><span data-stu-id="25a05-119">This example defines a combo-box control with a vertical scroll bar:</span></span>

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a><span data-ttu-id="25a05-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25a05-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25a05-121">Caselle combinate</span><span class="sxs-lookup"><span data-stu-id="25a05-121">Combo Boxes</span></span>](../controls/about-combo-boxes.md)
</dt> </dl>

 

 