---
description: Il metodo SetMediaTimes imposta l'ora di inizio e di fine del supporto.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'Metodo IAMTimelineSrc:: SetMediaTimes (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330179"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a><span data-ttu-id="9ebcf-103">Metodo IAMTimelineSrc:: SetMediaTimes</span><span class="sxs-lookup"><span data-stu-id="9ebcf-103">IAMTimelineSrc::SetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="9ebcf-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-104">\[Deprecated.</span></span> <span data-ttu-id="9ebcf-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ebcf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9ebcf-106">Il `SetMediaTimes` metodo imposta l'ora di inizio e di fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-106">The `SetMediaTimes` method sets the media stop and start times.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ebcf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ebcf-107">Syntax</span></span>


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="9ebcf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ebcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ebcf-109">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="9ebcf-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="9ebcf-110">Ora di inizio del supporto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-110">Media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="9ebcf-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="9ebcf-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="9ebcf-112">Tempo di arresto del supporto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-112">Media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ebcf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ebcf-113">Return value</span></span>

<span data-ttu-id="9ebcf-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ebcf-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ebcf-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ebcf-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ebcf-116">Remarks</span></span>

<span data-ttu-id="9ebcf-117">I tempi di supporto sono l'ora di arresto e di inizio rispetto al file multimediale originale.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-117">The media times are the stop and start times relative to the original media file.</span></span> <span data-ttu-id="9ebcf-118">Impostare sempre i tempi dei supporti quando si aggiunge un'origine video o audio alla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-118">Always set the media times when you add a video or audio source to the timeline.</span></span> <span data-ttu-id="9ebcf-119">In caso contrario, potrebbero verificarsi problemi di rendering.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-119">Otherwise, rendering problems might occur.</span></span> <span data-ttu-id="9ebcf-120">L'ora di arresto deve essere successiva all'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-120">The stop time must be greater than the start time.</span></span>

<span data-ttu-id="9ebcf-121">Per usare un frame ancora da un'origine video, impostare l'ora di arresto su un importo frazionario superiore all'ora di inizio, ad esempio 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-121">To use a still frame from a video source, set the stop time to a fractional amount more than the start time, such as 100 nanoseconds.</span></span> <span data-ttu-id="9ebcf-122">Se vengono impostate sullo stesso valore, viene generato un errore di rendering.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-122">Setting them to the same value causes a rendering error.</span></span>

<span data-ttu-id="9ebcf-123">Se la durata della sequenza temporale non corrisponde alla durata del supporto, l'origine si estende o compatta di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-123">If the timeline duration does not match the media duration, the source stretches or shrinks accordingly.</span></span> <span data-ttu-id="9ebcf-124">In questo modo il clip riproduca più lentamente o più velocemente rispetto alla velocità creata.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-124">This causes the clip to play slower or faster than the authored rate.</span></span> <span data-ttu-id="9ebcf-125">(Lo spostamento del pitch si verificherà in un'origine audio.) Per ulteriori informazioni, vedere [tempo in servizi di modifica DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="9ebcf-125">(Pitch shifting will occur in an audio source.) For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="9ebcf-126">È possibile specificare la durata del file di origine chiamando il metodo [**SetMediaLength**](iamtimelinesrc-setmedialength.md) .</span><span class="sxs-lookup"><span data-stu-id="9ebcf-126">You can specify the duration of the source file by calling the [**SetMediaLength**](iamtimelinesrc-setmedialength.md) method.</span></span> <span data-ttu-id="9ebcf-127">Se si imposta un'ora di arresto del supporto che supera la durata, DES tronca l'ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-127">If you set a media stop time that exceeds the duration, DES truncates the stop time.</span></span>

> [!Note]  
> <span data-ttu-id="9ebcf-128">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9ebcf-129">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ebcf-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9ebcf-130">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9ebcf-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ebcf-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ebcf-131">Requirements</span></span>



| <span data-ttu-id="9ebcf-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ebcf-132">Requirement</span></span> | <span data-ttu-id="9ebcf-133">Valore</span><span class="sxs-lookup"><span data-stu-id="9ebcf-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebcf-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ebcf-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9ebcf-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ebcf-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9ebcf-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ebcf-136">Library</span></span><br/> | <dl> <span data-ttu-id="9ebcf-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ebcf-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ebcf-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ebcf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ebcf-139">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="9ebcf-139">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="9ebcf-140">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="9ebcf-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




