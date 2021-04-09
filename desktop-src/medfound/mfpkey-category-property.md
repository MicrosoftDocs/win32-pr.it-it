---
description: Contiene il GUID di categoria per una trasformazione Media Foundation (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: Proprietà MFPKEY_CATEGORY (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882221"
---
# <a name="mfpkey_category-property"></a><span data-ttu-id="8db23-103">\_Proprietà di categoria MFPKEY</span><span class="sxs-lookup"><span data-stu-id="8db23-103">MFPKEY\_CATEGORY property</span></span>

<span data-ttu-id="8db23-104">Contiene il GUID di categoria per una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="8db23-104">Contains the category GUID for a Media Foundation transform (MFT).</span></span>



<span data-ttu-id="8db23-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8db23-105">Data type</span></span>

<span data-ttu-id="8db23-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="8db23-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8db23-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8db23-107">PROPVARIANT member</span></span>

<span data-ttu-id="8db23-108">**GUID** (**CLSID** \* )</span><span class="sxs-lookup"><span data-stu-id="8db23-108">**GUID** (**CLSID**\*)</span></span>

<span data-ttu-id="8db23-109">\_CLSID VT</span><span class="sxs-lookup"><span data-stu-id="8db23-109">VT\_CLSID</span></span>

<span data-ttu-id="8db23-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="8db23-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="8db23-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8db23-111">Remarks</span></span>

<span data-ttu-id="8db23-112">Il valore di questa proprietà è un GUID che identifica la categoria MFT.</span><span class="sxs-lookup"><span data-stu-id="8db23-112">The value of this property is a GUID that identifies the MFT category.</span></span> <span data-ttu-id="8db23-113">Per un elenco di categorie, vedere [**la \_ categoria MFT**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="8db23-113">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

<span data-ttu-id="8db23-114">Questa proprietà è facoltativa ed è solo informativa.</span><span class="sxs-lookup"><span data-stu-id="8db23-114">This property is optional and is informational only.</span></span> <span data-ttu-id="8db23-115">Un MFT può usare questa proprietà per segnalare la categoria in cui è registrata.</span><span class="sxs-lookup"><span data-stu-id="8db23-115">An MFT can use this property to report the category under which it is registered.</span></span> <span data-ttu-id="8db23-116">Per ottenere questa proprietà, eseguire una query su MFT per l'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="8db23-116">To get this property, query the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="8db23-117">Per enumerare una categoria MFT, chiamare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .</span><span class="sxs-lookup"><span data-stu-id="8db23-117">To enumerate an MFT category, call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function.</span></span> <span data-ttu-id="8db23-118">Non esiste un collegamento diretto tra la funzione **MFTEnum** e questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8db23-118">There is no direct link between the **MFTEnum** function and this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8db23-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8db23-119">Requirements</span></span>



| <span data-ttu-id="8db23-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8db23-120">Requirement</span></span> | <span data-ttu-id="8db23-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8db23-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8db23-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8db23-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8db23-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8db23-123">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8db23-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8db23-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8db23-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8db23-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8db23-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8db23-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8db23-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="8db23-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8db23-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8db23-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db23-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8db23-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8db23-130">Trasformazioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8db23-130">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




