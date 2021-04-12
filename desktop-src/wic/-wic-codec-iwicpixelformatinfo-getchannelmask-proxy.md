---
description: Funzione proxy per il metodo GetChannelMask.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: Funzione IWICPixelFormatInfo_GetChannelMask_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233543"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a><span data-ttu-id="26b26-103">IWICPixelFormatInfo \_ GetChannelMask- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="26b26-103">IWICPixelFormatInfo\_GetChannelMask\_Proxy function</span></span>

<span data-ttu-id="26b26-104">Funzione proxy per il metodo [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) .</span><span class="sxs-lookup"><span data-stu-id="26b26-104">Proxy function for the [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b26-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26b26-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a><span data-ttu-id="26b26-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26b26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26b26-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26b26-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b26-108">Tipo: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="26b26-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="26b26-109">Puntatore a questo oggetto [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="26b26-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="26b26-110">*uiChannelIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26b26-110">*uiChannelIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b26-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="26b26-111">Type: **UINT**</span></span>

<span data-ttu-id="26b26-112">Indice della maschera di canale da recuperare.</span><span class="sxs-lookup"><span data-stu-id="26b26-112">The index to the channel mask to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="26b26-113">*cbMaskBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26b26-113">*cbMaskBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b26-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="26b26-114">Type: **UINT**</span></span>

<span data-ttu-id="26b26-115">Dimensioni del buffer *pbMaskBuffer* .</span><span class="sxs-lookup"><span data-stu-id="26b26-115">The size of the *pbMaskBuffer* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="26b26-116">*pbMaskBuffer* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="26b26-116">*pbMaskBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="26b26-117">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="26b26-117">Type: \**BYTE\** _</span></span>

<span data-ttu-id="26b26-118">Puntatore al buffer della maschera.</span><span class="sxs-lookup"><span data-stu-id="26b26-118">Pointer to the mask buffer.</span></span>

</dd> <dt>

<span data-ttu-id="26b26-119">_pcbActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="26b26-119">_pcbActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26b26-120">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="26b26-120">Type: \**UINT\** _</span></span>

<span data-ttu-id="26b26-121">Dimensioni effettive del buffer necessarie per ottenere la maschera di canale.</span><span class="sxs-lookup"><span data-stu-id="26b26-121">The actual buffer size needed to obtain the channel mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26b26-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26b26-122">Return value</span></span>

<span data-ttu-id="26b26-123">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="26b26-123">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="26b26-124">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="26b26-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26b26-125">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26b26-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="26b26-126">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="26b26-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="26b26-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26b26-127">Requirements</span></span>



| <span data-ttu-id="26b26-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b26-128">Requirement</span></span> | <span data-ttu-id="26b26-129">Valore</span><span class="sxs-lookup"><span data-stu-id="26b26-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26b26-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26b26-130">Minimum supported client</span></span><br/> | <span data-ttu-id="26b26-131">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26b26-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="26b26-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26b26-132">Minimum supported server</span></span><br/> | <span data-ttu-id="26b26-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26b26-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="26b26-134">DLL</span><span class="sxs-lookup"><span data-stu-id="26b26-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26b26-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26b26-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




