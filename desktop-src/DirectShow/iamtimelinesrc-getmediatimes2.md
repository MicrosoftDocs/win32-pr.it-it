---
description: 'Il metodo GetMediaTimes2 recupera le ore di inizio e di fine del supporto. Questo metodo è equivalente a IAMTimelineSrc:: GetMediaTimes, ma accetta valori REFTIME.'
ms.assetid: c3961c2c-7198-44bd-8734-7301a7c5b21e
title: 'Metodo IAMTimelineSrc:: GetMediaTimes2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 779876e542ab51914725b326a0e3b217b893f254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330185"
---
# <a name="iamtimelinesrcgetmediatimes2-method"></a><span data-ttu-id="2d351-104">Metodo IAMTimelineSrc:: GetMediaTimes2</span><span class="sxs-lookup"><span data-stu-id="2d351-104">IAMTimelineSrc::GetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="2d351-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="2d351-105">\[Deprecated.</span></span> <span data-ttu-id="2d351-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2d351-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2d351-107">Il `GetMediaTimes2` metodo recupera le ore di inizio e di fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="2d351-107">The `GetMediaTimes2` method retrieves the media start and stop times.</span></span> <span data-ttu-id="2d351-108">Questo metodo è equivalente a [**IAMTimelineSrc:: GetMediaTimes**](iamtimelinesrc-getmediatimes.md), ma accetta valori [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="2d351-108">This method is equivalent to [**IAMTimelineSrc::GetMediaTimes**](iamtimelinesrc-getmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d351-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d351-109">Syntax</span></span>


```C++
HRESULT GetMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="2d351-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d351-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d351-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="2d351-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="2d351-112">Riceve l'ora di inizio del supporto, in secondi.</span><span class="sxs-lookup"><span data-stu-id="2d351-112">Receives the media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="2d351-113">*pStop*</span><span class="sxs-lookup"><span data-stu-id="2d351-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="2d351-114">Riceve l'ora di arresto del supporto, in secondi.</span><span class="sxs-lookup"><span data-stu-id="2d351-114">Receives the media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d351-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d351-115">Return value</span></span>

<span data-ttu-id="2d351-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2d351-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d351-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2d351-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d351-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d351-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2d351-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="2d351-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2d351-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2d351-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2d351-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2d351-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d351-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d351-122">Requirements</span></span>



| <span data-ttu-id="2d351-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d351-123">Requirement</span></span> | <span data-ttu-id="2d351-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2d351-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d351-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d351-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2d351-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d351-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2d351-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d351-127">Library</span></span><br/> | <dl> <span data-ttu-id="2d351-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d351-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d351-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d351-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d351-130">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="2d351-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="2d351-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="2d351-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




