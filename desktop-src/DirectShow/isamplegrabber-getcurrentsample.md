---
description: Il metodo GetCurrentSample non è implementato.
ms.assetid: 0c903498-3c1d-4e95-a797-ca8cfded25f2
title: 'Metodo ISampleGrabber:: GetCurrentSample (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentSample
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9a21f50f84f030502cfd3243d36595e465e1b85b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330508"
---
# <a name="isamplegrabbergetcurrentsample-method"></a><span data-ttu-id="96135-103">Metodo ISampleGrabber:: GetCurrentSample</span><span class="sxs-lookup"><span data-stu-id="96135-103">ISampleGrabber::GetCurrentSample method</span></span>

> [!Note]  
> <span data-ttu-id="96135-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="96135-104">\[Deprecated.</span></span> <span data-ttu-id="96135-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="96135-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="96135-106">Il metodo `GetCurrentSample` non è implementato.</span><span class="sxs-lookup"><span data-stu-id="96135-106">The `GetCurrentSample` method is not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="96135-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96135-107">Syntax</span></span>


```C++
HRESULT GetCurrentSample(
   IMediaSample **ppSample
);
```



## <a name="parameters"></a><span data-ttu-id="96135-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="96135-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96135-109">*ppSample*</span><span class="sxs-lookup"><span data-stu-id="96135-109">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="96135-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="96135-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96135-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96135-111">Return value</span></span>

<span data-ttu-id="96135-112">Restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="96135-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="96135-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="96135-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="96135-114">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="96135-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="96135-115">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="96135-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="96135-116">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="96135-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96135-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96135-117">Requirements</span></span>



| <span data-ttu-id="96135-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="96135-118">Requirement</span></span> | <span data-ttu-id="96135-119">Valore</span><span class="sxs-lookup"><span data-stu-id="96135-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96135-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96135-120">Header</span></span><br/>  | <dl> <span data-ttu-id="96135-121"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="96135-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="96135-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="96135-122">Library</span></span><br/> | <dl> <span data-ttu-id="96135-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96135-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96135-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96135-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96135-125">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="96135-125">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="96135-126">**Interfaccia ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="96135-126">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




