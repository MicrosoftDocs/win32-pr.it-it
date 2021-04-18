---
description: Funzione proxy per la negoziazione del formato pixel e della tavolozza per il codificatore.
ms.assetid: 01179598-ba40-4aed-a7c4-888cb4e851f4
title: Funzione WICSetEncoderFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICSetEncoderFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7ea0988d29d1d9ed04668dfbe8ce86b97af6534a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313420"
---
# <a name="wicsetencoderformat_proxy-function"></a><span data-ttu-id="c33d6-103">\_Funzione proxy WICSetEncoderFormat</span><span class="sxs-lookup"><span data-stu-id="c33d6-103">WICSetEncoderFormat\_Proxy function</span></span>

<span data-ttu-id="c33d6-104">Funzione proxy per la negoziazione del formato pixel e della tavolozza per il codificatore.</span><span class="sxs-lookup"><span data-stu-id="c33d6-104">Proxy function for negotiating the pixel format and the palette for the encoder.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c33d6-105">Syntax</span></span>


```C++
HRESULT WICSetEncoderFormat_Proxy(
  _In_  IWICBitmapSource      *pSourceIn,
  _In_  IWICPalette           *pIPalette,
  _In_  IWICBitmapFrameEncode *pIFrameEncode,
  _Out_ IWICBitmapSource      **ppSourceOut
);
```



## <a name="parameters"></a><span data-ttu-id="c33d6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c33d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c33d6-107">*pSourceIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c33d6-107">*pSourceIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33d6-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="c33d6-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="c33d6-109">Puntatore alla bitmap di origine.</span><span class="sxs-lookup"><span data-stu-id="c33d6-109">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="c33d6-110">_pIPalette \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c33d6-110">_pIPalette\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33d6-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="c33d6-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="c33d6-112">Puntatore alla tavolozza da utilizzare per la codifica.</span><span class="sxs-lookup"><span data-stu-id="c33d6-112">Pointer to the palette to use for encoding.</span></span>

</dd> <dt>

<span data-ttu-id="c33d6-113">_pIFrameEncode \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c33d6-113">_pIFrameEncode\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33d6-114">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="c33d6-114">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="c33d6-115">Puntatore all'oggetto di codifica del frame.</span><span class="sxs-lookup"><span data-stu-id="c33d6-115">Pointer to the frame encode object.</span></span>

</dd> <dt>

<span data-ttu-id="c33d6-116">_ppSourceOut \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c33d6-116">_ppSourceOut\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c33d6-117">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="c33d6-117">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="c33d6-118">Puntatore che riceve un puntatore all'origine di output.</span><span class="sxs-lookup"><span data-stu-id="c33d6-118">Pointer that receives a pointer to the output source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c33d6-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c33d6-119">Return value</span></span>

<span data-ttu-id="c33d6-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c33d6-120">Type: **HRESULT**</span></span>

<span data-ttu-id="c33d6-121">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c33d6-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c33d6-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c33d6-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c33d6-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c33d6-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c33d6-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c33d6-124">Requirements</span></span>



| <span data-ttu-id="c33d6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c33d6-125">Requirement</span></span> | <span data-ttu-id="c33d6-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c33d6-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c33d6-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c33d6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c33d6-128">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c33d6-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c33d6-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c33d6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c33d6-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c33d6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c33d6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c33d6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c33d6-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c33d6-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




