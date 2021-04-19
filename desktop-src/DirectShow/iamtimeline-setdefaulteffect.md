---
description: Il metodo SetDefaultEffect imposta l'effetto predefinito. Se il motore di rendering non è in grado di eseguire il rendering di un effetto, sostituisce l'effetto predefinito.
ms.assetid: 6ee94d86-c27f-4378-9a10-f3993a3ae657
title: 'Metodo IAMTimeline:: SetDefaultEffect (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 33e23070a7bb10dd040d08c145bfe1e0111026d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326785"
---
# <a name="iamtimelinesetdefaulteffect-method"></a><span data-ttu-id="767b3-104">Metodo IAMTimeline:: SetDefaultEffect</span><span class="sxs-lookup"><span data-stu-id="767b3-104">IAMTimeline::SetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="767b3-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="767b3-105">\[Deprecated.</span></span> <span data-ttu-id="767b3-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="767b3-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="767b3-107">Il `SetDefaultEffect` metodo imposta l'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="767b3-107">The `SetDefaultEffect` method sets the default effect.</span></span> <span data-ttu-id="767b3-108">Se il motore di rendering non è in grado di eseguire il rendering di un effetto, sostituisce l'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="767b3-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="767b3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="767b3-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="767b3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="767b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="767b3-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="767b3-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="767b3-112">Puntatore al GUID dell'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="767b3-112">Pointer to the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="767b3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="767b3-113">Return value</span></span>

<span data-ttu-id="767b3-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="767b3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="767b3-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="767b3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="767b3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="767b3-116">Remarks</span></span>

<span data-ttu-id="767b3-117">Se non si imposta un effetto predefinito o se l'effetto specificato come impostazione predefinita genera un errore, DES usa il proprio effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="767b3-117">If you do not set a default effect, or if the effect that you specify as a default causes an error, DES uses its own default effect.</span></span>

> [!Note]  
> <span data-ttu-id="767b3-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="767b3-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="767b3-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="767b3-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="767b3-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="767b3-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="767b3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="767b3-121">Requirements</span></span>



| <span data-ttu-id="767b3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="767b3-122">Requirement</span></span> | <span data-ttu-id="767b3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="767b3-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="767b3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="767b3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="767b3-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="767b3-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="767b3-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="767b3-126">Library</span></span><br/> | <dl> <span data-ttu-id="767b3-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="767b3-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="767b3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="767b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="767b3-129">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="767b3-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="767b3-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="767b3-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




