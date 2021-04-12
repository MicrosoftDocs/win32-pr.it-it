---
title: Struttura NORMALMENUITEM
description: Contiene informazioni su ogni elemento in una risorsa di menu che non apre un menu o un sottomenu. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Menu struttura NORMALMENUITEM e altre risorse
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340513"
---
# <a name="normalmenuitem-structure"></a><span data-ttu-id="fad37-105">Struttura NORMALMENUITEM</span><span class="sxs-lookup"><span data-stu-id="fad37-105">NORMALMENUITEM structure</span></span>

<span data-ttu-id="fad37-106">Contiene informazioni su ogni elemento in una risorsa di menu che non apre un menu o un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="fad37-106">Contains information about each item in a menu resource that does not open a menu or a submenu.</span></span> <span data-ttu-id="fad37-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="fad37-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad37-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fad37-108">Syntax</span></span>


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a><span data-ttu-id="fad37-109">Members</span><span class="sxs-lookup"><span data-stu-id="fad37-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="fad37-110">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="fad37-110">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="fad37-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="fad37-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fad37-112">Tipo di voce di menu.</span><span class="sxs-lookup"><span data-stu-id="fad37-112">The type of menu item.</span></span> <span data-ttu-id="fad37-113">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fad37-113">This member can be one of the following values.</span></span>



| <span data-ttu-id="fad37-114">Valore</span><span class="sxs-lookup"><span data-stu-id="fad37-114">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="fad37-115">Significato</span><span class="sxs-lookup"><span data-stu-id="fad37-115">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="fad37-116"><dt>**Fabbisogno \_ di FINE**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="fad37-116"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="fad37-117">La voce di menu è l'ultima in questo sottomenu o risorsa di menu; Questo flag viene utilizzato internamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fad37-117">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="fad37-118"><dt>**Fabbisogno \_ di POPUP**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="fad37-118"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="fad37-119">La voce di menu apre un menu o un sottomenu; il flag viene utilizzato internamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fad37-119">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/>                    |



 

</dd> <dt>

<span data-ttu-id="fad37-120">**menuText**</span><span class="sxs-lookup"><span data-stu-id="fad37-120">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="fad37-121">Tipo: **szOrOrd**</span><span class="sxs-lookup"><span data-stu-id="fad37-121">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="fad37-122">Stringa Unicode con terminazione null che contiene il testo di questa voce di menu.</span><span class="sxs-lookup"><span data-stu-id="fad37-122">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="fad37-123">Non esiste un limite fisso per le dimensioni di questa stringa.</span><span class="sxs-lookup"><span data-stu-id="fad37-123">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fad37-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="fad37-124">Remarks</span></span>

<span data-ttu-id="fad37-125">Esiste una struttura **NORMALMENUITEM** per ogni voce di menu che non apre un menu o un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="fad37-125">There is one **NORMALMENUITEM** structure for each menu item that does not open a menu or a submenu.</span></span> <span data-ttu-id="fad37-126">Indica l'ultima voce di menu in un menu impostando il membro **resInfo** su **fabbisogno \_ finale**.</span><span class="sxs-lookup"><span data-stu-id="fad37-126">Indicate the last menu item on a menu by setting the **resInfo** member to **MFR\_END**.</span></span>

<span data-ttu-id="fad37-127">Un separatore di menu è un tipo speciale di voce di menu che è inattivo, ma viene visualizzato come una barra di divisione tra due voci di menu attive.</span><span class="sxs-lookup"><span data-stu-id="fad37-127">A menu separator is a special type of menu item that is inactive but appears as a dividing bar between two active menu items.</span></span> <span data-ttu-id="fad37-128">Indicare un separatore di menu lasciando vuoto il membro **menuText** .</span><span class="sxs-lookup"><span data-stu-id="fad37-128">Indicate a menu separator by leaving the **menuText** member empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad37-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fad37-129">Requirements</span></span>



| <span data-ttu-id="fad37-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fad37-130">Requirement</span></span> | <span data-ttu-id="fad37-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fad37-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fad37-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fad37-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fad37-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fad37-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fad37-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fad37-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fad37-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fad37-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fad37-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fad37-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="fad37-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fad37-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fad37-138">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="fad37-138">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="fad37-139">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="fad37-139">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="fad37-140">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="fad37-140">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="fad37-141">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="fad37-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fad37-142">Risorse</span><span class="sxs-lookup"><span data-stu-id="fad37-142">Resources</span></span>](resources.md)
</dt> </dl>

 

 





