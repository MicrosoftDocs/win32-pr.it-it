---
description: Il metodo SrcAdd aggiunge un'origine alla traccia.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'Metodo IAMTimelineTrack:: SrcAdd (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325619"
---
# <a name="iamtimelinetracksrcadd-method"></a><span data-ttu-id="881ea-103">Metodo IAMTimelineTrack:: SrcAdd</span><span class="sxs-lookup"><span data-stu-id="881ea-103">IAMTimelineTrack::SrcAdd method</span></span>

> [!Note]  
> <span data-ttu-id="881ea-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="881ea-104">\[Deprecated.</span></span> <span data-ttu-id="881ea-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="881ea-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="881ea-106">Il `SrcAdd` metodo aggiunge un'origine alla traccia.</span><span class="sxs-lookup"><span data-stu-id="881ea-106">The `SrcAdd` method adds a source to the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="881ea-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="881ea-107">Syntax</span></span>


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="881ea-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="881ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="881ea-109">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="881ea-109">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="881ea-110">Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="881ea-110">Pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="881ea-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="881ea-111">Return value</span></span>

<span data-ttu-id="881ea-112">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="881ea-112">Returns S\_OK if successful.</span></span> <span data-ttu-id="881ea-113">Restituisce E \_ nointerface se l'oggetto non è un oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="881ea-113">Returns E\_NOINTERFACE if the object is not a source object.</span></span> <span data-ttu-id="881ea-114">In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="881ea-114">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="881ea-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="881ea-115">Remarks</span></span>

<span data-ttu-id="881ea-116">Impostare l'ora di inizio e di fine dell'origine prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="881ea-116">Set the source's start and stop times before calling this method.</span></span> <span data-ttu-id="881ea-117">(Chiamare [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md).)</span><span class="sxs-lookup"><span data-stu-id="881ea-117">(Call [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md).)</span></span>

<span data-ttu-id="881ea-118">Attualmente, DES non può eseguire contemporaneamente il rendering di più di 75 origini compresse con codec di Gestione compressione video (VCM).</span><span class="sxs-lookup"><span data-stu-id="881ea-118">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="881ea-119">Inoltre, se il progetto contiene più di 75 origini di questo tipo, è necessario utilizzare la riconnessione dinamica oppure il programma DES non può visualizzare in anteprima il progetto.</span><span class="sxs-lookup"><span data-stu-id="881ea-119">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="881ea-120">Per ulteriori informazioni, vedere [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="881ea-120">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="881ea-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="881ea-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="881ea-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="881ea-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="881ea-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="881ea-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="881ea-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="881ea-124">Requirements</span></span>



| <span data-ttu-id="881ea-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="881ea-125">Requirement</span></span> | <span data-ttu-id="881ea-126">Valore</span><span class="sxs-lookup"><span data-stu-id="881ea-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="881ea-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="881ea-127">Header</span></span><br/>  | <dl> <span data-ttu-id="881ea-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="881ea-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="881ea-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="881ea-129">Library</span></span><br/> | <dl> <span data-ttu-id="881ea-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="881ea-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="881ea-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="881ea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="881ea-132">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="881ea-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="881ea-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="881ea-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




