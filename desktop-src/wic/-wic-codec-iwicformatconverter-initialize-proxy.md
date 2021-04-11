---
description: Funzione proxy per il metodo Initialize.
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: Funzione IWICFormatConverter_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6450c1a508507db73e44ef8b88b4f94970ac6004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233170"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="ea29f-103">IWICFormatConverter \_ Inizializza la \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="ea29f-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="ea29f-104">Funzione proxy per il metodo [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="ea29f-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea29f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea29f-105">Syntax</span></span>


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a><span data-ttu-id="ea29f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea29f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea29f-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea29f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea29f-108">Tipo: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) \** _</span><span class="sxs-lookup"><span data-stu-id="ea29f-108">Type: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\** _</span></span>

<span data-ttu-id="ea29f-109">Puntatore a questo oggetto [_ *IWICFormatConverter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="ea29f-109">Pointer to this [_ *IWICFormatConverter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="ea29f-110">*pISource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea29f-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea29f-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="ea29f-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="ea29f-112">Bitmap di input da convertire</span><span class="sxs-lookup"><span data-stu-id="ea29f-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="ea29f-113">_dstFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea29f-113">_dstFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea29f-114">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="ea29f-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="ea29f-115">GUID del formato pixel di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ea29f-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="ea29f-116">*dithering* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea29f-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea29f-117">Tipo: **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="ea29f-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="ea29f-118">[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) utilizzato per la conversione.</span><span class="sxs-lookup"><span data-stu-id="ea29f-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="ea29f-119">*pIPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea29f-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea29f-120">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="ea29f-120">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="ea29f-121">Tavolozza da utilizzare per la conversione.</span><span class="sxs-lookup"><span data-stu-id="ea29f-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="ea29f-122">_alphaThresholdPercent \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea29f-122">_alphaThresholdPercent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea29f-123">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="ea29f-123">Type: **double**</span></span>

<span data-ttu-id="ea29f-124">Soglia alfa da utilizzare per la conversione.</span><span class="sxs-lookup"><span data-stu-id="ea29f-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="ea29f-125">*paletteTranslate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea29f-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea29f-126">Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="ea29f-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="ea29f-127">Tipo di conversione della tavolozza da utilizzare per la conversione.</span><span class="sxs-lookup"><span data-stu-id="ea29f-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea29f-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea29f-128">Return value</span></span>

<span data-ttu-id="ea29f-129">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ea29f-129">Type: **HRESULT**</span></span>

<span data-ttu-id="ea29f-130">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ea29f-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ea29f-131">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ea29f-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea29f-132">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ea29f-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ea29f-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea29f-133">Requirements</span></span>



| <span data-ttu-id="ea29f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea29f-134">Requirement</span></span> | <span data-ttu-id="ea29f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ea29f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea29f-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea29f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ea29f-137">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea29f-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ea29f-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea29f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ea29f-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea29f-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ea29f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ea29f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea29f-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea29f-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




