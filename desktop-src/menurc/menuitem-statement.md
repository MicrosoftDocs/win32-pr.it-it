---
title: MENUITEM (istruzione)
description: Definisce una voce di menu.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Menu di istruzioni MENUITEM e altre risorse
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2051b326b2f2f37c9e24e03bcb5e5116cf290a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299263"
---
# <a name="menuitem-statement"></a><span data-ttu-id="55f81-104">MENUITEM (istruzione)</span><span class="sxs-lookup"><span data-stu-id="55f81-104">MENUITEM statement</span></span>

<span data-ttu-id="55f81-105">Definisce una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="55f81-105">Defines a menu item.</span></span>

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span data-ttu-id="55f81-106"><span id="text"></span><span id="TEXT"></span>*testo*</span><span class="sxs-lookup"><span data-stu-id="55f81-106"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="55f81-107">Nome della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="55f81-107">The name of the menu item.</span></span>

<span data-ttu-id="55f81-108">La stringa può contenere i caratteri di escape **\\ t** e **\\ un oggetto**.</span><span class="sxs-lookup"><span data-stu-id="55f81-108">The string can contain the escape characters **\\t** and **\\a**.</span></span> <span data-ttu-id="55f81-109">Il carattere **\\ t** inserisce una scheda nella stringa e viene utilizzata per allineare il testo nelle colonne.</span><span class="sxs-lookup"><span data-stu-id="55f81-109">The **\\t** character inserts a tab in the string and is used to align text in columns.</span></span> <span data-ttu-id="55f81-110">I caratteri di tabulazione devono essere utilizzati solo nei menu, non nelle barre dei menu.</span><span class="sxs-lookup"><span data-stu-id="55f81-110">Tab characters should be used only in menus, not in menu bars.</span></span> <span data-ttu-id="55f81-111">Per informazioni sui menu, vedere [**risorsa popup**](popup-resource.md). Il carattere **\\ a** è allineato a tutto il testo che lo segue scaricando direttamente dalla barra dei menu o dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="55f81-111">(For information on menus, see [**POPUP Resource**](popup-resource.md).) The **\\a** character aligns all text that follows it flush right to the menu bar or pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="55f81-112"><span id="result"></span><span id="RESULT"></span>*risultato*</span><span class="sxs-lookup"><span data-stu-id="55f81-112"><span id="result"></span><span id="RESULT"></span>*result*</span></span>
</dt> <dd>

<span data-ttu-id="55f81-113">Numero che specifica il risultato generato quando l'utente seleziona la voce di menu.</span><span class="sxs-lookup"><span data-stu-id="55f81-113">A number that specifies the result generated when the user selects the menu item.</span></span> <span data-ttu-id="55f81-114">Questo parametro accetta un valore integer.</span><span class="sxs-lookup"><span data-stu-id="55f81-114">This parameter takes an integer value.</span></span> <span data-ttu-id="55f81-115">I risultati dei menu-item sono sempre numeri interi. Quando l'utente fa clic sul nome del menu-elemento, il risultato viene inviato alla finestra che possiede il menu.</span><span class="sxs-lookup"><span data-stu-id="55f81-115">Menu-item results are always integers; when the user clicks the menu-item name, the result is sent to the window that owns the menu.</span></span>

</dd> <dt>

<span data-ttu-id="55f81-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*opzione*</span><span class="sxs-lookup"><span data-stu-id="55f81-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="55f81-117">Aspetto della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="55f81-117">The appearance of the menu item.</span></span> <span data-ttu-id="55f81-118">Questo parametro facoltativo accetta una o più delle seguenti opzioni di menu ridefinite, separate da virgole o spazi.</span><span class="sxs-lookup"><span data-stu-id="55f81-118">This optional parameter takes one or more of the following redefined menu options, separated by commas or spaces.</span></span>



