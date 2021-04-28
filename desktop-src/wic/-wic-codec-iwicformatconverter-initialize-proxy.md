---
description: IWICFormatConverter_Initialize_Proxy funzione proxy per il metodo Initialize.
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: IWICFormatConverter_Initialize_Proxy funzione
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
ms.openlocfilehash: d70d852adc8f810438ce46dc30345e68fa27e0fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097159"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="9a27c-103">Funzione IWICFormatConverter \_ Initialize \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="9a27c-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="9a27c-104">Funzione proxy per il [**metodo Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize)</span><span class="sxs-lookup"><span data-stu-id="9a27c-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a27c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a27c-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="9a27c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a27c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a27c-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a27c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a27c-108">Tipo: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***</span><span class="sxs-lookup"><span data-stu-id="9a27c-108">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***</span></span>

<span data-ttu-id="9a27c-109">Puntatore a questo [**oggetto IWICFormatConverter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)</span><span class="sxs-lookup"><span data-stu-id="9a27c-109">Pointer to this [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="9a27c-110">*pISource* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9a27c-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a27c-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="9a27c-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="9a27c-112">Bitmap di input da convertire</span><span class="sxs-lookup"><span data-stu-id="9a27c-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="9a27c-113">*dstFormat* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9a27c-113">*dstFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a27c-114">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="9a27c-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="9a27c-115">GUID del formato pixel di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9a27c-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="9a27c-116">*dithering* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9a27c-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a27c-117">Tipo: **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="9a27c-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="9a27c-118">[**WICBitmapDitherType usato**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) per la conversione.</span><span class="sxs-lookup"><span data-stu-id="9a27c-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="9a27c-119">*pIPalette* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9a27c-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a27c-120">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="9a27c-120">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="9a27c-121">Riquadro da utilizzare per la conversione.</span><span class="sxs-lookup"><span data-stu-id="9a27c-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="9a27c-122">*alphaThresholdPercent* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9a27c-122">*alphaThresholdPercent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a27c-123">Tipo: **double**</span><span class="sxs-lookup"><span data-stu-id="9a27c-123">Type: **double**</span></span>

<span data-ttu-id="9a27c-124">Soglia alfa da usare per la conversione.</span><span class="sxs-lookup"><span data-stu-id="9a27c-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="9a27c-125">*paletteTranslate* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9a27c-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a27c-126">Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="9a27c-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="9a27c-127">Tipo di conversione della tavolozza da utilizzare per la conversione.</span><span class="sxs-lookup"><span data-stu-id="9a27c-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a27c-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a27c-128">Return value</span></span>

<span data-ttu-id="9a27c-129">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9a27c-129">Type: **HRESULT**</span></span>

<span data-ttu-id="9a27c-130">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9a27c-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a27c-131">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9a27c-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a27c-132">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="9a27c-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9a27c-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a27c-133">Requirements</span></span>



| <span data-ttu-id="9a27c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a27c-134">Requirement</span></span> | <span data-ttu-id="9a27c-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9a27c-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a27c-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a27c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9a27c-137">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9a27c-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9a27c-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a27c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9a27c-139">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a27c-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9a27c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9a27c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a27c-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a27c-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




