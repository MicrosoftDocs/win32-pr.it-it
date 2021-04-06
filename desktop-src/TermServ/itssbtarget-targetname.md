---
title: Proprietà TargetName di ITsSbTarget
description: Specifica o Recupera il nome della destinazione.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TargetName
- Servizi Desktop remoto proprietà TargetName, interfaccia ITsSbTarget
- Interfaccia ITsSbTarget Servizi Desktop remoto, proprietà TargetName
- Servizi Desktop remoto proprietà TargetName, interfaccia ITsSbTargetEx
- Interfaccia ITsSbTargetEx Servizi Desktop remoto, proprietà TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dce949abee4ca00184a2b784ab154dbd75b9de6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045919"
---
# <a name="itssbtargettargetname-property"></a><span data-ttu-id="8d954-108">Proprietà ITsSbTarget:: TargetName</span><span class="sxs-lookup"><span data-stu-id="8d954-108">ITsSbTarget::TargetName property</span></span>

<span data-ttu-id="8d954-109">Specifica o Recupera il nome della destinazione.</span><span class="sxs-lookup"><span data-stu-id="8d954-109">Specifies or retrieves the name of the target.</span></span>

<span data-ttu-id="8d954-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8d954-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d954-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d954-111">Syntax</span></span>


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="8d954-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8d954-112">Property value</span></span>

<span data-ttu-id="8d954-113">Variabile **BSTR** che specifica il nome di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8d954-113">A **BSTR** variable that specifies the target name.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d954-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d954-114">Remarks</span></span>

<span data-ttu-id="8d954-115">Questa proprietà è di sola lettura prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8d954-115">This property was read-only prior to Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d954-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d954-116">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d954-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d954-117">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="8d954-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8d954-118">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d954-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d954-119">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="8d954-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d954-120">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d954-121">IDL</span><span class="sxs-lookup"><span data-stu-id="8d954-121">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="8d954-122"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="8d954-122"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d954-123">IID</span><span class="sxs-lookup"><span data-stu-id="8d954-123">IID</span></span><br/></td>
<td><span data-ttu-id="8d954-124">IID_ITsSbTarget viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="8d954-124">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="8d954-125">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="8d954-125">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="8d954-126">e85e10ea-db0b-4752-B456-5fd5840901c0 in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d954-126">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="8d954-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d954-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d954-128">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="8d954-128">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="8d954-129">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="8d954-129">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





