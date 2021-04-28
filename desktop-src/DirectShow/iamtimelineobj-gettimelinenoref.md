---
description: 'Metodo IAMTimelineObj::GetTimelineNoRef: non supportato.'
ms.assetid: be7721e4-ba43-47c1-b955-e97afc5caac4
title: Metodo IAMTimelineObj::GetTimelineNoRef (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineNoRef
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f36918f7e2bc52fb8cb2898930ff1971ad33b74b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098532"
---
# <a name="iamtimelineobjgettimelinenoref-method"></a><span data-ttu-id="1c522-103">Metodo IAMTimelineObj::GetTimelineNoRef</span><span class="sxs-lookup"><span data-stu-id="1c522-103">IAMTimelineObj::GetTimelineNoRef method</span></span>

> [!Note]  
> <span data-ttu-id="1c522-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1c522-104">\[Deprecated.</span></span> <span data-ttu-id="1c522-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1c522-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1c522-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="1c522-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c522-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c522-107">Syntax</span></span>


```C++
HRESULT GetTimelineNoRef(
   IAMTimeline **ppResult
);
```



## <a name="parameters"></a><span data-ttu-id="1c522-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c522-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c522-109">*ppResult*</span><span class="sxs-lookup"><span data-stu-id="1c522-109">*ppResult*</span></span> 
</dt> <dd>

<span data-ttu-id="1c522-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="1c522-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c522-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c522-111">Return value</span></span>

<span data-ttu-id="1c522-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1c522-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1c522-113">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="1c522-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c522-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c522-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1c522-115">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="1c522-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1c522-116">Per ottenere Qedit.h, scaricare l'aggiornamento [Microsoft Windows SDK per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c522-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1c522-117">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1c522-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1c522-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c522-118">Requirements</span></span>



| <span data-ttu-id="1c522-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c522-119">Requirement</span></span> | <span data-ttu-id="1c522-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1c522-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c522-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c522-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1c522-122"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="1c522-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1c522-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c522-123">Library</span></span><br/> | <dl> <span data-ttu-id="1c522-124"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c522-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c522-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c522-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c522-126">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="1c522-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




