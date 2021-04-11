---
title: Risorsa POPUP
description: Definisce una voce di menu che può contenere voci di menu e sottomenu.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- Menu delle risorse POPUP e altre risorse
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c7a1af3bd8ed9aae8908aa7ff926a3f4799ee5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117061"
---
# <a name="popup-resource"></a><span data-ttu-id="3ec28-104">Risorsa POPUP</span><span class="sxs-lookup"><span data-stu-id="3ec28-104">POPUP resource</span></span>

<span data-ttu-id="3ec28-105">Definisce una voce di menu che può contenere voci di menu e sottomenu.</span><span class="sxs-lookup"><span data-stu-id="3ec28-105">Defines a menu item that can contain menu items and submenus.</span></span>

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a><span data-ttu-id="3ec28-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ec28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ec28-107"><span id="text"></span><span id="TEXT"></span>*testo*</span><span class="sxs-lookup"><span data-stu-id="3ec28-107"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="3ec28-108">Stringa che contiene il nome del menu.</span><span class="sxs-lookup"><span data-stu-id="3ec28-108">String that contains the name of the menu.</span></span> <span data-ttu-id="3ec28-109">Questa stringa deve essere racchiusa tra virgolette doppie (**"**).</span><span class="sxs-lookup"><span data-stu-id="3ec28-109">This string must be enclosed in double quotation marks (**"**).</span></span>

</dd> <dt>

<span data-ttu-id="3ec28-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*opzione*</span><span class="sxs-lookup"><span data-stu-id="3ec28-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="3ec28-111">Questo parametro specifica le opzioni di menu ridefinite che specificano l'aspetto della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="3ec28-111">This parameter specifies redefined menu options that specify the appearance of the menu item.</span></span> <span data-ttu-id="3ec28-112">Questo parametro facoltativo può essere uno o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3ec28-112">This optional parameter can be one or more of the following.</span></span>



| <span data-ttu-id="3ec28-113">Opzione</span><span class="sxs-lookup"><span data-stu-id="3ec28-113">Option</span></span>           | <span data-ttu-id="3ec28-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ec28-114">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec28-115">**SELEZIONATA**</span><span class="sxs-lookup"><span data-stu-id="3ec28-115">**CHECKED**</span></span>      | <span data-ttu-id="3ec28-116">Accanto alla voce di menu è presente un segno di spunta.</span><span class="sxs-lookup"><span data-stu-id="3ec28-116">Menu item has a check mark next to it.</span></span> <span data-ttu-id="3ec28-117">Questa opzione non è valida per un menu di primo livello.</span><span class="sxs-lookup"><span data-stu-id="3ec28-117">This option is not valid for a top-level menu.</span></span>                                                                                 |
| <span data-ttu-id="3ec28-118">**IN grigio**</span><span class="sxs-lookup"><span data-stu-id="3ec28-118">**GRAYED**</span></span>       | <span data-ttu-id="3ec28-119">La voce di menu inizialmente è inattiva e viene visualizzata nel menu in grigio o in una sfumatura schiarita del colore del testo del menu.</span><span class="sxs-lookup"><span data-stu-id="3ec28-119">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="3ec28-120">Questa opzione non può essere usata con l'opzione **inactive** .</span><span class="sxs-lookup"><span data-stu-id="3ec28-120">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="3ec28-121">**Guida**</span><span class="sxs-lookup"><span data-stu-id="3ec28-121">**HELP**</span></span>         | <span data-ttu-id="3ec28-122">Identifica un elemento della guida.</span><span class="sxs-lookup"><span data-stu-id="3ec28-122">Identifies a help item.</span></span> <span data-ttu-id="3ec28-123">La voce di menu è posizionata in corrispondenza della posizione più a destra nella barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="3ec28-123">The menu item is place at the right-most position on the menu bar.</span></span>                                                                            |
| <span data-ttu-id="3ec28-124">**INATTIVO**</span><span class="sxs-lookup"><span data-stu-id="3ec28-124">**INACTIVE**</span></span>     | <span data-ttu-id="3ec28-125">La voce di menu viene visualizzata, ma non è possibile selezionarla.</span><span class="sxs-lookup"><span data-stu-id="3ec28-125">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="3ec28-126">Questa opzione non può essere usata con l'opzione **grigio** .</span><span class="sxs-lookup"><span data-stu-id="3ec28-126">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="3ec28-127">**MENUBARBREAK**</span><span class="sxs-lookup"><span data-stu-id="3ec28-127">**MENUBARBREAK**</span></span> | <span data-ttu-id="3ec28-128">Analogamente a **MENUBREAK** , ad eccezione del fatto che per i menu popup, separa la nuova colonna dalla colonna precedente con una linea verticale.</span><span class="sxs-lookup"><span data-stu-id="3ec28-128">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="3ec28-129">**MENUBREAK**</span><span class="sxs-lookup"><span data-stu-id="3ec28-129">**MENUBREAK**</span></span>    | <span data-ttu-id="3ec28-130">Inserisce la voce di menu in una nuova riga per gli elementi statici della barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="3ec28-130">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="3ec28-131">Per i menu, inserisce la voce di menu in una nuova colonna senza linea di separazione tra le colonne.</span><span class="sxs-lookup"><span data-stu-id="3ec28-131">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> </dl>

<span data-ttu-id="3ec28-132">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="3ec28-132">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="3ec28-133">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="3ec28-133">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3ec28-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="3ec28-134">Examples</span></span>

<span data-ttu-id="3ec28-135">Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **popup** :</span><span class="sxs-lookup"><span data-stu-id="3ec28-135">The following example demonstrates the use of the **POPUP** statement:</span></span>

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3ec28-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ec28-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec28-137">**MENU**</span><span class="sxs-lookup"><span data-stu-id="3ec28-137">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="3ec28-138">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="3ec28-138">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> </dl>

 

 




