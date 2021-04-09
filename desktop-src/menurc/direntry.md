---
title: Struttura di diaffitto
description: Contiene un ordinale univoco che identifica un singolo tipo di carattere nel gruppo di risorse del tipo di carattere. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Menu della struttura di dirente e altre risorse
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742031"
---
# <a name="direntry-structure"></a><span data-ttu-id="4b87b-105">Struttura di diaffitto</span><span class="sxs-lookup"><span data-stu-id="4b87b-105">DIRENTRY structure</span></span>

<span data-ttu-id="4b87b-106">Contiene un ordinale univoco che identifica un singolo tipo di carattere nel gruppo di risorse del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="4b87b-106">Contains a unique ordinal that identifies an individual font in the font resource group.</span></span> <span data-ttu-id="4b87b-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="4b87b-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b87b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b87b-108">Syntax</span></span>


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a><span data-ttu-id="4b87b-109">Members</span><span class="sxs-lookup"><span data-stu-id="4b87b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b87b-110">**fontOrdinal**</span><span class="sxs-lookup"><span data-stu-id="4b87b-110">**fontOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="4b87b-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4b87b-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4b87b-112">Identificatore ordinale univoco per un singolo tipo di carattere in un gruppo di risorse dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="4b87b-112">A unique ordinal identifier for an individual font in a font resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b87b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b87b-113">Remarks</span></span>

<span data-ttu-id="4b87b-114">La struttura [**FONTDIRENTRY**](fontdirentry.md) per il tipo di carattere specificato segue direttamente la struttura di **dislocazione** per tale tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="4b87b-114">The [**FONTDIRENTRY**](fontdirentry.md) structure for the specified font directly follows the **DIRENTRY** structure for that font.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b87b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b87b-115">Requirements</span></span>



| <span data-ttu-id="4b87b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b87b-116">Requirement</span></span> | <span data-ttu-id="4b87b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4b87b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4b87b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b87b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4b87b-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b87b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4b87b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b87b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4b87b-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b87b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4b87b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b87b-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b87b-123">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4b87b-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4b87b-124">**FONTDIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="4b87b-124">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

[<span data-ttu-id="4b87b-125">**FONTGROUPHDR**</span><span class="sxs-lookup"><span data-stu-id="4b87b-125">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="4b87b-126">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4b87b-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4b87b-127">Risorse</span><span class="sxs-lookup"><span data-stu-id="4b87b-127">Resources</span></span>](resources.md)
</dt> </dl>

 

 





