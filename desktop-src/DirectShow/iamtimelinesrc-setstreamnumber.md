---
description: Il metodo SetStreamNumber specifica il flusso da leggere dal file di origine associato a questo oggetto di origine.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'Metodo IAMTimelineSrc:: SetStreamNumber (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330177"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a><span data-ttu-id="cb4f2-103">Metodo IAMTimelineSrc:: SetStreamNumber</span><span class="sxs-lookup"><span data-stu-id="cb4f2-103">IAMTimelineSrc::SetStreamNumber method</span></span>

> [!Note]  
> <span data-ttu-id="cb4f2-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-104">\[Deprecated.</span></span> <span data-ttu-id="cb4f2-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cb4f2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cb4f2-106">Il `SetStreamNumber` metodo specifica il flusso da leggere dal file di origine associato a questo oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-106">The `SetStreamNumber` method specifies which stream to read from the source file associated with this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb4f2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb4f2-107">Syntax</span></span>


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a><span data-ttu-id="cb4f2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb4f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb4f2-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="cb4f2-109">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="cb4f2-110">Il numero di flusso, dal set di flussi che corrispondono al tipo di supporto del gruppo padre.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-110">The stream number, from the set of streams matching the media type of the parent group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb4f2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb4f2-111">Return value</span></span>

<span data-ttu-id="cb4f2-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cb4f2-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb4f2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb4f2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb4f2-114">Remarks</span></span>

<span data-ttu-id="cb4f2-115">Il parametro *Val* specifica un numero di flusso dal set di flussi che corrisponde al tipo di supporto del gruppo padre, non dall'intero set di flussi nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-115">The *Val* parameter specifies a stream number from the set of streams that matches the parent group's media type, not from the entire set of streams in the source file.</span></span> <span data-ttu-id="cb4f2-116">Si supponga, ad esempio, che un file contenga due flussi video e due flussi audio.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-116">For example, For example, suppose that a file contains two video streams and two audio streams.</span></span> <span data-ttu-id="cb4f2-117">Se l'oggetto di origine si trova all'interno di un gruppo video, impostando *Val* su 0 viene selezionato il primo flusso video.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-117">If the source object is inside a video group, setting *Val* to 0 selects the first video stream.</span></span> <span data-ttu-id="cb4f2-118">Il chiamante è responsabile della specifica di un numero di flusso valido.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-118">The caller is responsible for specifying a valid stream number.</span></span>

<span data-ttu-id="cb4f2-119">Il valore predefinito per il numero di flusso è zero.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-119">The stream number defaults to zero.</span></span>

> [!Note]  
> <span data-ttu-id="cb4f2-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cb4f2-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cb4f2-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cb4f2-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="cb4f2-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb4f2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb4f2-123">Requirements</span></span>



| <span data-ttu-id="cb4f2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb4f2-124">Requirement</span></span> | <span data-ttu-id="cb4f2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cb4f2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4f2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb4f2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cb4f2-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb4f2-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cb4f2-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb4f2-128">Library</span></span><br/> | <dl> <span data-ttu-id="cb4f2-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb4f2-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb4f2-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb4f2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb4f2-131">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="cb4f2-131">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="cb4f2-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="cb4f2-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




