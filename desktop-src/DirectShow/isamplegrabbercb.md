---
description: "L'interfaccia ISampleGrabberCB fornisce metodi di callback per il metodo ISampleGrabber:: secallback. Se l'applicazione chiama tale metodo, deve implementare questa interfaccia. Per ulteriori informazioni, vedere ISampleGrabber."
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Interfaccia ISampleGrabberCB (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326272"
---
# <a name="isamplegrabbercb-interface"></a><span data-ttu-id="751b5-105">Interfaccia ISampleGrabberCB</span><span class="sxs-lookup"><span data-stu-id="751b5-105">ISampleGrabberCB interface</span></span>

> [!Note]  
> <span data-ttu-id="751b5-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="751b5-106">\[Deprecated.</span></span> <span data-ttu-id="751b5-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="751b5-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="751b5-108">L' `ISampleGrabberCB` interfaccia fornisce metodi di callback per il metodo [**ISampleGrabber:: secallback**](isamplegrabber-setcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="751b5-108">The `ISampleGrabberCB` interface provides callback methods for the [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) method.</span></span> <span data-ttu-id="751b5-109">Se l'applicazione chiama tale metodo, deve implementare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="751b5-109">If your application calls that method, it must implement this interface.</span></span> <span data-ttu-id="751b5-110">Per ulteriori informazioni, vedere [**ISampleGrabber**](isamplegrabber.md).</span><span class="sxs-lookup"><span data-stu-id="751b5-110">For more information, see [**ISampleGrabber**](isamplegrabber.md).</span></span>

## <a name="members"></a><span data-ttu-id="751b5-111">Membri</span><span class="sxs-lookup"><span data-stu-id="751b5-111">Members</span></span>

<span data-ttu-id="751b5-112">L'interfaccia **ISampleGrabberCB** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="751b5-112">The **ISampleGrabberCB** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="751b5-113">**ISampleGrabberCB** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="751b5-113">**ISampleGrabberCB** also has these types of members:</span></span>

-   [<span data-ttu-id="751b5-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="751b5-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="751b5-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="751b5-115">Methods</span></span>

<span data-ttu-id="751b5-116">L'interfaccia **ISampleGrabberCB** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="751b5-116">The **ISampleGrabberCB** interface has these methods.</span></span>



| <span data-ttu-id="751b5-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="751b5-117">Method</span></span>                                        | <span data-ttu-id="751b5-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="751b5-118">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="751b5-119">**BufferCB**</span><span class="sxs-lookup"><span data-stu-id="751b5-119">**BufferCB**</span></span>](isamplegrabbercb-buffercb.md) | <span data-ttu-id="751b5-120">Metodo di callback che riceve un puntatore al buffer di esempio.</span><span class="sxs-lookup"><span data-stu-id="751b5-120">Callback method that receives a pointer to the sample buffer.</span></span><br/> |
| [<span data-ttu-id="751b5-121">**SampleCB**</span><span class="sxs-lookup"><span data-stu-id="751b5-121">**SampleCB**</span></span>](isamplegrabbercb-samplecb.md) | <span data-ttu-id="751b5-122">Metodo di callback che riceve un puntatore all'esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="751b5-122">Callback method that receives a pointer to the media sample.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="751b5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="751b5-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="751b5-124">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="751b5-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="751b5-125">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="751b5-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="751b5-126">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="751b5-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="751b5-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="751b5-127">Requirements</span></span>



| <span data-ttu-id="751b5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="751b5-128">Requirement</span></span> | <span data-ttu-id="751b5-129">Valore</span><span class="sxs-lookup"><span data-stu-id="751b5-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="751b5-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="751b5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="751b5-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="751b5-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="751b5-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="751b5-132">Library</span></span><br/> | <dl> <span data-ttu-id="751b5-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="751b5-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
