---
description: 'Metodo IAMTimelineObj::GetGroupIBelongTo : non supportato.'
ms.assetid: a6242c1d-cf9a-4c96-9cfd-d32199ae74b8
title: Metodo IAMTimelineObj::GetGroupIBelongTo (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGroupIBelongTo
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7aac3e043d068588e6a9330c193c1b5fb7828688
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098559"
---
# <a name="iamtimelineobjgetgroupibelongto-method"></a><span data-ttu-id="5b503-103">Metodo IAMTimelineObj::GetGroupIBelongTo</span><span class="sxs-lookup"><span data-stu-id="5b503-103">IAMTimelineObj::GetGroupIBelongTo method</span></span>

> [!Note]  
> <span data-ttu-id="5b503-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5b503-104">\[Deprecated.</span></span> <span data-ttu-id="5b503-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5b503-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5b503-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="5b503-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b503-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b503-107">Syntax</span></span>


```C++
HRESULT GetGroupIBelongTo(
   IAMTimelineGroup **ppGroup
);
```



## <a name="parameters"></a><span data-ttu-id="5b503-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b503-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b503-109">*ppGroup*</span><span class="sxs-lookup"><span data-stu-id="5b503-109">*ppGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="5b503-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5b503-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b503-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b503-111">Return value</span></span>

<span data-ttu-id="5b503-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5b503-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5b503-113">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5b503-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b503-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b503-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5b503-115">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5b503-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5b503-116">Per ottenere Qedit.h, scaricare Microsoft Windows SDK [Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b503-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5b503-117">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5b503-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5b503-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b503-118">Requirements</span></span>



| <span data-ttu-id="5b503-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b503-119">Requirement</span></span> | <span data-ttu-id="5b503-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5b503-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b503-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b503-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5b503-122"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="5b503-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5b503-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="5b503-123">Library</span></span><br/> | <dl> <span data-ttu-id="5b503-124"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b503-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b503-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b503-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b503-126">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="5b503-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




