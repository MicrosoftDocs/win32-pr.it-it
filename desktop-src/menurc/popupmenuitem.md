---
title: Struttura POPUPMENUITEM
description: Contiene informazioni sulle voci di menu in una risorsa di menu che aprono un menu o un sottomenu. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Menu struttura POPUPMENUITEM e altre risorse
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963894"
---
# <a name="popupmenuitem-structure"></a><span data-ttu-id="6de1f-105">Struttura POPUPMENUITEM</span><span class="sxs-lookup"><span data-stu-id="6de1f-105">POPUPMENUITEM structure</span></span>

<span data-ttu-id="6de1f-106">Contiene informazioni sulle voci di menu in una risorsa di menu che aprono un menu o un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="6de1f-106">Contains information about the menu items in a menu resource that open a menu or a submenu.</span></span> <span data-ttu-id="6de1f-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="6de1f-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de1f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6de1f-108">Syntax</span></span>


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a><span data-ttu-id="6de1f-109">Members</span><span class="sxs-lookup"><span data-stu-id="6de1f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6de1f-110">**type**</span><span class="sxs-lookup"><span data-stu-id="6de1f-110">**type**</span></span>
</dt> <dd>

<span data-ttu-id="6de1f-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6de1f-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6de1f-112">Descrive la voce di menu.</span><span class="sxs-lookup"><span data-stu-id="6de1f-112">Describes the menu item.</span></span> <span data-ttu-id="6de1f-113">Alcuni dei valori che questo membro può avere includono quelli mostrati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="6de1f-113">Some of the values this member can have include those shown in the list below.</span></span>

<span data-ttu-id="6de1f-114">Oltre ai valori indicati, questo membro può anche essere una combinazione dei valori di tipo elencati con il membro **ftype** della struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="6de1f-114">In addition to the values shown, this member can also be a combination of the type values listed with the **fType** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="6de1f-115">I valori del tipo sono quelli che iniziano con MFT \_ .</span><span class="sxs-lookup"><span data-stu-id="6de1f-115">The type values are those that begin with MFT\_.</span></span> <span data-ttu-id="6de1f-116">Per usare questi valori di tipo MFT predefiniti \_ \* , includere l'istruzione seguente nel file RC:</span><span class="sxs-lookup"><span data-stu-id="6de1f-116">To use these predefined MFT\_\* type values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`



| <span data-ttu-id="6de1f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6de1f-117">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="6de1f-118">Significato</span><span class="sxs-lookup"><span data-stu-id="6de1f-118">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <span data-ttu-id="6de1f-119"><dt>**MF \_ FINE**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="6de1f-119"><dt>**MF\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="6de1f-120">La voce di menu è l'ultima nel menu; il flag viene utilizzato internamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6de1f-120">The menu item is the last on the menu; the flag is used internally by the system.</span></span> <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="6de1f-121"><dt>**MF \_ POPUP**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="6de1f-121"><dt>**MF\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="6de1f-122">La voce di menu apre un menu o un sottomenu; il flag viene utilizzato internamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6de1f-122">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="6de1f-123">**state**</span><span class="sxs-lookup"><span data-stu-id="6de1f-123">**state**</span></span>
</dt> <dd>

<span data-ttu-id="6de1f-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6de1f-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6de1f-125">Descrive la voce di menu.</span><span class="sxs-lookup"><span data-stu-id="6de1f-125">Describes the menu item.</span></span> <span data-ttu-id="6de1f-126">Questo membro può essere una combinazione dei valori di stato elencati con il membro **dwState** della struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="6de1f-126">This member can be a combination of the state values listed with the **dwState** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="6de1f-127">I valori di stato sono quelli che iniziano con MFS \_ .</span><span class="sxs-lookup"><span data-stu-id="6de1f-127">The state values are those that begin with MFS\_.</span></span> <span data-ttu-id="6de1f-128">Per usare questi valori di stato MFS predefiniti \_ \* , includere l'istruzione seguente nel file RC:</span><span class="sxs-lookup"><span data-stu-id="6de1f-128">To use these predefined MFS\_\* state values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`

</dd> <dt>

<span data-ttu-id="6de1f-129">**id**</span><span class="sxs-lookup"><span data-stu-id="6de1f-129">**id**</span></span>
</dt> <dd>

