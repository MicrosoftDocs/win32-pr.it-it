---
title: Struttura NEWHEADER
description: Contiene il numero di componenti icona o cursore in un gruppo di risorse. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menu struttura NEWHEADER e altre risorse
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963896"
---
# <a name="newheader-structure"></a><span data-ttu-id="26cee-105">Struttura NEWHEADER</span><span class="sxs-lookup"><span data-stu-id="26cee-105">NEWHEADER structure</span></span>

<span data-ttu-id="26cee-106">Contiene il numero di componenti icona o cursore in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26cee-106">Contains the number of icon or cursor components in a resource group.</span></span> <span data-ttu-id="26cee-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="26cee-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="26cee-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26cee-108">Syntax</span></span>


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a><span data-ttu-id="26cee-109">Members</span><span class="sxs-lookup"><span data-stu-id="26cee-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="26cee-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="26cee-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="26cee-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="26cee-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="26cee-112">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="26cee-112">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="26cee-113">**ResType**</span><span class="sxs-lookup"><span data-stu-id="26cee-113">**ResType**</span></span>
</dt> <dd>

<span data-ttu-id="26cee-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="26cee-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="26cee-115">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="26cee-115">The resource type.</span></span> <span data-ttu-id="26cee-116">Questo membro deve avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="26cee-116">This member must have one of the following values.</span></span>



| <span data-ttu-id="26cee-117">Valore</span><span class="sxs-lookup"><span data-stu-id="26cee-117">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="26cee-118">Significato</span><span class="sxs-lookup"><span data-stu-id="26cee-118">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <span data-ttu-id="26cee-119"><dt>**Res \_ CURSORE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="26cee-119"><dt>**RES\_CURSOR**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="26cee-120">Tipo di risorsa Cursor.</span><span class="sxs-lookup"><span data-stu-id="26cee-120">Cursor resource type.</span></span><br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <span data-ttu-id="26cee-121"><dt>**Res \_ ICONA**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="26cee-121"><dt>**RES\_ICON**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="26cee-122">Tipo di risorsa icona.</span><span class="sxs-lookup"><span data-stu-id="26cee-122">Icon resource type.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="26cee-123">**ResCount**</span><span class="sxs-lookup"><span data-stu-id="26cee-123">**ResCount**</span></span>
</dt> <dd>

<span data-ttu-id="26cee-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="26cee-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="26cee-125">Numero di componenti icona o cursore nel gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26cee-125">The number of icon or cursor components in the resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26cee-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="26cee-126">Remarks</span></span>

<span data-ttu-id="26cee-127">Una o più strutture [**RESDIR**](resdir.md) seguono immediatamente la struttura **NEWHEADER** nel file res.</span><span class="sxs-lookup"><span data-stu-id="26cee-127">One or more [**RESDIR**](resdir.md) structures immediately follow the **NEWHEADER** structure in the .res file.</span></span> <span data-ttu-id="26cee-128">Il membro **ResCount** specifica il numero di strutture **RESDIR** .</span><span class="sxs-lookup"><span data-stu-id="26cee-128">The **ResCount** member specifies the number of **RESDIR** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="26cee-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26cee-129">Requirements</span></span>



| <span data-ttu-id="26cee-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="26cee-130">Requirement</span></span> | <span data-ttu-id="26cee-131">Valore</span><span class="sxs-lookup"><span data-stu-id="26cee-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="26cee-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26cee-132">Minimum supported client</span></span><br/> | <span data-ttu-id="26cee-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26cee-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="26cee-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26cee-134">Minimum supported server</span></span><br/> | <span data-ttu-id="26cee-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26cee-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="26cee-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26cee-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="26cee-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="26cee-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="26cee-138">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="26cee-138">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="26cee-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="26cee-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="26cee-140">Risorse</span><span class="sxs-lookup"><span data-stu-id="26cee-140">Resources</span></span>](resources.md)
</dt> </dl>

 

 





