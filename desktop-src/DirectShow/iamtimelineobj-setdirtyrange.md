---
description: 'Metodo IAMTimelineObj::SetDirtyRange: non implementato.'
ms.assetid: f3be3b5a-7ab9-44ca-8a03-33fb905d3aea
title: Metodo IAMTimelineObj::SetDirtyRange (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e3f70e5ba9d01733df154911c4f40d2b9d33776
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119489"
---
# <a name="iamtimelineobjsetdirtyrange-method"></a><span data-ttu-id="7fabe-103">Metodo IAMTimelineObj::SetDirtyRange</span><span class="sxs-lookup"><span data-stu-id="7fabe-103">IAMTimelineObj::SetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="7fabe-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7fabe-104">\[Deprecated.</span></span> <span data-ttu-id="7fabe-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7fabe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7fabe-106">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="7fabe-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fabe-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fabe-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="7fabe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fabe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fabe-109">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="7fabe-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="7fabe-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7fabe-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7fabe-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="7fabe-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="7fabe-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7fabe-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fabe-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fabe-113">Return value</span></span>

<span data-ttu-id="7fabe-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7fabe-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7fabe-115">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="7fabe-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fabe-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fabe-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7fabe-117">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7fabe-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7fabe-118">Per ottenere Qedit.h, scaricare l'aggiornamento [Microsoft Windows SDK per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fabe-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7fabe-119">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7fabe-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7fabe-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fabe-120">Requirements</span></span>



| <span data-ttu-id="7fabe-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fabe-121">Requirement</span></span> | <span data-ttu-id="7fabe-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7fabe-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fabe-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fabe-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7fabe-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="7fabe-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7fabe-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="7fabe-125">Library</span></span><br/> | <dl> <span data-ttu-id="7fabe-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fabe-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fabe-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fabe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fabe-128">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="7fabe-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




