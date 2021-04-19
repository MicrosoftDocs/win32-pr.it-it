---
description: Il metodo SampleCB è un metodo di callback che riceve un puntatore all'esempio multimediale.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'Metodo ISampleGrabberCB:: SampleCB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e66f4a43666add7a5d6cb579fcf15f0fc1ec0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332024"
---
# <a name="isamplegrabbercbsamplecb-method"></a><span data-ttu-id="700ba-103">Metodo ISampleGrabberCB:: SampleCB</span><span class="sxs-lookup"><span data-stu-id="700ba-103">ISampleGrabberCB::SampleCB method</span></span>

> [!Note]  
> <span data-ttu-id="700ba-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="700ba-104">\[Deprecated.</span></span> <span data-ttu-id="700ba-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="700ba-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="700ba-106">Il `SampleCB` metodo è un metodo di callback che riceve un puntatore all'esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="700ba-106">The `SampleCB` method is a callback method that receives a pointer to the media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="700ba-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="700ba-107">Syntax</span></span>


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="700ba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="700ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="700ba-109">*SampleTime*</span><span class="sxs-lookup"><span data-stu-id="700ba-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="700ba-110">Ora di inizio dell'esempio, in secondi.</span><span class="sxs-lookup"><span data-stu-id="700ba-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="700ba-111">*pSample*</span><span class="sxs-lookup"><span data-stu-id="700ba-111">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="700ba-112">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="700ba-112">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="700ba-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="700ba-113">Return value</span></span>

<span data-ttu-id="700ba-114">Restituisce \_ OK se ha esito positivo o un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="700ba-114">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="700ba-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="700ba-115">Remarks</span></span>

<span data-ttu-id="700ba-116">Per impostare il callback, chiamare [**ISampleGrabber:: secallback**](isamplegrabber-setcallback.md).</span><span class="sxs-lookup"><span data-stu-id="700ba-116">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="700ba-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="700ba-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="700ba-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="700ba-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="700ba-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="700ba-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="700ba-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="700ba-120">Requirements</span></span>



| <span data-ttu-id="700ba-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="700ba-121">Requirement</span></span> | <span data-ttu-id="700ba-122">Valore</span><span class="sxs-lookup"><span data-stu-id="700ba-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="700ba-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="700ba-123">Header</span></span><br/>  | <dl> <span data-ttu-id="700ba-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="700ba-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="700ba-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="700ba-125">Library</span></span><br/> | <dl> <span data-ttu-id="700ba-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="700ba-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="700ba-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="700ba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700ba-128">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="700ba-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="700ba-129">**Interfaccia ISampleGrabberCB**</span><span class="sxs-lookup"><span data-stu-id="700ba-129">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




