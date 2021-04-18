---
description: Il metodo SetSmartRecompressFormat specifica un formato di compressione video da usare per la ricompressione intelligente.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'Metodo IAMTimelineGroup:: SetSmartRecompressFormat (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331622"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a><span data-ttu-id="69e28-103">Metodo IAMTimelineGroup:: SetSmartRecompressFormat</span><span class="sxs-lookup"><span data-stu-id="69e28-103">IAMTimelineGroup::SetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="69e28-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="69e28-104">\[Deprecated.</span></span> <span data-ttu-id="69e28-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="69e28-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="69e28-106">Il `SetSmartRecompressFormat` metodo specifica un formato di compressione video da usare per la ricompressione intelligente.</span><span class="sxs-lookup"><span data-stu-id="69e28-106">The `SetSmartRecompressFormat` method specifies a video compression format to use for smart recompression.</span></span>

<span data-ttu-id="69e28-107">La ricompressione intelligente non è supportata per i gruppi audio.</span><span class="sxs-lookup"><span data-stu-id="69e28-107">Smart recompression is not supported for audio groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e28-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69e28-108">Syntax</span></span>


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="69e28-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="69e28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69e28-110">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="69e28-110">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="69e28-111">Puntatore a una struttura che descrive il formato di compressione.</span><span class="sxs-lookup"><span data-stu-id="69e28-111">Pointer to a structure describing the compression format.</span></span> <span data-ttu-id="69e28-112">Attualmente, solo la struttura [**SCompFmt0**](scompfmt0.md) è valida.</span><span class="sxs-lookup"><span data-stu-id="69e28-112">Currently, only the [**SCompFmt0**](scompfmt0.md) structure is valid.</span></span> <span data-ttu-id="69e28-113">È necessario eseguire il cast di questo parametro a un puntatore di tipo **Long**.</span><span class="sxs-lookup"><span data-stu-id="69e28-113">You must cast this parameter to a pointer of type **long**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69e28-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69e28-114">Return value</span></span>

<span data-ttu-id="69e28-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="69e28-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69e28-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69e28-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="69e28-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="69e28-117">Remarks</span></span>

<span data-ttu-id="69e28-118">Prima di chiamare questo metodo, chiamare il metodo [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) sullo stesso gruppo, per specificare un formato non compresso.</span><span class="sxs-lookup"><span data-stu-id="69e28-118">Before calling this method, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method on the same group, to specify an uncompressed format.</span></span>

<span data-ttu-id="69e28-119">Se il `SetSmartRecompressFormat` metodo ha esito positivo, è possibile usare il motore di rendering intelligente per generare un flusso video compresso.</span><span class="sxs-lookup"><span data-stu-id="69e28-119">If the `SetSmartRecompressFormat` method succeeds, you can use the Smart Render Engine to output a compressed video stream.</span></span> <span data-ttu-id="69e28-120">Il video compresso avrà la larghezza, l'altezza e la frequenza dei fotogrammi specificati nel parametro *pFormat* .</span><span class="sxs-lookup"><span data-stu-id="69e28-120">The compressed video will have the width, height, and frame rate that was specified in the *pFormat* parameter.</span></span> <span data-ttu-id="69e28-121">Questi valori eseguiranno l'override di quelli specificati per il formato non compresso nel metodo **SetMediaType** .</span><span class="sxs-lookup"><span data-stu-id="69e28-121">These values will override those given for the uncompressed format in the **SetMediaType** method.</span></span> <span data-ttu-id="69e28-122">Tuttavia, per sfruttare i vantaggi della ricompressione intelligente, i due formati devono corrispondere.</span><span class="sxs-lookup"><span data-stu-id="69e28-122">However, to get the benefits of smart recompression, the two formats should match.</span></span> <span data-ttu-id="69e28-123">In altre parole, i formati compressi e non compressi dovrebbero avere la stessa altezza, larghezza e frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="69e28-123">In other words, the compressed and uncompressed formats should have the same height, width, and frame rate.</span></span>

<span data-ttu-id="69e28-124">Se il motore di rendering intelligente non riesce a produrre il formato compresso, produrrà invece un flusso video non compresso.</span><span class="sxs-lookup"><span data-stu-id="69e28-124">If the Smart Render Engine is unable to produce the compressed format, it will produce an uncompressed video stream instead.</span></span> <span data-ttu-id="69e28-125">In tal caso, il motore di rendering intelligente segnala un \_ \_ errore di \_ rendering del compressore di ID Dex \_ durante il metodo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="69e28-125">If that occurs, the Smart Render Engine reports a DEX\_IDS\_CANT\_FIND\_COMPRESSOR rendering error during the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="69e28-126">L'applicazione può rilevare questo errore tramite il metodo [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) .</span><span class="sxs-lookup"><span data-stu-id="69e28-126">The application can catch this error through the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="69e28-127">Per ulteriori informazioni, vedere [registrazione degli errori](logging-errors.md) e [rendering degli errori](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="69e28-127">(For more information, see [Logging Errors](logging-errors.md) and [Rendering Errors](rendering-errors.md).)</span></span>

<span data-ttu-id="69e28-128">Il formato di ricompressione intelligente non è permanente.</span><span class="sxs-lookup"><span data-stu-id="69e28-128">The smart recompression format is not persistent.</span></span> <span data-ttu-id="69e28-129">Se in un'applicazione viene utilizzata la ricompressione intelligente, è necessario impostare il formato di ricompressione ogni volta che viene caricato un file di progetto.</span><span class="sxs-lookup"><span data-stu-id="69e28-129">If an application uses smart recompression, it must set the recompression format whenever it loads a project file.</span></span>

> [!Note]  
> <span data-ttu-id="69e28-130">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="69e28-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="69e28-131">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="69e28-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="69e28-132">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="69e28-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="69e28-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69e28-133">Requirements</span></span>



| <span data-ttu-id="69e28-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="69e28-134">Requirement</span></span> | <span data-ttu-id="69e28-135">Valore</span><span class="sxs-lookup"><span data-stu-id="69e28-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69e28-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69e28-136">Header</span></span><br/>  | <dl> <span data-ttu-id="69e28-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="69e28-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="69e28-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="69e28-138">Library</span></span><br/> | <dl> <span data-ttu-id="69e28-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69e28-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69e28-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69e28-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e28-141">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="69e28-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="69e28-142">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="69e28-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="69e28-143">Motore di rendering intelligente</span><span class="sxs-lookup"><span data-stu-id="69e28-143">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> <dt>

[<span data-ttu-id="69e28-144">Scrittura di un progetto in un file</span><span class="sxs-lookup"><span data-stu-id="69e28-144">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




