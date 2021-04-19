---
description: Il metodo BufferCB è un metodo di callback che riceve un puntatore al buffer di esempio.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'Metodo ISampleGrabberCB:: BufferCB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332640"
---
# <a name="isamplegrabbercbbuffercb-method"></a><span data-ttu-id="0fda2-103">Metodo ISampleGrabberCB:: BufferCB</span><span class="sxs-lookup"><span data-stu-id="0fda2-103">ISampleGrabberCB::BufferCB method</span></span>

> [!Note]  
> <span data-ttu-id="0fda2-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0fda2-104">\[Deprecated.</span></span> <span data-ttu-id="0fda2-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0fda2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0fda2-106">Il metodo **BufferCB** è un metodo di callback che riceve un puntatore al buffer di esempio.</span><span class="sxs-lookup"><span data-stu-id="0fda2-106">The **BufferCB** method is a callback method that receives a pointer to the sample buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fda2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fda2-107">Syntax</span></span>


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a><span data-ttu-id="0fda2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fda2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fda2-109">*SampleTime*</span><span class="sxs-lookup"><span data-stu-id="0fda2-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="0fda2-110">Ora di inizio dell'esempio, in secondi.</span><span class="sxs-lookup"><span data-stu-id="0fda2-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="0fda2-111">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="0fda2-111">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="0fda2-112">Puntatore a un buffer che contiene i dati di esempio.</span><span class="sxs-lookup"><span data-stu-id="0fda2-112">Pointer to a buffer that contains the sample data.</span></span> <span data-ttu-id="0fda2-113">Il formato dei dati dipende dal tipo di supporto del PIN di input del grabber di esempio.</span><span class="sxs-lookup"><span data-stu-id="0fda2-113">The format of the data depends on the media type of the Sample Grabber's input pin.</span></span> <span data-ttu-id="0fda2-114">Per ottenere il tipo di supporto, chiamare [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="0fda2-114">To get the media type, call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fda2-115">*BufferLen*</span><span class="sxs-lookup"><span data-stu-id="0fda2-115">*BufferLen*</span></span> 
</dt> <dd>

<span data-ttu-id="0fda2-116">Lunghezza del buffer a cui punta *pbuffer* in byte.</span><span class="sxs-lookup"><span data-stu-id="0fda2-116">Length of the buffer pointed to by *pBuffer*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fda2-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fda2-117">Return value</span></span>

<span data-ttu-id="0fda2-118">Restituisce \_ OK se ha esito positivo o un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0fda2-118">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fda2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fda2-119">Remarks</span></span>

<span data-ttu-id="0fda2-120">Questo metodo di callback riceve un puntatore ai dati nell'esempio multimediale più recente.</span><span class="sxs-lookup"><span data-stu-id="0fda2-120">This callback method receives a pointer to the data in the most recent media sample.</span></span>

> [!Note]  
> <span data-ttu-id="0fda2-121">Questo metodo riceve un puntatore ai dati di esempio originali, non a una copia.</span><span class="sxs-lookup"><span data-stu-id="0fda2-121">This method receives a pointer to the original sample data, not a copy.</span></span> <span data-ttu-id="0fda2-122">La documentazione originale ha dichiarato erroneamente che *pbuffer* contiene una copia dei dati.</span><span class="sxs-lookup"><span data-stu-id="0fda2-122">The original documentation incorrectly stated that *pBuffer* contains a copy of the data.</span></span>

 

<span data-ttu-id="0fda2-123">Per impostare il callback, chiamare [**ISampleGrabber:: secallback**](isamplegrabber-setcallback.md).</span><span class="sxs-lookup"><span data-stu-id="0fda2-123">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="0fda2-124">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="0fda2-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0fda2-125">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0fda2-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0fda2-126">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0fda2-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0fda2-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fda2-127">Requirements</span></span>



| <span data-ttu-id="0fda2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fda2-128">Requirement</span></span> | <span data-ttu-id="0fda2-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0fda2-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fda2-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0fda2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0fda2-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fda2-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0fda2-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="0fda2-132">Library</span></span><br/> | <dl> <span data-ttu-id="0fda2-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fda2-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fda2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fda2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fda2-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="0fda2-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="0fda2-136">**Interfaccia ISampleGrabberCB**</span><span class="sxs-lookup"><span data-stu-id="0fda2-136">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




