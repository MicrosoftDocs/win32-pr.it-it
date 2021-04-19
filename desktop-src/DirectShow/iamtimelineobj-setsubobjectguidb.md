---
description: "Il metodo SetSubObjectGUIDB specifica il GUID dell'oggetto SubObject associato a questo oggetto. Questo metodo è equivalente a IAMTimelineObj:: SetSubObjectGUID ma accetta un valore BSTR."
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: 'Metodo IAMTimelineObj:: SetSubObjectGUIDB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8df74249f061321ccd710822b8c2e0b76d5c3582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327665"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a><span data-ttu-id="e145b-104">Metodo IAMTimelineObj:: SetSubObjectGUIDB</span><span class="sxs-lookup"><span data-stu-id="e145b-104">IAMTimelineObj::SetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="e145b-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e145b-105">\[Deprecated.</span></span> <span data-ttu-id="e145b-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e145b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e145b-107">Il `SetSubObjectGUIDB` metodo specifica il GUID dell'oggetto SubObject associato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e145b-107">The `SetSubObjectGUIDB` method specifies the GUID of the subobject associated with this object.</span></span> <span data-ttu-id="e145b-108">Questo metodo è equivalente a [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) ma accetta un valore **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="e145b-108">This method is equivalent to [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) but takes a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e145b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e145b-109">Syntax</span></span>


```C++
HRESULT SetSubObjectGUIDB(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e145b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e145b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e145b-111">*newVal*</span><span class="sxs-lookup"><span data-stu-id="e145b-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e145b-112">**BSTR** che rappresenta il GUID dell'oggetto SubObject.</span><span class="sxs-lookup"><span data-stu-id="e145b-112">**BSTR** representing the GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e145b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e145b-113">Return value</span></span>

<span data-ttu-id="e145b-114">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="e145b-114">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e145b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e145b-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e145b-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e145b-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e145b-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e145b-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e145b-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e145b-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e145b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e145b-119">Requirements</span></span>



| <span data-ttu-id="e145b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e145b-120">Requirement</span></span> | <span data-ttu-id="e145b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e145b-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e145b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e145b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e145b-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e145b-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e145b-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="e145b-124">Library</span></span><br/> | <dl> <span data-ttu-id="e145b-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e145b-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e145b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e145b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e145b-127">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="e145b-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="e145b-128">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e145b-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




