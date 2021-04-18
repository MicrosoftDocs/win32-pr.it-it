---
description: Il metodo GetSampleGrabber recupera un puntatore all'interfaccia ISampleGrabber, che consente a un'applicazione di recuperare singoli campioni da un flusso multimediale.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'Metodo IMediaDet:: GetSampleGrabber (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327825"
---
# <a name="imediadetgetsamplegrabber-method"></a><span data-ttu-id="9ca1d-103">Metodo IMediaDet:: GetSampleGrabber</span><span class="sxs-lookup"><span data-stu-id="9ca1d-103">IMediaDet::GetSampleGrabber method</span></span>

> [!Note]  
> <span data-ttu-id="9ca1d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9ca1d-104">\[Deprecated.</span></span> <span data-ttu-id="9ca1d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ca1d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9ca1d-106">Il `GetSampleGrabber` metodo recupera un puntatore all'interfaccia [**ISampleGrabber**](isamplegrabber.md) , che consente a un'applicazione di recuperare singoli campioni da un flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="9ca1d-106">The `GetSampleGrabber` method retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface, which enables an application to retrieve individual samples from a media stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca1d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ca1d-107">Syntax</span></span>


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="9ca1d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ca1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ca1d-109">*ppVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9ca1d-109">*ppVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ca1d-110">Riceve un puntatore all'interfaccia [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="9ca1d-110">Receives a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ca1d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ca1d-111">Return value</span></span>

<span data-ttu-id="9ca1d-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9ca1d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ca1d-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ca1d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca1d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ca1d-114">Remarks</span></span>

<span data-ttu-id="9ca1d-115">Chiamare [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="9ca1d-115">Call [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) before calling this method.</span></span> <span data-ttu-id="9ca1d-116">L'interfaccia [**ISampleGrabber**](isamplegrabber.md) consente di recuperare singoli esempi di supporti dal flusso.</span><span class="sxs-lookup"><span data-stu-id="9ca1d-116">The [**ISampleGrabber**](isamplegrabber.md) interface enables you to retrieve individual media samples from the stream.</span></span> <span data-ttu-id="9ca1d-117">Se è sufficiente una bitmap da un fotogramma video, chiamare invece il metodo [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) .</span><span class="sxs-lookup"><span data-stu-id="9ca1d-117">If you just need a bitmap from a video frame, call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method instead.</span></span> <span data-ttu-id="9ca1d-118">L'interfaccia **ISampleGrabber** è più flessibile, ma richiede più lavoro da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9ca1d-118">The **ISampleGrabber** interface is more flexible, but requires more work by the application.</span></span>

<span data-ttu-id="9ca1d-119">Se questo metodo ha esito positivo, l'interfaccia [**ISampleGrabber**](isamplegrabber.md) restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="9ca1d-119">If this method succeeds, the [**ISampleGrabber**](isamplegrabber.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="9ca1d-120">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="9ca1d-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="9ca1d-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="9ca1d-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9ca1d-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ca1d-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9ca1d-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9ca1d-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ca1d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ca1d-124">Requirements</span></span>



| <span data-ttu-id="9ca1d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ca1d-125">Requirement</span></span> | <span data-ttu-id="9ca1d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9ca1d-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca1d-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ca1d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9ca1d-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ca1d-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9ca1d-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ca1d-129">Library</span></span><br/> | <dl> <span data-ttu-id="9ca1d-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ca1d-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ca1d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ca1d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca1d-132">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="9ca1d-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="9ca1d-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="9ca1d-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




