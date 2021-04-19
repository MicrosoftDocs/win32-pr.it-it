---
description: "Il metodo SetMediaTimes2 imposta l'ora di inizio e di fine del supporto. Questo metodo è equivalente a IAMTimelineSrc:: SetMediaTimes, ma accetta valori REFTIME."
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: 'Metodo IAMTimelineSrc:: SetMediaTimes2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4aa4f68a6fb93c329507edceea4e9665bfecd5f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332747"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a><span data-ttu-id="ba42c-104">Metodo IAMTimelineSrc:: SetMediaTimes2</span><span class="sxs-lookup"><span data-stu-id="ba42c-104">IAMTimelineSrc::SetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="ba42c-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ba42c-105">\[Deprecated.</span></span> <span data-ttu-id="ba42c-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ba42c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ba42c-107">Il `SetMediaTimes2` metodo imposta l'ora di inizio e di fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="ba42c-107">The `SetMediaTimes2` method sets the media stop and start times.</span></span> <span data-ttu-id="ba42c-108">Questo metodo è equivalente a [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md), ma accetta valori [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="ba42c-108">This method is equivalent to [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba42c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba42c-109">Syntax</span></span>


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="ba42c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba42c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba42c-111">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="ba42c-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="ba42c-112">Ora di inizio del supporto, in secondi.</span><span class="sxs-lookup"><span data-stu-id="ba42c-112">Media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ba42c-113">*Stop*</span><span class="sxs-lookup"><span data-stu-id="ba42c-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="ba42c-114">Tempo di arresto del supporto, in secondi.</span><span class="sxs-lookup"><span data-stu-id="ba42c-114">Media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba42c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba42c-115">Return value</span></span>

<span data-ttu-id="ba42c-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ba42c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba42c-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba42c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba42c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba42c-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ba42c-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="ba42c-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ba42c-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ba42c-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ba42c-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ba42c-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba42c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba42c-122">Requirements</span></span>



| <span data-ttu-id="ba42c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba42c-123">Requirement</span></span> | <span data-ttu-id="ba42c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ba42c-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba42c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba42c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ba42c-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba42c-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ba42c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="ba42c-127">Library</span></span><br/> | <dl> <span data-ttu-id="ba42c-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba42c-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba42c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba42c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba42c-130">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="ba42c-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="ba42c-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="ba42c-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




