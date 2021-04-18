---
description: 'Non supportata. Chiamare il metodo IAMTimeline:: CreateEmptyNode per creare un nuovo oggetto sequenza temporale. Una volta creato un oggetto, non è possibile modificarne il tipo.'
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: 'Metodo IAMTimelineObj:: SetTimelineType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a63031968a2dfb43d98f9b7f59bd2d9051042732
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330802"
---
# <a name="iamtimelineobjsettimelinetype-method"></a><span data-ttu-id="0b173-105">Metodo IAMTimelineObj:: SetTimelineType</span><span class="sxs-lookup"><span data-stu-id="0b173-105">IAMTimelineObj::SetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="0b173-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0b173-106">\[Deprecated.</span></span> <span data-ttu-id="0b173-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0b173-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0b173-108">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="0b173-108">Not supported.</span></span> <span data-ttu-id="0b173-109">Chiamare il metodo [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) per creare un nuovo oggetto sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="0b173-109">Call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method to create a new timeline object.</span></span> <span data-ttu-id="0b173-110">Una volta creato un oggetto, non è possibile modificarne il tipo.</span><span class="sxs-lookup"><span data-stu-id="0b173-110">Once an object is created, you cannot change its type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b173-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b173-111">Syntax</span></span>


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a><span data-ttu-id="0b173-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b173-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b173-113">*newVal*</span><span class="sxs-lookup"><span data-stu-id="0b173-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="0b173-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0b173-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b173-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b173-115">Return value</span></span>

<span data-ttu-id="0b173-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0b173-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0b173-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0b173-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b173-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b173-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0b173-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="0b173-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0b173-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0b173-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0b173-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0b173-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b173-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b173-122">Requirements</span></span>



| <span data-ttu-id="0b173-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b173-123">Requirement</span></span> | <span data-ttu-id="0b173-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0b173-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b173-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b173-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0b173-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b173-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0b173-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b173-127">Library</span></span><br/> | <dl> <span data-ttu-id="0b173-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b173-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b173-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b173-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b173-130">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="0b173-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




