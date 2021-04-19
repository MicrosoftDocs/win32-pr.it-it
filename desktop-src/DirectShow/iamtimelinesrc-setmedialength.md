---
description: Il metodo SetMediaLength specifica la durata del file di origine.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'Metodo IAMTimelineSrc:: SetMediaLength (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332749"
---
# <a name="iamtimelinesrcsetmedialength-method"></a><span data-ttu-id="e9385-103">Metodo IAMTimelineSrc:: SetMediaLength</span><span class="sxs-lookup"><span data-stu-id="e9385-103">IAMTimelineSrc::SetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="e9385-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e9385-104">\[Deprecated.</span></span> <span data-ttu-id="e9385-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e9385-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e9385-106">Il `SetMediaLength` metodo specifica la durata del file di origine.</span><span class="sxs-lookup"><span data-stu-id="e9385-106">The `SetMediaLength` method specifies the duration of the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9385-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9385-107">Syntax</span></span>


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="e9385-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9385-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9385-109">*Length*</span><span class="sxs-lookup"><span data-stu-id="e9385-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="e9385-110">Lunghezza del supporto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="e9385-110">Media length, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9385-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9385-111">Return value</span></span>

<span data-ttu-id="e9385-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e9385-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9385-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e9385-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9385-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9385-114">Remarks</span></span>

<span data-ttu-id="e9385-115">È possibile evitare potenziali errori di rendering impostando la lunghezza del supporto prima di impostare l'ora di arresto del supporto.</span><span class="sxs-lookup"><span data-stu-id="e9385-115">You can avoid potential rendering errors by setting the media length before you set the media stop time.</span></span> <span data-ttu-id="e9385-116">Quando si imposta l'ora di arresto del supporto, DES verifica la lunghezza del supporto.</span><span class="sxs-lookup"><span data-stu-id="e9385-116">When you set the media stop time, DES checks it against the media length.</span></span>

<span data-ttu-id="e9385-117">Questo metodo non convalida il parametro *length* , ma il valore deve corrispondere alla durata effettiva del file di origine.</span><span class="sxs-lookup"><span data-stu-id="e9385-117">This method does not validate the *Length* parameter, but the value must equal the actual duration of the source file.</span></span> <span data-ttu-id="e9385-118">Ottenere la durata del file di origine chiamando [**IMediaDet:: Get \_ StreamLength**](imediadet-get-streamlength.md).</span><span class="sxs-lookup"><span data-stu-id="e9385-118">Obtain the source file duration by calling [**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md).</span></span>

> [!Note]  
> <span data-ttu-id="e9385-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e9385-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e9385-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e9385-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e9385-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e9385-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9385-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9385-122">Requirements</span></span>



| <span data-ttu-id="e9385-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9385-123">Requirement</span></span> | <span data-ttu-id="e9385-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e9385-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9385-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9385-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e9385-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9385-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e9385-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9385-127">Library</span></span><br/> | <dl> <span data-ttu-id="e9385-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9385-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9385-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9385-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9385-130">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="e9385-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="e9385-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e9385-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




