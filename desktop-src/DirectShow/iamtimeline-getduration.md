---
description: Il metodo GetDuration recupera la durata della sequenza temporale.
ms.assetid: d60269b8-597a-4ba4-932a-54b4a36e9a7a
title: 'Metodo IAMTimeline:: GetDuration (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98257c40bf2072a2b8881a4744cdbe6d3a4e7df5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327426"
---
# <a name="iamtimelinegetduration-method"></a><span data-ttu-id="57bca-103">Metodo IAMTimeline:: GetDuration</span><span class="sxs-lookup"><span data-stu-id="57bca-103">IAMTimeline::GetDuration method</span></span>

> [!Note]  
> <span data-ttu-id="57bca-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="57bca-104">\[Deprecated.</span></span> <span data-ttu-id="57bca-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="57bca-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="57bca-106">Il `GetDuration` metodo recupera la durata della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="57bca-106">The `GetDuration` method retrieves the duration of the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="57bca-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57bca-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   REFERENCE_TIME *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="57bca-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="57bca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57bca-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="57bca-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="57bca-110">Riceve la durata della sequenza temporale, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="57bca-110">Receives the duration of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57bca-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57bca-111">Return value</span></span>

<span data-ttu-id="57bca-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="57bca-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57bca-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57bca-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57bca-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="57bca-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="57bca-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="57bca-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="57bca-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="57bca-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="57bca-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="57bca-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57bca-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57bca-118">Requirements</span></span>



| <span data-ttu-id="57bca-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="57bca-119">Requirement</span></span> | <span data-ttu-id="57bca-120">Valore</span><span class="sxs-lookup"><span data-stu-id="57bca-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57bca-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57bca-121">Header</span></span><br/>  | <dl> <span data-ttu-id="57bca-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="57bca-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="57bca-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="57bca-123">Library</span></span><br/> | <dl> <span data-ttu-id="57bca-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57bca-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57bca-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57bca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57bca-126">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="57bca-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="57bca-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="57bca-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




