---
description: Il metodo EnterBitmapGrabMode passa il rilevatore di supporti alla modalità di recupero bitmap e cerca il grafico del filtro a un orario specificato.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'Metodo IMediaDet:: EnterBitmapGrabMode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328330"
---
# <a name="imediadetenterbitmapgrabmode-method"></a><span data-ttu-id="20493-103">Metodo IMediaDet:: EnterBitmapGrabMode</span><span class="sxs-lookup"><span data-stu-id="20493-103">IMediaDet::EnterBitmapGrabMode method</span></span>

> [!Note]  
> <span data-ttu-id="20493-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="20493-104">\[Deprecated.</span></span> <span data-ttu-id="20493-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="20493-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="20493-106">Il `EnterBitmapGrabMode` metodo passa il rilevatore di supporti alla modalità di recupero bitmap e cerca il grafico del filtro a un orario specificato.</span><span class="sxs-lookup"><span data-stu-id="20493-106">The `EnterBitmapGrabMode` method switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="20493-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20493-107">Syntax</span></span>


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a><span data-ttu-id="20493-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="20493-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20493-109">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="20493-109">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="20493-110">Tempo, in secondi, in cui il grafico Cerca.</span><span class="sxs-lookup"><span data-stu-id="20493-110">Time, in seconds, to which the graph seeks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20493-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20493-111">Return value</span></span>

<span data-ttu-id="20493-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="20493-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="20493-113">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="20493-113">Possible values include the following:</span></span>



| <span data-ttu-id="20493-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="20493-114">Return code</span></span>                                                                                             | <span data-ttu-id="20493-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20493-115">Description</span></span>                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="20493-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="20493-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="20493-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="20493-117">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="20493-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="20493-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="20493-119">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="20493-119">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="20493-120"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="20493-120"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="20493-121">Il file di origine non dispone di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="20493-121">The source file does not have a video stream.</span></span><br/> |
| <dl> <span data-ttu-id="20493-122"><dt>**tempo di VFW \_ E \_ \_ scaduto**</dt></span><span class="sxs-lookup"><span data-stu-id="20493-122"><dt>**VFW\_E\_TIME\_EXPIRED**</dt></span></span> </dl>    | <span data-ttu-id="20493-123">Timeout del comando seek.</span><span class="sxs-lookup"><span data-stu-id="20493-123">Seek command timed out.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="20493-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="20493-124">Remarks</span></span>

<span data-ttu-id="20493-125">Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="20493-125">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="20493-126">Questo metodo inserisce il filtro [**grabber di esempio**](sample-grabber-filter.md) nel grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="20493-126">This method inserts the [**Sample Grabber**](sample-grabber-filter.md) filter into the filter graph.</span></span> <span data-ttu-id="20493-127">È quindi possibile chiamare [**IMediaDet:: GetSampleGrabber**](imediadet-getsamplegrabber.md) per ottenere un puntatore all'interfaccia [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="20493-127">You can then call [**IMediaDet::GetSampleGrabber**](imediadet-getsamplegrabber.md) to obtain a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span> <span data-ttu-id="20493-128">Quando il rilevamento multimediale passa alla modalità di cattura della bitmap, i vari metodi informativi in **IMediaDet** non funzionano.</span><span class="sxs-lookup"><span data-stu-id="20493-128">Once the media detector enters bitmap grab mode, the various informational methods in **IMediaDet** do not work.</span></span>

<span data-ttu-id="20493-129">I metodi [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md) inseriscono anche il rilevatore multimediale in modalità di cattura bitmap.</span><span class="sxs-lookup"><span data-stu-id="20493-129">The [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md) methods also put the media detector into bitmap grab mode.</span></span>

> [!Note]  
> <span data-ttu-id="20493-130">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="20493-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="20493-131">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="20493-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="20493-132">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="20493-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20493-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20493-133">Requirements</span></span>



| <span data-ttu-id="20493-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="20493-134">Requirement</span></span> | <span data-ttu-id="20493-135">Valore</span><span class="sxs-lookup"><span data-stu-id="20493-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20493-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20493-136">Header</span></span><br/>  | <dl> <span data-ttu-id="20493-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="20493-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="20493-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="20493-138">Library</span></span><br/> | <dl> <span data-ttu-id="20493-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20493-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20493-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20493-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20493-141">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="20493-141">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="20493-142">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="20493-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




