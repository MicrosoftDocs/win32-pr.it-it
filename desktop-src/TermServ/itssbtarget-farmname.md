---
title: Proprietà Farmname ITsSbTarget
description: Recupera o specifica il nome della farm a cui viene unita la destinazione.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà farmname
- Servizi Desktop remoto proprietà farmname, interfaccia ITsSbTarget
- Interfaccia ITsSbTarget Servizi Desktop remoto, proprietà Farmname
- Servizi Desktop remoto proprietà farmname, interfaccia ITsSbTargetEx
- Interfaccia ITsSbTargetEx Servizi Desktop remoto, proprietà Farmname
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94f86b2cf0ec257be9fe9b801e6fceae364a46e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718319"
---
# <a name="itssbtargetfarmname-property"></a><span data-ttu-id="24d9e-108">Proprietà ITsSbTarget:: Farmname</span><span class="sxs-lookup"><span data-stu-id="24d9e-108">ITsSbTarget::FarmName property</span></span>

<span data-ttu-id="24d9e-109">Recupera o specifica il nome della farm a cui viene unita la destinazione.</span><span class="sxs-lookup"><span data-stu-id="24d9e-109">Retrieves or specifies the name of the farm to which this target is joined.</span></span>

<span data-ttu-id="24d9e-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="24d9e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="24d9e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24d9e-111">Syntax</span></span>


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="24d9e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="24d9e-112">Property value</span></span>

<span data-ttu-id="24d9e-113">Variabile **BSTR** che contiene il nome della farm.</span><span class="sxs-lookup"><span data-stu-id="24d9e-113">A **BSTR** variable that contains the farm name.</span></span>

## <a name="requirements"></a><span data-ttu-id="24d9e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24d9e-114">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24d9e-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24d9e-115">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="24d9e-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="24d9e-116">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24d9e-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24d9e-117">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="24d9e-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="24d9e-118">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24d9e-119">IDL</span><span class="sxs-lookup"><span data-stu-id="24d9e-119">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="24d9e-120"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="24d9e-120"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24d9e-121">IID</span><span class="sxs-lookup"><span data-stu-id="24d9e-121">IID</span></span><br/></td>
<td><span data-ttu-id="24d9e-122">IID_ITsSbTarget viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="24d9e-122">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="24d9e-123">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="24d9e-123">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="24d9e-124">e85e10ea-db0b-4752-B456-5fd5840901c0 in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="24d9e-124">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="24d9e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24d9e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24d9e-126">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="24d9e-126">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="24d9e-127">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="24d9e-127">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





