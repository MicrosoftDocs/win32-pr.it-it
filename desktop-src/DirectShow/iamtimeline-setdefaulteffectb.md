---
description: "Il metodo SetDefaultEffectB imposta l'effetto predefinito. Questo metodo è equivalente a IAMTimeline:: SetDefaultEffect, ma accetta un valore BSTR anziché un puntatore a un GUID."
ms.assetid: ffee9728-f69e-48a4-ac0a-d41347a20deb
title: 'Metodo IAMTimeline:: SetDefaultEffectB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a8722a195078cb032285e4ea2ac449ad045d54f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326783"
---
# <a name="iamtimelinesetdefaulteffectb-method"></a><span data-ttu-id="d4e55-104">Metodo IAMTimeline:: SetDefaultEffectB</span><span class="sxs-lookup"><span data-stu-id="d4e55-104">IAMTimeline::SetDefaultEffectB method</span></span>

> [!Note]  
> <span data-ttu-id="d4e55-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="d4e55-105">\[Deprecated.</span></span> <span data-ttu-id="d4e55-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d4e55-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d4e55-107">Il `SetDefaultEffectB` metodo imposta l'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="d4e55-107">The `SetDefaultEffectB` method sets the default effect.</span></span> <span data-ttu-id="d4e55-108">Questo metodo è equivalente a [**IAMTimeline:: SetDefaultEffect**](iamtimeline-setdefaulteffect.md), ma accetta un valore BSTR anziché un puntatore a un GUID.</span><span class="sxs-lookup"><span data-stu-id="d4e55-108">This method is equivalent to [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md), but takes a BSTR value, rather than a pointer to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4e55-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4e55-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffectB(
   BSTR pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="d4e55-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4e55-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4e55-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="d4e55-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e55-112">Valore BSTR che rappresenta il GUID dell'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="d4e55-112">BSTR value representing the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4e55-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4e55-113">Return value</span></span>

<span data-ttu-id="d4e55-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d4e55-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d4e55-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d4e55-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4e55-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4e55-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d4e55-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="d4e55-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d4e55-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d4e55-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d4e55-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d4e55-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d4e55-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4e55-120">Requirements</span></span>



| <span data-ttu-id="d4e55-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4e55-121">Requirement</span></span> | <span data-ttu-id="d4e55-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d4e55-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e55-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4e55-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d4e55-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4e55-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d4e55-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4e55-125">Library</span></span><br/> | <dl> <span data-ttu-id="d4e55-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4e55-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4e55-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4e55-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4e55-128">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="d4e55-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="d4e55-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="d4e55-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




