---
description: Funzione proxy per il metodo CreateBitmapFromMemory.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: Funzione IWICImagingFactory_CreateBitmapFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316806"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a><span data-ttu-id="ea25a-103">IWICImagingFactory \_ CreateBitmapFromMemory- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="ea25a-103">IWICImagingFactory\_CreateBitmapFromMemory\_Proxy function</span></span>

<span data-ttu-id="ea25a-104">Funzione proxy per il metodo [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) .</span><span class="sxs-lookup"><span data-stu-id="ea25a-104">Proxy function for the [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea25a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea25a-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="ea25a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea25a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea25a-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea25a-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea25a-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="ea25a-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="ea25a-109">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea25a-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea25a-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ea25a-110">Type: **UINT**</span></span>

<span data-ttu-id="ea25a-111">Larghezza della nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="ea25a-111">The width of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ea25a-112">*uiHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea25a-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea25a-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ea25a-113">Type: **UINT**</span></span>

<span data-ttu-id="ea25a-114">Altezza della nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="ea25a-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ea25a-115">*PixelFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea25a-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea25a-116">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="ea25a-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="ea25a-117">Formato pixel della nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="ea25a-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ea25a-118">*cbStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea25a-118">*cbStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea25a-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ea25a-119">Type: **UINT**</span></span>

<span data-ttu-id="ea25a-120">[*Stride*](/windows) dei dati pixel specificati.</span><span class="sxs-lookup"><span data-stu-id="ea25a-120">The [*stride*](/windows) of the given pixel data.</span></span>

</dd> <dt>

<span data-ttu-id="ea25a-121">*cbBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea25a-121">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea25a-122">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ea25a-122">Type: **UINT**</span></span>

<span data-ttu-id="ea25a-123">Dimensioni di *pbBuffer*.</span><span class="sxs-lookup"><span data-stu-id="ea25a-123">The size of *pbBuffer*.</span></span>

</dd> <dt>

<span data-ttu-id="ea25a-124">*pbBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea25a-124">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea25a-125">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="ea25a-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="ea25a-126">Buffer utilizzato per creare la bitmap.</span><span class="sxs-lookup"><span data-stu-id="ea25a-126">The buffer used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ea25a-127">_ppIBitmap \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ea25a-127">_ppIBitmap\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea25a-128">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="ea25a-128">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="ea25a-129">Puntatore che riceve un puntatore alla nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="ea25a-129">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea25a-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea25a-130">Return value</span></span>

<span data-ttu-id="ea25a-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ea25a-131">Type: **HRESULT**</span></span>

<span data-ttu-id="ea25a-132">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ea25a-132">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ea25a-133">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ea25a-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea25a-134">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ea25a-134">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ea25a-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea25a-135">Requirements</span></span>



| <span data-ttu-id="ea25a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea25a-136">Requirement</span></span> | <span data-ttu-id="ea25a-137">Valore</span><span class="sxs-lookup"><span data-stu-id="ea25a-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea25a-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea25a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ea25a-139">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea25a-139">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ea25a-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea25a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ea25a-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea25a-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ea25a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ea25a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea25a-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea25a-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