<span data-ttu-id="6de1f-130">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6de1f-130">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6de1f-131">Espressione numerica che identifica la voce di menu passata nel messaggio del [**\_ comando WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="6de1f-131">A numeric expression that identifies the menu item that is passed in the [**WM\_COMMAND**](wm-command.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6de1f-132">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="6de1f-132">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="6de1f-133">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="6de1f-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6de1f-134">Set di flag di bit che specificano il tipo di voce di menu.</span><span class="sxs-lookup"><span data-stu-id="6de1f-134">A set of bit flags that specify the type of menu item.</span></span> <span data-ttu-id="6de1f-135">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6de1f-135">This member can be one of the following values.</span></span>



| <span data-ttu-id="6de1f-136">Valore</span><span class="sxs-lookup"><span data-stu-id="6de1f-136">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="6de1f-137">Significato</span><span class="sxs-lookup"><span data-stu-id="6de1f-137">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="6de1f-138"><dt>**Fabbisogno \_ di FINE**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="6de1f-138"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="6de1f-139">La voce di menu è l'ultima in questo sottomenu o risorsa di menu; Questo flag viene utilizzato internamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6de1f-139">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="6de1f-140"><dt>**Fabbisogno \_ di POPUP**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="6de1f-140"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="6de1f-141">La voce di menu apre un menu o un sottomenu; il flag viene utilizzato internamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6de1f-141">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="6de1f-142">**menuText**</span><span class="sxs-lookup"><span data-stu-id="6de1f-142">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="6de1f-143">Tipo: **szOrOrd**</span><span class="sxs-lookup"><span data-stu-id="6de1f-143">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="6de1f-144">Stringa Unicode con terminazione null che contiene il testo di questa voce di menu.</span><span class="sxs-lookup"><span data-stu-id="6de1f-144">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="6de1f-145">Non esiste un limite fisso per le dimensioni di questa stringa.</span><span class="sxs-lookup"><span data-stu-id="6de1f-145">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6de1f-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="6de1f-146">Remarks</span></span>

<span data-ttu-id="6de1f-147">Esiste una struttura **POPUPMENUITEM** per ogni voce di menu che apre un menu o un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="6de1f-147">There is one **POPUPMENUITEM** structure for each menu item that opens a menu or a submenu.</span></span> <span data-ttu-id="6de1f-148">Identificare questo tipo di voce di menu impostando il membro del **tipo** su **MF \_ popup** e impostando il bit del **\_ popup fabbisogno** nel membro **resInfo** su 0x0001.</span><span class="sxs-lookup"><span data-stu-id="6de1f-148">Identify this type of menu item by setting the **type** member to **MF\_POPUP** and by setting the **MFR\_POPUP** bit in the **resInfo** member to 0x0001.</span></span> <span data-ttu-id="6de1f-149">In questo caso, i dati finali scritti nella risorsa [**di \_ menu RT**](/windows/desktop/menurc/resource-types) per il menu o il sottomenu sono la struttura [**MENUHELPID**](menuhelpid.md) .</span><span class="sxs-lookup"><span data-stu-id="6de1f-149">In this case, the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for the menu or submenu is the [**MENUHELPID**](menuhelpid.md) structure.</span></span> <span data-ttu-id="6de1f-150">**MENUHELPID** contiene un'espressione numerica che identifica il menu durante l'elaborazione della [**\_ Guida WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="6de1f-150">**MENUHELPID** contains a numeric expression that identifies the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

<span data-ttu-id="6de1f-151">Inoltre, ogni struttura **POPUPMENUITEM** che ha il **bit \_ popup di fabbisogno** impostato nel membro **ResInfo** sarà seguita da una struttura [**MENUHELPID**](menuhelpid.md) più un numero aggiuntivo di strutture **POPUPMENUITEM** , una per ogni voce di menu in quel sottomenu.</span><span class="sxs-lookup"><span data-stu-id="6de1f-151">Additionally, every **POPUPMENUITEM** structure that has the **MFR\_POPUP** bit set in the **resInfo** member will be followed by a [**MENUHELPID**](menuhelpid.md) structure plus an additional number of **POPUPMENUITEM** structures, one for each menu item in that submenu.</span></span> <span data-ttu-id="6de1f-152">L'ultima struttura **POPUPMENUITEM** nel sottomenu avrà il bit **\_ finale di fabbisogno** impostato nel membro **resInfo** .</span><span class="sxs-lookup"><span data-stu-id="6de1f-152">The last **POPUPMENUITEM** structure in the submenu will have the **MFR\_END** bit set in the **resInfo** member.</span></span> <span data-ttu-id="6de1f-153">Per trovare la fine della risorsa, cercare un termine di un **fabbisogno \_** di base corrispondente per ogni **\_ popup di fabbisogno** , oltre a un' **\_ estremità ulteriore di fabbisogno** che corrisponda al set più esterno di voci di menu.</span><span class="sxs-lookup"><span data-stu-id="6de1f-153">To find the end of the resource, look for a matching **MFR\_END** for every **MFR\_POPUP** plus one additional **MFR\_END** that matches the outermost set of menu items.</span></span>

<span data-ttu-id="6de1f-154">Indica l'ultima voce di menu impostando il membro del **tipo** su **MF \_ end**.</span><span class="sxs-lookup"><span data-stu-id="6de1f-154">Indicate the last menu item by setting the **type** member to **MF\_END**.</span></span> <span data-ttu-id="6de1f-155">Poiché è possibile annidare i sottomenu, possono essere presenti più livelli di **MF \_ end**.</span><span class="sxs-lookup"><span data-stu-id="6de1f-155">Because you can nest submenus, there can be multiple levels of **MF\_END**.</span></span> <span data-ttu-id="6de1f-156">In questi casi, le voci di menu sono sequenziali.</span><span class="sxs-lookup"><span data-stu-id="6de1f-156">In these instances, the menu items are sequential.</span></span>

## <a name="requirements"></a><span data-ttu-id="6de1f-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6de1f-157">Requirements</span></span>



| <span data-ttu-id="6de1f-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="6de1f-158">Requirement</span></span> | <span data-ttu-id="6de1f-159">Valore</span><span class="sxs-lookup"><span data-stu-id="6de1f-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6de1f-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6de1f-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6de1f-161">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6de1f-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6de1f-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6de1f-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6de1f-163">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6de1f-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6de1f-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6de1f-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="6de1f-165">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6de1f-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6de1f-166">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="6de1f-166">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="6de1f-167">**MENUHELPID**</span><span class="sxs-lookup"><span data-stu-id="6de1f-167">**MENUHELPID**</span></span>](menuhelpid.md)
</dt> <dt>

[<span data-ttu-id="6de1f-168">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="6de1f-168">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="6de1f-169">**NORMALMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="6de1f-169">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

<span data-ttu-id="6de1f-170">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="6de1f-170">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6de1f-171">Risorse</span><span class="sxs-lookup"><span data-stu-id="6de1f-171">Resources</span></span>](resources.md)
</dt> </dl>

 

