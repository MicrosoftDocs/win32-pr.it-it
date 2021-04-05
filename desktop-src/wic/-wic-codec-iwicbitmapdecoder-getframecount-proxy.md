---
description: Funzione proxy per il metodo GetFrameCount.
ms.assetid: 2103af73-60a2-4c1c-8db2-7dfd474440eb
title: Funzione IWICBitmapDecoder_GetFrameCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrameCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 784f362d711f22f5bfe1728f41309cdd7c22e788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751239"
---
# <a name="iwicbitmapdecoder_getframecount_proxy-function"></a><span data-ttu-id="93464-103">IWICBitmapDecoder \_ GetFrameCount- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="93464-103">IWICBitmapDecoder\_GetFrameCount\_Proxy function</span></span>

<span data-ttu-id="93464-104">Funzione proxy per il metodo [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .</span><span class="sxs-lookup"><span data-stu-id="93464-104">Proxy function for the [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="93464-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93464-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrameCount_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="93464-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93464-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93464-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93464-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93464-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="93464-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="93464-109">Puntatore a questo oggetto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="93464-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="93464-110">*pcount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="93464-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93464-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="93464-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="93464-112">Puntatore che riceve il numero totale di frame nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="93464-112">A pointer that receives the total number of frames in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93464-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93464-113">Return value</span></span>

<span data-ttu-id="93464-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="93464-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="93464-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="93464-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="93464-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93464-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="93464-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="93464-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="93464-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93464-118">Requirements</span></span>



| <span data-ttu-id="93464-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="93464-119">Requirement</span></span> | <span data-ttu-id="93464-120">Valore</span><span class="sxs-lookup"><span data-stu-id="93464-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93464-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93464-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93464-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93464-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="93464-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93464-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93464-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93464-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="93464-125">DLL</span><span class="sxs-lookup"><span data-stu-id="93464-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93464-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93464-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




