---
description: IWICBitmapFrameEncode_SetThumbnail_Proxy funzione proxy per il metodo SetThumbnail.
ms.assetid: 3ad473ec-9218-4ed1-961d-a2aa0d542119
title: IWICBitmapFrameEncode_SetThumbnail_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9af9dd2d4f8fe71a6dc94420db17383a5da6da28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116599"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="f63fc-103">Funzione proxy IWICBitmapFrameEncode \_ SetThumbnail \_</span><span class="sxs-lookup"><span data-stu-id="f63fc-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="f63fc-104">Funzione proxy per il [**metodo SetThumbnail.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)</span><span class="sxs-lookup"><span data-stu-id="f63fc-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f63fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f63fc-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="f63fc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f63fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f63fc-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f63fc-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f63fc-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="f63fc-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="f63fc-109">Puntatore a [**questo oggetto IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="f63fc-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="f63fc-110">*pIThumbnail* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f63fc-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f63fc-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="f63fc-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="f63fc-112">Origine bitmap da usare come anteprima.</span><span class="sxs-lookup"><span data-stu-id="f63fc-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f63fc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f63fc-113">Return value</span></span>

<span data-ttu-id="f63fc-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f63fc-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f63fc-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f63fc-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f63fc-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="f63fc-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f63fc-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f63fc-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f63fc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f63fc-118">Requirements</span></span>



| <span data-ttu-id="f63fc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f63fc-119">Requirement</span></span> | <span data-ttu-id="f63fc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f63fc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f63fc-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f63fc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f63fc-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f63fc-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f63fc-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f63fc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f63fc-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f63fc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f63fc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f63fc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f63fc-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f63fc-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




