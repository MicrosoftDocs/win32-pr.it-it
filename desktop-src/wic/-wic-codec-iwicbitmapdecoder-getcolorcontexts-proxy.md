---
description: IWICBitmapDecoder_GetColorContexts_Proxy funzione proxy per il metodo GetColorContexts.
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: IWICBitmapDecoder_GetColorContexts_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e550ca4ebd863e58a4bd285c48a2a01aad059b03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086259"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="477f7-103">Funzione proxy IWICBitmapDecoder \_ GetColorContexts \_</span><span class="sxs-lookup"><span data-stu-id="477f7-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="477f7-104">Funzione proxy per il [**metodo GetColorContexts.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)</span><span class="sxs-lookup"><span data-stu-id="477f7-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="477f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="477f7-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="477f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="477f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="477f7-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="477f7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="477f7-108">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="477f7-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="477f7-109">Puntatore a [**questo oggetto IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="477f7-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="477f7-110">*cCount* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="477f7-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="477f7-111">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="477f7-111">Type: **UINT**</span></span>

<span data-ttu-id="477f7-112">Numero di contesti di colore da recuperare.</span><span class="sxs-lookup"><span data-stu-id="477f7-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="477f7-113">Questo valore deve essere la dimensione di , o minore di, la dimensione disponibile per *ppIColorContexts*.</span><span class="sxs-lookup"><span data-stu-id="477f7-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="477f7-114">*ppIColorContexts* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="477f7-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="477f7-115">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="477f7-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="477f7-116">Puntatore che riceve un puntatore a [**IWICColorContext.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)</span><span class="sxs-lookup"><span data-stu-id="477f7-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="477f7-117">*pcActualCount* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="477f7-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="477f7-118">Tipo: **UINT \***</span><span class="sxs-lookup"><span data-stu-id="477f7-118">Type: **UINT\***</span></span>

<span data-ttu-id="477f7-119">Puntatore che riceve il numero di contesti di colore contenuti nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="477f7-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="477f7-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="477f7-120">Return value</span></span>

<span data-ttu-id="477f7-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="477f7-121">Type: **HRESULT**</span></span>

<span data-ttu-id="477f7-122">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="477f7-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="477f7-123">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="477f7-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="477f7-124">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="477f7-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="477f7-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="477f7-125">Requirements</span></span>



| <span data-ttu-id="477f7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="477f7-126">Requirement</span></span> | <span data-ttu-id="477f7-127">Valore</span><span class="sxs-lookup"><span data-stu-id="477f7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="477f7-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="477f7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="477f7-129">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="477f7-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="477f7-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="477f7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="477f7-131">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="477f7-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="477f7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="477f7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="477f7-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="477f7-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




