---
description: Il metodo SetBufferSamples specifica se copiare i dati di esempio in un buffer mentre passa attraverso il filtro.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'Metodo ISampleGrabber:: SetBufferSamples (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330504"
---
# <a name="isamplegrabbersetbuffersamples-method"></a><span data-ttu-id="653e0-103">Metodo ISampleGrabber:: SetBufferSamples</span><span class="sxs-lookup"><span data-stu-id="653e0-103">ISampleGrabber::SetBufferSamples method</span></span>

> [!Note]  
> <span data-ttu-id="653e0-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="653e0-104">\[Deprecated.</span></span> <span data-ttu-id="653e0-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="653e0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="653e0-106">Il metodo **SetBufferSamples** specifica se copiare i dati di esempio in un buffer mentre passa attraverso il filtro.</span><span class="sxs-lookup"><span data-stu-id="653e0-106">The **SetBufferSamples** method specifies whether to copy sample data into a buffer as it goes through the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="653e0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="653e0-107">Syntax</span></span>


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a><span data-ttu-id="653e0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="653e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="653e0-109">*BufferThem*</span><span class="sxs-lookup"><span data-stu-id="653e0-109">*BufferThem*</span></span> 
</dt> <dd>

<span data-ttu-id="653e0-110">Valore booleano che specifica se memorizzare nel buffer i dati di esempio.</span><span class="sxs-lookup"><span data-stu-id="653e0-110">Boolean value specifying whether to buffer sample data.</span></span> <span data-ttu-id="653e0-111">Se **true**, il filtro copia i dati di esempio in un buffer interno.</span><span class="sxs-lookup"><span data-stu-id="653e0-111">If **TRUE**, the filter copies sample data into an internal buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="653e0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="653e0-112">Return value</span></span>

<span data-ttu-id="653e0-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="653e0-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="653e0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="653e0-114">Remarks</span></span>

<span data-ttu-id="653e0-115">Per ottenere il buffer copiato, chiamare [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="653e0-115">To get the copied buffer, call [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="653e0-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="653e0-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="653e0-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="653e0-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="653e0-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="653e0-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="653e0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="653e0-119">Requirements</span></span>



| <span data-ttu-id="653e0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="653e0-120">Requirement</span></span> | <span data-ttu-id="653e0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="653e0-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="653e0-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="653e0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="653e0-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="653e0-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="653e0-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="653e0-124">Library</span></span><br/> | <dl> <span data-ttu-id="653e0-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="653e0-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="653e0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="653e0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="653e0-127">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="653e0-127">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="653e0-128">**Interfaccia ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="653e0-128">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




