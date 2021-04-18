---
description: Non implementato.
ms.assetid: 14ff2979-134f-45e4-98e1-1a119e1ffee2
title: 'Metodo IAMTimelineObj:: SetDirtyRange2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7ce2511a4b94f656197cef1bcb2c3cdfb4b4df61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330820"
---
# <a name="iamtimelineobjsetdirtyrange2-method"></a><span data-ttu-id="eb7ba-103">Metodo IAMTimelineObj:: SetDirtyRange2</span><span class="sxs-lookup"><span data-stu-id="eb7ba-103">IAMTimelineObj::SetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="eb7ba-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-104">\[Deprecated.</span></span> <span data-ttu-id="eb7ba-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb7ba-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eb7ba-106">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb7ba-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb7ba-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="eb7ba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb7ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb7ba-109">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="eb7ba-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7ba-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eb7ba-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="eb7ba-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7ba-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb7ba-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb7ba-113">Return value</span></span>

<span data-ttu-id="eb7ba-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb7ba-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb7ba-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb7ba-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb7ba-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eb7ba-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eb7ba-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="eb7ba-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eb7ba-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eb7ba-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb7ba-120">Requirements</span></span>



| <span data-ttu-id="eb7ba-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb7ba-121">Requirement</span></span> | <span data-ttu-id="eb7ba-122">Valore</span><span class="sxs-lookup"><span data-stu-id="eb7ba-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb7ba-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb7ba-123">Header</span></span><br/>  | <dl> <span data-ttu-id="eb7ba-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb7ba-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eb7ba-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb7ba-125">Library</span></span><br/> | <dl> <span data-ttu-id="eb7ba-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb7ba-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb7ba-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb7ba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb7ba-128">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="eb7ba-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




