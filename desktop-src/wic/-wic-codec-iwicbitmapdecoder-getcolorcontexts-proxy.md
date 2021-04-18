---
description: Funzione proxy per il metodo GetColorContexts.
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: Funzione IWICBitmapDecoder_GetColorContexts_Proxy
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
ms.openlocfilehash: 737ad4b8bbb0014a04129d3a264cecaed4b5fe8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313433"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="b88f1-103">IWICBitmapDecoder \_ GetColorContexts- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="b88f1-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="b88f1-104">Funzione proxy per il metodo [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="b88f1-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b88f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b88f1-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="b88f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b88f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b88f1-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b88f1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b88f1-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="b88f1-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="b88f1-109">Puntatore a questo oggetto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="b88f1-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="b88f1-110">*ccount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b88f1-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b88f1-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b88f1-111">Type: **UINT**</span></span>

<span data-ttu-id="b88f1-112">Il numero di contesti di colore da recuperare.</span><span class="sxs-lookup"><span data-stu-id="b88f1-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="b88f1-113">Questo valore deve essere di dimensioni maggiori o minori di, ovvero le dimensioni disponibili per *ppIColorContexts*.</span><span class="sxs-lookup"><span data-stu-id="b88f1-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="b88f1-114">*ppIColorContexts* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b88f1-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b88f1-115">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="b88f1-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="b88f1-116">Puntatore che riceve un puntatore a [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="b88f1-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="b88f1-117">*pcActualCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b88f1-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b88f1-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="b88f1-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="b88f1-119">Puntatore che riceve il numero di contesti di colore contenuti nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b88f1-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b88f1-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b88f1-120">Return value</span></span>

<span data-ttu-id="b88f1-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b88f1-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b88f1-122">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b88f1-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b88f1-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b88f1-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b88f1-124">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b88f1-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b88f1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b88f1-125">Requirements</span></span>



| <span data-ttu-id="b88f1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b88f1-126">Requirement</span></span> | <span data-ttu-id="b88f1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b88f1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b88f1-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b88f1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b88f1-129">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b88f1-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b88f1-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b88f1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b88f1-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b88f1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b88f1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b88f1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b88f1-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b88f1-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




