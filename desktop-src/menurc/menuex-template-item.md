---
title: Struttura MENUEX_TEMPLATE_ITEM
description: Definisce una voce di menu in un modello di menu esteso. Questa definizione di struttura è solo per la spiegazione; non è presente in alcun file di intestazione standard.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- Menu struttura MENUEX_TEMPLATE_ITEM e altre risorse
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518699"
---
# <a name="menuex_template_item-structure"></a><span data-ttu-id="229be-105">Struttura dell'elemento del \_ modello menuex \_</span><span class="sxs-lookup"><span data-stu-id="229be-105">MENUEX\_TEMPLATE\_ITEM structure</span></span>

<span data-ttu-id="229be-106">Definisce una voce di menu in un modello di menu esteso.</span><span class="sxs-lookup"><span data-stu-id="229be-106">Defines a menu item in an extended menu template.</span></span> <span data-ttu-id="229be-107">Questa definizione di struttura è solo per la spiegazione; non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="229be-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="229be-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="229be-108">Syntax</span></span>

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a><span data-ttu-id="229be-109">Members</span><span class="sxs-lookup"><span data-stu-id="229be-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="229be-110">**dwType**</span><span class="sxs-lookup"><span data-stu-id="229be-110">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="229be-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="229be-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="229be-112">Tipo di voce di menu.</span><span class="sxs-lookup"><span data-stu-id="229be-112">The menu item type.</span></span> <span data-ttu-id="229be-113">Questo membro può essere una combinazione dei valori di tipo (a partire da MFT) elencati con la struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="229be-113">This member can be a combination of the type (beginning with MFT) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="229be-114">**dwState**</span><span class="sxs-lookup"><span data-stu-id="229be-114">**dwState**</span></span>
</dt> <dd>

<span data-ttu-id="229be-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="229be-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="229be-116">Stato della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="229be-116">The menu item state.</span></span> <span data-ttu-id="229be-117">Questo membro può essere una combinazione dei valori di stato (a partire da MFS) elencati con la struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="229be-117">This member can be a combination of the state (beginning with MFS) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="229be-118">**uId**</span><span class="sxs-lookup"><span data-stu-id="229be-118">**uId**</span></span>
</dt> <dd>

<span data-ttu-id="229be-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="229be-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="229be-120">Identificatore della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="229be-120">The menu item identifier.</span></span> <span data-ttu-id="229be-121">Si tratta di un valore definito dall'applicazione che identifica la voce di menu.</span><span class="sxs-lookup"><span data-stu-id="229be-121">This is an application-defined value that identifies the menu item.</span></span> <span data-ttu-id="229be-122">In una risorsa di menu esteso gli elementi che aprono menu a discesa o sottomenu nonché elementi di comando possono avere identificatori.</span><span class="sxs-lookup"><span data-stu-id="229be-122">In an extended menu resource, items that open drop-down menus or submenus as well as command items can have identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="229be-123">**wFlags**</span><span class="sxs-lookup"><span data-stu-id="229be-123">**wFlags**</span></span>
</dt> <dd>

<span data-ttu-id="229be-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="229be-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="229be-125">Specifica se la voce di menu è l'ultimo elemento della barra dei menu, il menu a discesa, il sottomenu o il menu di scelta rapida e se è un elemento che apre un menu a discesa o un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="229be-125">Specifies whether the menu item is the last item in the menu bar, drop-down menu, submenu, or shortcut menu and whether it is an item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="229be-126">Questo membro può essere zero o più di questi valori.</span><span class="sxs-lookup"><span data-stu-id="229be-126">This member can be zero or more of these values.</span></span> <span data-ttu-id="229be-127">Per le applicazioni a 32 bit, questo membro è una parola; per le applicazioni a 16 bit, si tratta di un byte.</span><span class="sxs-lookup"><span data-stu-id="229be-127">For 32-bit applications, this member is a word; for 16-bit applications, it is a byte.</span></span>

<dt>

<span data-ttu-id="229be-128">0x80</span><span class="sxs-lookup"><span data-stu-id="229be-128">0x80</span></span>
</dt> <dd>

<span data-ttu-id="229be-129">La struttura definisce l'ultima voce di menu della barra dei menu, il menu a discesa, il sottomenu o il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="229be-129">The structure defines the last menu item in the menu bar, drop-down menu, submenu, or shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="229be-130">0x01</span><span class="sxs-lookup"><span data-stu-id="229be-130">0x01</span></span>
</dt> <dd>

<span data-ttu-id="229be-131">La struttura definisce un elemento che apre un menu a discesa o un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="229be-131">The structure defines a item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="229be-132">Le strutture successive definiscono le voci di menu nel menu a discesa o nel sottomenu corrispondente.</span><span class="sxs-lookup"><span data-stu-id="229be-132">Subsequent structures define menu items in the corresponding drop-down menu or submenu.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="229be-133">**szText**</span><span class="sxs-lookup"><span data-stu-id="229be-133">**szText**</span></span>
</dt> <dd>

<span data-ttu-id="229be-134">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="229be-134">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="229be-135">Testo della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="229be-135">The menu item text.</span></span> <span data-ttu-id="229be-136">Questo membro è una stringa Unicode con terminazione null, allineata al confine di una parola.</span><span class="sxs-lookup"><span data-stu-id="229be-136">This member is a null-terminated Unicode string, aligned on a word boundary.</span></span> <span data-ttu-id="229be-137">Le dimensioni della definizione della voce di menu variano a seconda della lunghezza di questa stringa.</span><span class="sxs-lookup"><span data-stu-id="229be-137">The size of the menu item definition varies depending on the length of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="229be-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="229be-138">Remarks</span></span>

<span data-ttu-id="229be-139">Un modello di menu esteso è costituito da una struttura di [**\_ \_ intestazione del modello menuex**](menuex-template-header.md) seguita da una o più strutture di **\_ \_ elementi del modello menuex** contigue.</span><span class="sxs-lookup"><span data-stu-id="229be-139">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one or more contiguous **MENUEX\_TEMPLATE\_ITEM** structures.</span></span> <span data-ttu-id="229be-140">Le strutture degli **\_ \_ elementi del modello menuex** , che sono di lunghezza variabile, sono allineate ai limiti **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="229be-140">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="229be-141">Per creare un menu da un modello di menu esteso in memoria, usare la funzione [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="229be-141">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="229be-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="229be-142">Requirements</span></span>



| <span data-ttu-id="229be-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="229be-143">Requirement</span></span> | <span data-ttu-id="229be-144">Valore</span><span class="sxs-lookup"><span data-stu-id="229be-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="229be-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="229be-145">Minimum supported client</span></span><br/> | <span data-ttu-id="229be-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="229be-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="229be-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="229be-147">Minimum supported server</span></span><br/> | <span data-ttu-id="229be-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="229be-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="229be-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="229be-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="229be-150">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="229be-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="229be-151">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="229be-151">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="229be-152">**\_intestazione del modello menuex \_**</span><span class="sxs-lookup"><span data-stu-id="229be-152">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="229be-153">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="229be-153">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

<span data-ttu-id="229be-154">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="229be-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="229be-155">Menu</span><span class="sxs-lookup"><span data-stu-id="229be-155">Menus</span></span>](menus.md)
</dt> </dl>

 

 





