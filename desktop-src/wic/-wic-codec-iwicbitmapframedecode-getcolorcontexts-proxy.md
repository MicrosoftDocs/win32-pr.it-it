---
description: Funzione proxy per il metodo GetColorContexts.
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: Funzione IWICBitmapFrameDecode_GetColorContexts_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e22166e98e4ef276a6bf1d72dfc860cf8fb511e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226040"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a><span data-ttu-id="55b03-103">IWICBitmapFrameDecode \_ GetColorContexts- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="55b03-103">IWICBitmapFrameDecode\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="55b03-104">Funzione proxy per il metodo [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="55b03-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b03-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55b03-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="55b03-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="55b03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b03-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55b03-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b03-108">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="55b03-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="55b03-109">Puntatore a questo oggetto [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="55b03-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="55b03-110">*ccount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55b03-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b03-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="55b03-111">Type: **UINT**</span></span>

<span data-ttu-id="55b03-112">Il numero di contesti di colore da recuperare.</span><span class="sxs-lookup"><span data-stu-id="55b03-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="55b03-113">Questo valore deve essere di dimensioni maggiori o minori di, ovvero le dimensioni disponibili per *ppIColorContexts*.</span><span class="sxs-lookup"><span data-stu-id="55b03-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="55b03-114">*ppIColorContexts* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="55b03-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55b03-115">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="55b03-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="55b03-116">Puntatore che riceve un puntatore agli oggetti [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) .</span><span class="sxs-lookup"><span data-stu-id="55b03-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects.</span></span>

</dd> <dt>

<span data-ttu-id="55b03-117">*pcActualCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="55b03-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55b03-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="55b03-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="55b03-119">Puntatore che riceve il numero di contesti di colore contenuti nel frame dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="55b03-119">A pointer that receives the number of color contexts contained in the image frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b03-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55b03-120">Return value</span></span>

<span data-ttu-id="55b03-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="55b03-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="55b03-122">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="55b03-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="55b03-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="55b03-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="55b03-124">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="55b03-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="55b03-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55b03-125">Requirements</span></span>



| <span data-ttu-id="55b03-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="55b03-126">Requirement</span></span> | <span data-ttu-id="55b03-127">Valore</span><span class="sxs-lookup"><span data-stu-id="55b03-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55b03-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55b03-128">Minimum supported client</span></span><br/> | <span data-ttu-id="55b03-129">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55b03-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="55b03-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55b03-130">Minimum supported server</span></span><br/> | <span data-ttu-id="55b03-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55b03-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="55b03-132">DLL</span><span class="sxs-lookup"><span data-stu-id="55b03-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b03-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55b03-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




