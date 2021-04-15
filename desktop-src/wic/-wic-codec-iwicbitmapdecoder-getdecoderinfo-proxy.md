---
description: Funzione proxy per il metodo GetDecoderInfo.
ms.assetid: 4117492e-d652-4c72-9979-cc4e554a6fd8
title: Funzione IWICBitmapDecoder_GetDecoderInfo_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetDecoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ca3e234bc6bbff8899b88c89169a59d9838350b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484772"
---
# <a name="iwicbitmapdecoder_getdecoderinfo_proxy-function"></a><span data-ttu-id="8fccb-103">IWICBitmapDecoder \_ GetDecoderInfo- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="8fccb-103">IWICBitmapDecoder\_GetDecoderInfo\_Proxy function</span></span>

<span data-ttu-id="8fccb-104">Funzione proxy per il metodo [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="8fccb-104">Proxy function for the [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fccb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fccb-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetDecoderInfo_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _Out_ IWICBitmapDecoderInfo **ppIDecoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8fccb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fccb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fccb-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fccb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fccb-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="8fccb-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="8fccb-109">Puntatore a questo oggetto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="8fccb-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="8fccb-110">*ppIDecoderInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8fccb-110">*ppIDecoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fccb-111">Tipo: **[ **IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="8fccb-111">Type: **[**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span></span>

<span data-ttu-id="8fccb-112">Puntatore che riceve un puntatore a un [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span><span class="sxs-lookup"><span data-stu-id="8fccb-112">A pointer that receives a pointer to an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fccb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fccb-113">Return value</span></span>

<span data-ttu-id="8fccb-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8fccb-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8fccb-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8fccb-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8fccb-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8fccb-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fccb-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8fccb-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8fccb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fccb-118">Requirements</span></span>



| <span data-ttu-id="8fccb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fccb-119">Requirement</span></span> | <span data-ttu-id="8fccb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8fccb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fccb-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fccb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8fccb-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8fccb-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8fccb-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fccb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8fccb-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8fccb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8fccb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8fccb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fccb-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fccb-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




