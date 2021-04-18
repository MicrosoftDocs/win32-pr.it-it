---
title: Risorsa MENUEX
description: Definisce il contenuto di una risorsa di menu. | Risorsa MENUEX
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menu risorse MENUEX e altre risorse
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321825"
---
# <a name="menuex-resource"></a><span data-ttu-id="b3e7c-105">Risorsa MENUEX</span><span class="sxs-lookup"><span data-stu-id="b3e7c-105">MENUEX resource</span></span>

<span data-ttu-id="b3e7c-106">Definisce il contenuto di una risorsa di menu.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="b3e7c-107">Una risorsa di menu è una raccolta di informazioni che definiscono l'aspetto e la funzione di un menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="b3e7c-108">Un menu è uno strumento di input speciale che consente a un utente di selezionare i comandi e aprire sottomenu da un elenco di voci di menu.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span> <span data-ttu-id="b3e7c-109">Definisce inoltre quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b3e7c-109">It also defines the following:</span></span>

-   <span data-ttu-id="b3e7c-110">Identificatori della guida nei menu.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-110">Help identifiers on menus.</span></span>
-   <span data-ttu-id="b3e7c-111">Identificatori nei menu.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-111">Identifiers on menus.</span></span>
-   <span data-ttu-id="b3e7c-112">Usare i flag di tipo **MFT \_ \** _ e i flag di stato _*MFS \_ \*\*_ .</span><span class="sxs-lookup"><span data-stu-id="b3e7c-112">Use of the **MFT\_\** _ type flags and _*MFS\_\*\*_ state flags.</span></span> <span data-ttu-id="b3e7c-113">Per ulteriori informazioni su questi flag, vedere la struttura [_ *MENUITEMINFO* \*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="b3e7c-113">For more information on these flags, see the [_ *MENUITEMINFO*\*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a><span data-ttu-id="b3e7c-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3e7c-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3e7c-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span><span class="sxs-lookup"><span data-stu-id="b3e7c-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-116">Definisce una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-116">Defines a menu item.</span></span>

<dl> <dt>

<span data-ttu-id="b3e7c-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span><span class="sxs-lookup"><span data-stu-id="b3e7c-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-118">Stringa contenente il testo per la voce di menu.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-118">String containing the text for the menu item.</span></span> <span data-ttu-id="b3e7c-119">Per ulteriori informazioni, vedere [**MenuItem**](menuitem-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b3e7c-119">For more information, see [**MENUITEM**](menuitem-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3e7c-120"><span id="id"></span><span id="ID"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="b3e7c-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-121">Espressione numerica che indica l'identificatore della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-121">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="b3e7c-122"><span id="type"></span><span id="TYPE"></span>*tipo*</span><span class="sxs-lookup"><span data-stu-id="b3e7c-122"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-123">Espressione numerica che indica il tipo di voce di menu per usare i valori di tipo MFT predefiniti \_ \* , includere l'istruzione seguente nel file RC:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="b3e7c-123">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="b3e7c-124"><span id="state"></span><span id="STATE"></span>*stato*</span><span class="sxs-lookup"><span data-stu-id="b3e7c-124"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-125">Espressione numerica che indica lo stato della voce di menu per usare i valori di stato MFS predefiniti \_ \* , includere l'istruzione seguente in. File RC:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="b3e7c-125">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b3e7c-126"><span id="POPUP"></span><span id="popup"></span>[**POPUP**](popup-resource.md)</span><span class="sxs-lookup"><span data-stu-id="b3e7c-126"><span id="POPUP"></span><span id="popup"></span>[**POPUP**](popup-resource.md)</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-127">Definisce una voce di menu a cui è associato un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-127">Defines a menu item that has a submenu associated with it.</span></span>

<dl> <dt>

<span data-ttu-id="b3e7c-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span><span class="sxs-lookup"><span data-stu-id="b3e7c-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-129">Stringa contenente il testo per la voce di menu.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-129">String containing the text for the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="b3e7c-130"><span id="id"></span><span id="ID"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="b3e7c-130"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-131">Espressione numerica che indica l'identificatore della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-131">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="b3e7c-132"><span id="type"></span><span id="TYPE"></span>*tipo*</span><span class="sxs-lookup"><span data-stu-id="b3e7c-132"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-133">Espressione numerica che indica il tipo di voce di menu per usare i valori di tipo MFT predefiniti \_ \* , includere l'istruzione seguente in. File RC:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="b3e7c-133">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="b3e7c-134"><span id="state"></span><span id="STATE"></span>*stato*</span><span class="sxs-lookup"><span data-stu-id="b3e7c-134"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-135">Espressione numerica che indica lo stato della voce di menu per usare i valori di stato MFS predefiniti \_ \* , includere l'istruzione seguente nel file RC:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="b3e7c-135">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="b3e7c-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span><span class="sxs-lookup"><span data-stu-id="b3e7c-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-137">Espressione numerica che indica l'identificatore usato per identificare il menu durante l'elaborazione della [**\_ Guida WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="b3e7c-137">Numeric expression indicating the identifier used to identify the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b3e7c-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span><span class="sxs-lookup"><span data-stu-id="b3e7c-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span></span>
</dt> <dd>

<span data-ttu-id="b3e7c-139">Contiene qualsiasi combinazione di istruzioni [**MenuItem**](menuitem-statement.md) e [**popup**](popup-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="b3e7c-139">Contains any combination of the [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statements.</span></span>

</dd> </dl>

<span data-ttu-id="b3e7c-140">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b3e7c-140">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="b3e7c-141">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b3e7c-141">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3e7c-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3e7c-142">Remarks</span></span>

<span data-ttu-id="b3e7c-143">Le operazioni aritmetiche e booleane valide che possono essere contenute in qualsiasi espressione numerica nelle istruzioni di **menuex** sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3e7c-143">The valid arithmetic and Boolean operations that can be contained in any of the numeric expressions in the statements of **MENUEX** are as follows:</span></span>

-   <span data-ttu-id="b3e7c-144">Aggiungi (' +')</span><span class="sxs-lookup"><span data-stu-id="b3e7c-144">Add ('+')</span></span>
-   <span data-ttu-id="b3e7c-145">Subtract ('-')</span><span class="sxs-lookup"><span data-stu-id="b3e7c-145">Subtract ('-')</span></span>
-   <span data-ttu-id="b3e7c-146">Meno unario ('-')</span><span class="sxs-lookup"><span data-stu-id="b3e7c-146">Unary minus ('-')</span></span>
-   <span data-ttu-id="b3e7c-147">NOT unario (' ~')</span><span class="sxs-lookup"><span data-stu-id="b3e7c-147">Unary NOT ('~')</span></span>
-   <span data-ttu-id="b3e7c-148">E (' &')</span><span class="sxs-lookup"><span data-stu-id="b3e7c-148">AND ('&')</span></span>
-   <span data-ttu-id="b3e7c-149">O (' \| ')</span><span class="sxs-lookup"><span data-stu-id="b3e7c-149">OR ('\|')</span></span>

## <a name="see-also"></a><span data-ttu-id="b3e7c-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3e7c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e7c-151">Uso di menu</span><span class="sxs-lookup"><span data-stu-id="b3e7c-151">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="b3e7c-152">**ACCELERATORI**</span><span class="sxs-lookup"><span data-stu-id="b3e7c-152">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="b3e7c-153">**CARATTERISTICHE**</span><span class="sxs-lookup"><span data-stu-id="b3e7c-153">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="b3e7c-154">**DIALOGO**</span><span class="sxs-lookup"><span data-stu-id="b3e7c-154">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="b3e7c-155">**LINGUAGGIO**</span><span class="sxs-lookup"><span data-stu-id="b3e7c-155">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="b3e7c-156">**MENU**</span><span class="sxs-lookup"><span data-stu-id="b3e7c-156">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="b3e7c-157">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="b3e7c-157">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="b3e7c-158">**POPUP**</span><span class="sxs-lookup"><span data-stu-id="b3e7c-158">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="b3e7c-159">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="b3e7c-159">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="b3e7c-160">**UN'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="b3e7c-160">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="b3e7c-161">**Versione**</span><span class="sxs-lookup"><span data-stu-id="b3e7c-161">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
