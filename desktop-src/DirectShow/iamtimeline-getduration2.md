---
description: 'Il metodo GetDuration2 recupera la durata della sequenza temporale. Questo metodo è equivalente a IAMTimeline:: GetDuration, ma accetta un parametro di tipo Double.'
ms.assetid: 49f5eed3-7fab-4f08-b65c-300349b197cb
title: 'Metodo IAMTimeline:: GetDuration2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc840e642f6c08825f6f53869229e9cc27e87b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329145"
---
# <a name="iamtimelinegetduration2-method"></a><span data-ttu-id="3f125-104">Metodo IAMTimeline:: GetDuration2</span><span class="sxs-lookup"><span data-stu-id="3f125-104">IAMTimeline::GetDuration2 method</span></span>

> [!Note]  
> <span data-ttu-id="3f125-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="3f125-105">\[Deprecated.</span></span> <span data-ttu-id="3f125-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3f125-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3f125-107">Il `GetDuration2` metodo recupera la durata della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="3f125-107">The `GetDuration2` method retrieves the duration of the timeline.</span></span> <span data-ttu-id="3f125-108">Questo metodo è equivalente a [**IAMTimeline:: GetDuration**](iamtimeline-getduration.md), ma accetta un parametro di tipo **Double**.</span><span class="sxs-lookup"><span data-stu-id="3f125-108">This method is equivalent to [**IAMTimeline::GetDuration**](iamtimeline-getduration.md), but takes a parameter of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f125-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f125-109">Syntax</span></span>


```C++
HRESULT GetDuration2(
   double *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="3f125-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f125-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f125-111">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="3f125-111">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="3f125-112">Riceve la durata della sequenza temporale, in secondi frazionari.</span><span class="sxs-lookup"><span data-stu-id="3f125-112">Receives the duration of the timeline, in fractional seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f125-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f125-113">Return value</span></span>

<span data-ttu-id="3f125-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3f125-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f125-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f125-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f125-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f125-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3f125-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="3f125-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3f125-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f125-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3f125-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3f125-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f125-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f125-120">Requirements</span></span>



| <span data-ttu-id="3f125-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f125-121">Requirement</span></span> | <span data-ttu-id="3f125-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3f125-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f125-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f125-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3f125-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f125-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3f125-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f125-125">Library</span></span><br/> | <dl> <span data-ttu-id="3f125-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f125-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f125-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f125-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f125-128">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="3f125-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="3f125-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="3f125-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




