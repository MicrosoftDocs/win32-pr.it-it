---
description: IWICBitmapDecoder_CopyPalette_Proxy funzione proxy per il metodo CopyPalette.
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: IWICBitmapDecoder_CopyPalette_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56dbc523fe29ef9cc958b6ffbd80509284b78b88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086359"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="b65d9-103">Funzione proxy IWICBitmapDecoder \_ CopyPalette \_</span><span class="sxs-lookup"><span data-stu-id="b65d9-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="b65d9-104">Funzione proxy per il [**metodo CopyPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)</span><span class="sxs-lookup"><span data-stu-id="b65d9-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b65d9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b65d9-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="b65d9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b65d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b65d9-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b65d9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b65d9-108">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="b65d9-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="b65d9-109">Puntatore a [**questo oggetto IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="b65d9-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="b65d9-110">*pIPalette* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b65d9-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b65d9-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="b65d9-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="b65d9-112">Tavolozza delle immagini da copiare.</span><span class="sxs-lookup"><span data-stu-id="b65d9-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b65d9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b65d9-113">Return value</span></span>

<span data-ttu-id="b65d9-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b65d9-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b65d9-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b65d9-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b65d9-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="b65d9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b65d9-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b65d9-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b65d9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b65d9-118">Requirements</span></span>



| <span data-ttu-id="b65d9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b65d9-119">Requirement</span></span> | <span data-ttu-id="b65d9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b65d9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b65d9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b65d9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b65d9-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b65d9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b65d9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b65d9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b65d9-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b65d9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b65d9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b65d9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b65d9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b65d9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




