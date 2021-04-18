---
description: Il metodo RemoveAll rimuove definitivamente questo oggetto dalla sequenza temporale, inclusi i sottooggetti e gli elementi figlio.
ms.assetid: 9596cf47-63fe-4839-a6d5-3685fc91a935
title: 'Metodo IAMTimelineObj:: RemoveAll (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.RemoveAll
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1888b89773253285036c89e20332d92555b6db2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330822"
---
# <a name="iamtimelineobjremoveall-method"></a><span data-ttu-id="f15f5-103">Metodo IAMTimelineObj:: RemoveAll</span><span class="sxs-lookup"><span data-stu-id="f15f5-103">IAMTimelineObj::RemoveAll method</span></span>

> [!Note]  
> <span data-ttu-id="f15f5-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f15f5-104">\[Deprecated.</span></span> <span data-ttu-id="f15f5-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f15f5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f15f5-106">Il `RemoveAll` metodo rimuove definitivamente questo oggetto dalla sequenza temporale, inclusi i sottooggetti e gli elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="f15f5-106">The `RemoveAll` method permanently removes this object from the timeline, including subobjects and children.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15f5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f15f5-107">Syntax</span></span>


```C++
HRESULT RemoveAll();
```



## <a name="parameters"></a><span data-ttu-id="f15f5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f15f5-108">Parameters</span></span>

<span data-ttu-id="f15f5-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f15f5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f15f5-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f15f5-110">Return value</span></span>

<span data-ttu-id="f15f5-111">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f15f5-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f15f5-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f15f5-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f15f5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f15f5-113">Remarks</span></span>

<span data-ttu-id="f15f5-114">Per rimuovere un oggetto per poterlo reinserire altrove nella sequenza temporale, chiamare [**IAMTimelineObj:: Remove**](iamtimelineobj-remove.md).</span><span class="sxs-lookup"><span data-stu-id="f15f5-114">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md).</span></span>

> [!Note]  
> <span data-ttu-id="f15f5-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f15f5-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f15f5-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f15f5-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f15f5-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f15f5-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f15f5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f15f5-118">Requirements</span></span>



| <span data-ttu-id="f15f5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f15f5-119">Requirement</span></span> | <span data-ttu-id="f15f5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f15f5-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f15f5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f15f5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f15f5-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f15f5-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f15f5-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f15f5-123">Library</span></span><br/> | <dl> <span data-ttu-id="f15f5-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f15f5-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f15f5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f15f5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15f5-126">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="f15f5-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f15f5-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="f15f5-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




