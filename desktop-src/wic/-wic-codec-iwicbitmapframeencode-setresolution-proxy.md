---
description: IWICBitmapFrameEncode_SetResolution_Proxy funzione proxy per il metodo SetResolution.
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: IWICBitmapFrameEncode_SetResolution_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 632d6e797d499c4c5468505a4cee49e088ab025a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116609"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="980e8-103">Funzione proxy IWICBitmapFrameEncode \_ SetResolution \_</span><span class="sxs-lookup"><span data-stu-id="980e8-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="980e8-104">Funzione proxy per il [**metodo SetResolution.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)</span><span class="sxs-lookup"><span data-stu-id="980e8-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="980e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="980e8-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="980e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="980e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="980e8-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="980e8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="980e8-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="980e8-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="980e8-109">Puntatore a [**questo oggetto IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="980e8-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="980e8-110">*dpiX* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="980e8-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="980e8-111">Tipo: **double**</span><span class="sxs-lookup"><span data-stu-id="980e8-111">Type: **double**</span></span>

<span data-ttu-id="980e8-112">Valore di risoluzione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="980e8-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="980e8-113">*dpiY* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="980e8-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="980e8-114">Tipo: **double**</span><span class="sxs-lookup"><span data-stu-id="980e8-114">Type: **double**</span></span>

<span data-ttu-id="980e8-115">Valore di risoluzione verticale.</span><span class="sxs-lookup"><span data-stu-id="980e8-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="980e8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="980e8-116">Return value</span></span>

<span data-ttu-id="980e8-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="980e8-117">Type: **HRESULT**</span></span>

<span data-ttu-id="980e8-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="980e8-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="980e8-119">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="980e8-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="980e8-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="980e8-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="980e8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="980e8-121">Requirements</span></span>



| <span data-ttu-id="980e8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="980e8-122">Requirement</span></span> | <span data-ttu-id="980e8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="980e8-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="980e8-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="980e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="980e8-125">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="980e8-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="980e8-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="980e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="980e8-127">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="980e8-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="980e8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="980e8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="980e8-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="980e8-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




