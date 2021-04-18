---
description: L'interfaccia ISampleGrabber viene esposta dal filtro Grabber di esempio. Consente a un'applicazione di recuperare singoli esempi di supporti mentre passano attraverso il grafico del filtro.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Interfaccia ISampleGrabber (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324414"
---
# <a name="isamplegrabber-interface"></a><span data-ttu-id="67fc9-104">Interfaccia ISampleGrabber</span><span class="sxs-lookup"><span data-stu-id="67fc9-104">ISampleGrabber interface</span></span>

> [!Note]  
> <span data-ttu-id="67fc9-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="67fc9-105">\[Deprecated.</span></span> <span data-ttu-id="67fc9-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="67fc9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="67fc9-107">L'interfaccia **ISampleGrabber** viene esposta dal filtro [**grabber di esempio**](sample-grabber-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="67fc9-107">The **ISampleGrabber** interface is exposed by the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="67fc9-108">Consente a un'applicazione di recuperare singoli esempi di supporti mentre passano attraverso il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="67fc9-108">It enables an application to retrieve individual media samples as they move through the filter graph.</span></span>

## <a name="members"></a><span data-ttu-id="67fc9-109">Membri</span><span class="sxs-lookup"><span data-stu-id="67fc9-109">Members</span></span>

<span data-ttu-id="67fc9-110">L'interfaccia **ISampleGrabber** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="67fc9-110">The **ISampleGrabber** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="67fc9-111">**ISampleGrabber** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="67fc9-111">**ISampleGrabber** also has these types of members:</span></span>

-   [<span data-ttu-id="67fc9-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="67fc9-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67fc9-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="67fc9-113">Methods</span></span>

<span data-ttu-id="67fc9-114">L'interfaccia **ISampleGrabber** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="67fc9-114">The **ISampleGrabber** interface has these methods.</span></span>



| <span data-ttu-id="67fc9-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="67fc9-115">Method</span></span>                                                                | <span data-ttu-id="67fc9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67fc9-116">Description</span></span>                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67fc9-117">**GetConnectedMediaType**</span><span class="sxs-lookup"><span data-stu-id="67fc9-117">**GetConnectedMediaType**</span></span>](isamplegrabber-getconnectedmediatype.md) | <span data-ttu-id="67fc9-118">Recupera il tipo di supporto per la connessione sul pin di input di Sample Grabber.</span><span class="sxs-lookup"><span data-stu-id="67fc9-118">Retrieves the media type for the connection on the input pin of Sample Grabber.</span></span><br/>                                        |
| [<span data-ttu-id="67fc9-119">**GetCurrentBuffer**</span><span class="sxs-lookup"><span data-stu-id="67fc9-119">**GetCurrentBuffer**</span></span>](isamplegrabber-getcurrentbuffer.md)           | <span data-ttu-id="67fc9-120">Recupera una copia dell'esempio che il filtro ha ricevuto più di recente.</span><span class="sxs-lookup"><span data-stu-id="67fc9-120">Retrieves a copy of the sample that the filter received most recently.</span></span><br/>                                                 |
| [<span data-ttu-id="67fc9-121">**GetCurrentSample**</span><span class="sxs-lookup"><span data-stu-id="67fc9-121">**GetCurrentSample**</span></span>](isamplegrabber-getcurrentsample.md)           | <span data-ttu-id="67fc9-122">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="67fc9-122">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="67fc9-123">**SetBufferSamples**</span><span class="sxs-lookup"><span data-stu-id="67fc9-123">**SetBufferSamples**</span></span>](isamplegrabber-setbuffersamples.md)           | <span data-ttu-id="67fc9-124">Specifica se copiare i dati di esempio in un buffer mentre passa attraverso il filtro.</span><span class="sxs-lookup"><span data-stu-id="67fc9-124">Specifies whether to copy sample data into a buffer as it goes through the filter.</span></span><br/>                                     |
| [<span data-ttu-id="67fc9-125">**SetCallback**</span><span class="sxs-lookup"><span data-stu-id="67fc9-125">**SetCallback**</span></span>](isamplegrabber-setcallback.md)                     | <span data-ttu-id="67fc9-126">Specifica un metodo di callback da chiamare sugli esempi in arrivo.</span><span class="sxs-lookup"><span data-stu-id="67fc9-126">Specifies a callback method to call on incoming samples.</span></span><br/>                                                               |
| [<span data-ttu-id="67fc9-127">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="67fc9-127">**SetMediaType**</span></span>](isamplegrabber-setmediatype.md)                   | <span data-ttu-id="67fc9-128">Specifica il tipo di supporto per la connessione sul pin di input del grabber di esempio.</span><span class="sxs-lookup"><span data-stu-id="67fc9-128">Specifies the media type for the connection on the input pin of the Sample Grabber.</span></span><br/>                                    |
| [<span data-ttu-id="67fc9-129">**SetOneShot**</span><span class="sxs-lookup"><span data-stu-id="67fc9-129">**SetOneShot**</span></span>](isamplegrabber-setoneshot.md)                       | <span data-ttu-id="67fc9-130">Specifica se il filtro [**grabber di esempio**](sample-grabber-filter.md) si arresta dopo la ricezione di un campione da parte del filtro.</span><span class="sxs-lookup"><span data-stu-id="67fc9-130">Specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67fc9-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="67fc9-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="67fc9-132">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="67fc9-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="67fc9-133">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="67fc9-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="67fc9-134">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="67fc9-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67fc9-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67fc9-135">Requirements</span></span>



| <span data-ttu-id="67fc9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="67fc9-136">Requirement</span></span> | <span data-ttu-id="67fc9-137">Valore</span><span class="sxs-lookup"><span data-stu-id="67fc9-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67fc9-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67fc9-138">Header</span></span><br/>  | <dl> <span data-ttu-id="67fc9-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="67fc9-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="67fc9-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="67fc9-140">Library</span></span><br/> | <dl> <span data-ttu-id="67fc9-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67fc9-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67fc9-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67fc9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67fc9-143">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="67fc9-143">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 
