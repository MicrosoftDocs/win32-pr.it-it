---
description: Funzione proxy per il metodo GetBitsPerPixel.
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: Funzione IWICPixelFormatInfo_GetBitsPerPixel_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f8d3469ca7c1eacf1f6755cbf5b6243527639d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316802"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a><span data-ttu-id="20216-103">IWICPixelFormatInfo \_ GetBitsPerPixel- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="20216-103">IWICPixelFormatInfo\_GetBitsPerPixel\_Proxy function</span></span>

<span data-ttu-id="20216-104">Funzione proxy per il metodo [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) .</span><span class="sxs-lookup"><span data-stu-id="20216-104">Proxy function for the [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20216-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20216-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a><span data-ttu-id="20216-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20216-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20216-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20216-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20216-108">Tipo: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="20216-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="20216-109">Puntatore a questo oggetto [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="20216-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="20216-110">*puiBitsPerPixel* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="20216-110">*puiBitsPerPixel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20216-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="20216-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="20216-112">Puntatore che riceve il BPP del formato pixel.</span><span class="sxs-lookup"><span data-stu-id="20216-112">Pointer that receives the BPP of the pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20216-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20216-113">Return value</span></span>

<span data-ttu-id="20216-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="20216-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="20216-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="20216-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="20216-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="20216-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="20216-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="20216-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="20216-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20216-118">Requirements</span></span>



| <span data-ttu-id="20216-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="20216-119">Requirement</span></span> | <span data-ttu-id="20216-120">Valore</span><span class="sxs-lookup"><span data-stu-id="20216-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20216-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20216-121">Minimum supported client</span></span><br/> | <span data-ttu-id="20216-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20216-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="20216-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20216-123">Minimum supported server</span></span><br/> | <span data-ttu-id="20216-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20216-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="20216-125">DLL</span><span class="sxs-lookup"><span data-stu-id="20216-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20216-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20216-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




