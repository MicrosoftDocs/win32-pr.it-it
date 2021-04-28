---
description: IWICBitmapDecoder_GetThumbnail_Proxy funzione proxy per il metodo GetThumbnail.
ms.assetid: 37a6ba78-0d1b-47f6-9b12-8ad123c8ee86
title: IWICBitmapDecoder_GetThumbnail_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3fb4d6ae050772bb6392e1d94c88ef5bfc23d2ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100609"
---
# <a name="iwicbitmapdecoder_getthumbnail_proxy-function"></a><span data-ttu-id="c5af8-103">Funzione IWICBitmapDecoder \_ GetThumbnail \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="c5af8-103">IWICBitmapDecoder\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="c5af8-104">Funzione proxy per [**il metodo GetThumbnail.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)</span><span class="sxs-lookup"><span data-stu-id="c5af8-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5af8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5af8-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetThumbnail_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="c5af8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5af8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5af8-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5af8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5af8-108">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="c5af8-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="c5af8-109">Puntatore a [**questo oggetto IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="c5af8-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="c5af8-110">*ppIThumbnail* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="c5af8-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5af8-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="c5af8-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="c5af8-112">Puntatore che riceve un puntatore [**all'oggetto IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) dell'anteprima.</span><span class="sxs-lookup"><span data-stu-id="c5af8-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5af8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5af8-113">Return value</span></span>

<span data-ttu-id="c5af8-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c5af8-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c5af8-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c5af8-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5af8-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c5af8-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5af8-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c5af8-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c5af8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5af8-118">Requirements</span></span>



| <span data-ttu-id="c5af8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5af8-119">Requirement</span></span> | <span data-ttu-id="c5af8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c5af8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5af8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5af8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c5af8-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c5af8-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c5af8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5af8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c5af8-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5af8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c5af8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c5af8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5af8-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5af8-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




