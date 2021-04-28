---
description: 'Metodo IAMTimeline::RemGroupFromList: non supportato.'
ms.assetid: 9ad5f5ee-2a2a-448b-9da4-2ad8d543eb22
title: Metodo IAMTimeline::RemGroupFromList (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.RemGroupFromList
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fcb2a73f32ab1c1f401a4508c63e53cc58ebcfb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098689"
---
# <a name="iamtimelineremgroupfromlist-method"></a><span data-ttu-id="916f9-103">Metodo IAMTimeline::RemGroupFromList</span><span class="sxs-lookup"><span data-stu-id="916f9-103">IAMTimeline::RemGroupFromList method</span></span>

> [!Note]  
> <span data-ttu-id="916f9-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="916f9-104">\[Deprecated.</span></span> <span data-ttu-id="916f9-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="916f9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="916f9-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="916f9-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="916f9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="916f9-107">Syntax</span></span>


```C++
HRESULT RemGroupFromList(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a><span data-ttu-id="916f9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="916f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="916f9-109">*pGroup*</span><span class="sxs-lookup"><span data-stu-id="916f9-109">*pGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="916f9-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="916f9-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="916f9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="916f9-111">Return value</span></span>

<span data-ttu-id="916f9-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="916f9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="916f9-113">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="916f9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="916f9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="916f9-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="916f9-115">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="916f9-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="916f9-116">Per ottenere Qedit.h, scaricare Microsoft Windows SDK [Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="916f9-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="916f9-117">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="916f9-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="916f9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="916f9-118">Requirements</span></span>



| <span data-ttu-id="916f9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="916f9-119">Requirement</span></span> | <span data-ttu-id="916f9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="916f9-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="916f9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="916f9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="916f9-122"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="916f9-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="916f9-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="916f9-123">Library</span></span><br/> | <dl> <span data-ttu-id="916f9-124"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="916f9-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="916f9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="916f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="916f9-126">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="916f9-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




