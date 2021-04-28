---
description: 'Metodo IAMTimelineObj::GetDirtyRange2 : non supportato.'
ms.assetid: 3acd36f2-52f4-4734-a753-c6a6ce7e9187
title: Metodo IAMTimelineObj::GetDirtyRange2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 14c573403bf946b54bbfcc74ae41145a3f1c5c7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119519"
---
# <a name="iamtimelineobjgetdirtyrange2-method"></a><span data-ttu-id="6fdca-103">Metodo IAMTimelineObj::GetDirtyRange2</span><span class="sxs-lookup"><span data-stu-id="6fdca-103">IAMTimelineObj::GetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="6fdca-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6fdca-104">\[Deprecated.</span></span> <span data-ttu-id="6fdca-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6fdca-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6fdca-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="6fdca-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdca-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fdca-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="6fdca-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6fdca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fdca-109">*Pstart*</span><span class="sxs-lookup"><span data-stu-id="6fdca-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6fdca-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="6fdca-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6fdca-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="6fdca-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="6fdca-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="6fdca-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fdca-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6fdca-113">Return value</span></span>

<span data-ttu-id="6fdca-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6fdca-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fdca-115">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="6fdca-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fdca-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fdca-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6fdca-117">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6fdca-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6fdca-118">Per ottenere Qedit.h, scaricare Microsoft Windows SDK [Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fdca-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6fdca-119">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6fdca-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6fdca-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fdca-120">Requirements</span></span>



| <span data-ttu-id="6fdca-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fdca-121">Requirement</span></span> | <span data-ttu-id="6fdca-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6fdca-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fdca-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fdca-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6fdca-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="6fdca-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6fdca-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="6fdca-125">Library</span></span><br/> | <dl> <span data-ttu-id="6fdca-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fdca-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fdca-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fdca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fdca-128">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="6fdca-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




