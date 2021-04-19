---
description: Il metodo GetMediaTimes recupera le ore di inizio e di fine del supporto.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: 'Metodo IAMTimelineSrc:: GetMediaTimes (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa6e9cbb69da504a929e23722068583489063b9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332765"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a><span data-ttu-id="2e27c-103">Metodo IAMTimelineSrc:: GetMediaTimes</span><span class="sxs-lookup"><span data-stu-id="2e27c-103">IAMTimelineSrc::GetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="2e27c-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="2e27c-104">\[Deprecated.</span></span> <span data-ttu-id="2e27c-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2e27c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2e27c-106">Il `GetMediaTimes` metodo recupera le ore di inizio e di fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="2e27c-106">The `GetMediaTimes` method retrieves the media start and stop times.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e27c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e27c-107">Syntax</span></span>


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="2e27c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e27c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e27c-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="2e27c-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="2e27c-110">Riceve l'ora di inizio del supporto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="2e27c-110">Receives the media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="2e27c-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="2e27c-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="2e27c-112">Riceve l'ora di arresto del supporto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="2e27c-112">Receives the media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e27c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e27c-113">Return value</span></span>

<span data-ttu-id="2e27c-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2e27c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e27c-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e27c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e27c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e27c-116">Remarks</span></span>

<span data-ttu-id="2e27c-117">I tempi dei supporti sono relativi al file multimediale originale.</span><span class="sxs-lookup"><span data-stu-id="2e27c-117">The media times are relative to the original media file.</span></span> <span data-ttu-id="2e27c-118">Per ulteriori informazioni, vedere [tempo in servizi di modifica DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="2e27c-118">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="2e27c-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="2e27c-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2e27c-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2e27c-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2e27c-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2e27c-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e27c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e27c-122">Requirements</span></span>



| <span data-ttu-id="2e27c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e27c-123">Requirement</span></span> | <span data-ttu-id="2e27c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2e27c-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e27c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e27c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2e27c-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e27c-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2e27c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="2e27c-127">Library</span></span><br/> | <dl> <span data-ttu-id="2e27c-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e27c-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e27c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e27c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e27c-130">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="2e27c-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="2e27c-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="2e27c-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