| <span data-ttu-id="55f81-119">Opzione</span><span class="sxs-lookup"><span data-stu-id="55f81-119">Option</span></span>           | <span data-ttu-id="55f81-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55f81-120">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55f81-121">**SELEZIONATA**</span><span class="sxs-lookup"><span data-stu-id="55f81-121">**CHECKED**</span></span>      | <span data-ttu-id="55f81-122">Accanto alla voce di menu è presente un segno di spunta.</span><span class="sxs-lookup"><span data-stu-id="55f81-122">Menu item has a check mark next to it.</span></span>                                                                                                                                |
| <span data-ttu-id="55f81-123">**IN grigio**</span><span class="sxs-lookup"><span data-stu-id="55f81-123">**GRAYED**</span></span>       | <span data-ttu-id="55f81-124">La voce di menu inizialmente è inattiva e viene visualizzata nel menu in grigio o in una sfumatura schiarita del colore del testo del menu.</span><span class="sxs-lookup"><span data-stu-id="55f81-124">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="55f81-125">Questa opzione non può essere usata con l'opzione **inactive** .</span><span class="sxs-lookup"><span data-stu-id="55f81-125">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="55f81-126">**Guida**</span><span class="sxs-lookup"><span data-stu-id="55f81-126">**HELP**</span></span>         | <span data-ttu-id="55f81-127">Identifica un elemento della guida.</span><span class="sxs-lookup"><span data-stu-id="55f81-127">Identifies a help item.</span></span> <span data-ttu-id="55f81-128">Questa opzione non ha alcun effetto sull'aspetto della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="55f81-128">This option has no effect on the appearance of the menu item.</span></span>                                                                                 |
| <span data-ttu-id="55f81-129">**INATTIVO**</span><span class="sxs-lookup"><span data-stu-id="55f81-129">**INACTIVE**</span></span>     | <span data-ttu-id="55f81-130">La voce di menu viene visualizzata, ma non è possibile selezionarla.</span><span class="sxs-lookup"><span data-stu-id="55f81-130">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="55f81-131">Questa opzione non può essere usata con l'opzione **grigio** .</span><span class="sxs-lookup"><span data-stu-id="55f81-131">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="55f81-132">**MENUBARBREAK**</span><span class="sxs-lookup"><span data-stu-id="55f81-132">**MENUBARBREAK**</span></span> | <span data-ttu-id="55f81-133">Analogamente a **MENUBREAK** , ad eccezione del fatto che per i menu popup, separa la nuova colonna dalla colonna precedente con una linea verticale.</span><span class="sxs-lookup"><span data-stu-id="55f81-133">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="55f81-134">**MENUBREAK**</span><span class="sxs-lookup"><span data-stu-id="55f81-134">**MENUBREAK**</span></span>    | <span data-ttu-id="55f81-135">Inserisce la voce di menu in una nuova riga per gli elementi statici della barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="55f81-135">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="55f81-136">Per i menu, inserisce la voce di menu in una nuova colonna senza linea di separazione tra le colonne.</span><span class="sxs-lookup"><span data-stu-id="55f81-136">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="55f81-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**SEPARATORE MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="55f81-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM SEPARATOR**</span></span>
</dt> <dd>

<span data-ttu-id="55f81-138">Il formato **separatore MenuItem** dell'istruzione **MenuItem** crea una voce di menu inattiva che funge da barra di divisione tra due voci di menu attive in un menu.</span><span class="sxs-lookup"><span data-stu-id="55f81-138">The **MENUITEM SEPARATOR** form of the **MENUITEM** statement creates an inactive menu item that serves as a dividing bar between two active menu items on a menu.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="55f81-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="55f81-139">Examples</span></span>

<span data-ttu-id="55f81-140">Nell'esempio seguente viene illustrato l'utilizzo delle istruzioni del **separatore** **MenuItem** e MenuItem:</span><span class="sxs-lookup"><span data-stu-id="55f81-140">The following example demonstrates the use of the **MENUITEM** and **MENUITEM SEPARATOR** statements:</span></span>

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a><span data-ttu-id="55f81-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55f81-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f81-142">**MENU**</span><span class="sxs-lookup"><span data-stu-id="55f81-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="55f81-143">**POPUP**</span><span class="sxs-lookup"><span data-stu-id="55f81-143">**POPUP**</span></span>](popup-resource.md)
</dt> </dl>

 

 




