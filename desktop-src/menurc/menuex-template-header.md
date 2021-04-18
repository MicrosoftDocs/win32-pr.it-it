---
title: Struttura MENUEX_TEMPLATE_HEADER
description: Definisce l'intestazione per un modello di menu esteso. Questa definizione di struttura è solo per la spiegazione; non è presente in alcun file di intestazione standard.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- Menu struttura MENUEX_TEMPLATE_HEADER e altre risorse
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301201"
---
# <a name="menuex_template_header-structure"></a><span data-ttu-id="b372e-105">Struttura di intestazione del \_ modello menuex \_</span><span class="sxs-lookup"><span data-stu-id="b372e-105">MENUEX\_TEMPLATE\_HEADER structure</span></span>

<span data-ttu-id="b372e-106">Definisce l'intestazione per un modello di menu esteso.</span><span class="sxs-lookup"><span data-stu-id="b372e-106">Defines the header for an extended menu template.</span></span> <span data-ttu-id="b372e-107">Questa definizione di struttura è solo per la spiegazione; non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="b372e-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b372e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b372e-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a><span data-ttu-id="b372e-109">Members</span><span class="sxs-lookup"><span data-stu-id="b372e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b372e-110">**wVersion**</span><span class="sxs-lookup"><span data-stu-id="b372e-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b372e-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b372e-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b372e-112">Numero di versione del modello.</span><span class="sxs-lookup"><span data-stu-id="b372e-112">The template version number.</span></span> <span data-ttu-id="b372e-113">Questo membro deve essere 1 per i modelli di menu estesi.</span><span class="sxs-lookup"><span data-stu-id="b372e-113">This member must be 1 for extended menu templates.</span></span>

</dd> <dt>

<span data-ttu-id="b372e-114">**wOffset**</span><span class="sxs-lookup"><span data-stu-id="b372e-114">**wOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b372e-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b372e-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b372e-116">Offset alla prima struttura dell' [**\_ \_ elemento del modello menuex**](menuex-template-item.md) , relativa alla fine del membro della struttura.</span><span class="sxs-lookup"><span data-stu-id="b372e-116">The offset to the first [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structure, relative to the end of this structure member.</span></span> <span data-ttu-id="b372e-117">Se la definizione del primo elemento segue immediatamente il membro **dwHelpId** , questo membro deve essere 4.</span><span class="sxs-lookup"><span data-stu-id="b372e-117">If the first item definition immediately follows the **dwHelpId** member, this member should be 4.</span></span>

</dd> <dt>

<span data-ttu-id="b372e-118">**dwHelpId**</span><span class="sxs-lookup"><span data-stu-id="b372e-118">**dwHelpId**</span></span>
</dt> <dd>

<span data-ttu-id="b372e-119">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b372e-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="b372e-120">Identificatore della guida della barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="b372e-120">The help identifier of menu bar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b372e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="b372e-121">Remarks</span></span>

<span data-ttu-id="b372e-122">Un modello di menu esteso è costituito da una struttura di **\_ \_ intestazione del modello menuex** seguita da una o più strutture di [**\_ \_ elementi del modello menuex**](menuex-template-item.md) contigue.</span><span class="sxs-lookup"><span data-stu-id="b372e-122">An extended menu template consists of a **MENUEX\_TEMPLATE\_HEADER** structure followed by one or more contiguous [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structures.</span></span> <span data-ttu-id="b372e-123">Le strutture degli **\_ \_ elementi del modello menuex** , che sono di lunghezza variabile, sono allineate ai limiti **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b372e-123">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="b372e-124">Per creare un menu da un modello di menu esteso in memoria, usare la funzione [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="b372e-124">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b372e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b372e-125">Requirements</span></span>



| <span data-ttu-id="b372e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b372e-126">Requirement</span></span> | <span data-ttu-id="b372e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b372e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b372e-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b372e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b372e-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b372e-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b372e-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b372e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b372e-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b372e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b372e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b372e-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="b372e-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b372e-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b372e-134">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="b372e-134">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="b372e-135">**\_elemento del modello menuex \_**</span><span class="sxs-lookup"><span data-stu-id="b372e-135">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

<span data-ttu-id="b372e-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b372e-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b372e-137">Menu</span><span class="sxs-lookup"><span data-stu-id="b372e-137">Menus</span></span>](menus.md)
</dt> </dl>

 

 





