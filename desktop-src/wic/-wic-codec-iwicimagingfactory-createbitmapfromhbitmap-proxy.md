---
description: Funzione proxy per il metodo CreateBitmapFromHBITMAP.
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: Funzione IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316808"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a><span data-ttu-id="a8d97-103">IWICImagingFactory \_ CreateBitmapFromHBITMAP- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="a8d97-103">IWICImagingFactory\_CreateBitmapFromHBITMAP\_Proxy function</span></span>

<span data-ttu-id="a8d97-104">Funzione proxy per il metodo [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) .</span><span class="sxs-lookup"><span data-stu-id="a8d97-104">Proxy function for the [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d97-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8d97-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="a8d97-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8d97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8d97-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8d97-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d97-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="a8d97-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="a8d97-109">_hBitmap \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8d97-109">_hBitmap\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d97-110">Tipo: **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="a8d97-110">Type: **HBITMAP**</span></span>

<span data-ttu-id="a8d97-111">Handle bitmap da cui creare la bitmap.</span><span class="sxs-lookup"><span data-stu-id="a8d97-111">A bitmap handle to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="a8d97-112">*hPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8d97-112">*hPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d97-113">Tipo: **HPALETTE**</span><span class="sxs-lookup"><span data-stu-id="a8d97-113">Type: **HPALETTE**</span></span>

<span data-ttu-id="a8d97-114">Handle della tavolozza utilizzato per creare la bitmap.</span><span class="sxs-lookup"><span data-stu-id="a8d97-114">A palette handle used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="a8d97-115">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a8d97-115">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d97-116">Tipo: **[ **WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span><span class="sxs-lookup"><span data-stu-id="a8d97-116">Type: **[**WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span></span>

<span data-ttu-id="a8d97-117">Opzioni del canale alfa per creare la bitmap.</span><span class="sxs-lookup"><span data-stu-id="a8d97-117">The alpha channel options to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="a8d97-118">*ppIBitmap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a8d97-118">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d97-119">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="a8d97-119">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="a8d97-120">Puntatore che riceve un puntatore alla nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="a8d97-120">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8d97-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8d97-121">Return value</span></span>

<span data-ttu-id="a8d97-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a8d97-122">Type: **HRESULT**</span></span>

<span data-ttu-id="a8d97-123">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a8d97-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a8d97-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8d97-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8d97-125">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a8d97-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a8d97-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8d97-126">Requirements</span></span>



| <span data-ttu-id="a8d97-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8d97-127">Requirement</span></span> | <span data-ttu-id="a8d97-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a8d97-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d97-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8d97-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d97-130">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8d97-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a8d97-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8d97-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d97-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8d97-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a8d97-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a8d97-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8d97-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8d97-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




