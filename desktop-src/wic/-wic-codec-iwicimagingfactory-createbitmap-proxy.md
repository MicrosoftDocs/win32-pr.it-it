---
description: Funzione proxy per il metodo CreateBitmap.
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: Funzione IWICImagingFactory_CreateBitmap_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56684de0280ae27bf2ec1e900bd718faec4733fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316810"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a><span data-ttu-id="e6881-103">IWICImagingFactory \_ CreateBitmap- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="e6881-103">IWICImagingFactory\_CreateBitmap\_Proxy function</span></span>

<span data-ttu-id="e6881-104">Funzione proxy per il metodo [**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) .</span><span class="sxs-lookup"><span data-stu-id="e6881-104">Proxy function for the [**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6881-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6881-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmap_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  UINT                       uiWidth,
  _In_  UINT                       uiHeight,
  _In_  REFWICPixelFormatGUID      pixelFormat,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="e6881-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6881-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6881-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6881-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6881-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="e6881-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="e6881-109">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6881-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6881-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e6881-110">Type: **UINT**</span></span>

<span data-ttu-id="e6881-111">Larghezza della nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="e6881-111">The width of the new bitmap .</span></span>

</dd> <dt>

<span data-ttu-id="e6881-112">*uiHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6881-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6881-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e6881-113">Type: **UINT**</span></span>

<span data-ttu-id="e6881-114">Altezza della nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="e6881-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="e6881-115">*PixelFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6881-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6881-116">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="e6881-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="e6881-117">Formato pixel della nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="e6881-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="e6881-118">*opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6881-118">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6881-119">Tipo: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="e6881-119">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="e6881-120">Opzioni di creazione della cache della nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="e6881-120">The cache creation options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="e6881-121">*ppIBitmap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e6881-121">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6881-122">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="e6881-122">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="e6881-123">Puntatore che riceve un puntatore alla nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="e6881-123">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6881-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6881-124">Return value</span></span>

<span data-ttu-id="e6881-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e6881-125">Type: **HRESULT**</span></span>

<span data-ttu-id="e6881-126">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e6881-126">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6881-127">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6881-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6881-128">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e6881-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e6881-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6881-129">Requirements</span></span>



| <span data-ttu-id="e6881-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6881-130">Requirement</span></span> | <span data-ttu-id="e6881-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e6881-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6881-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6881-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e6881-133">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6881-133">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e6881-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6881-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e6881-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6881-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e6881-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e6881-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6881-137"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6881-137"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




