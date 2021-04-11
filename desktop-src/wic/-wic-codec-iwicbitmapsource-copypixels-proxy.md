---
description: Funzione proxy per il metodo CopyPixels.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: Funzione IWICBitmapSource_CopyPixels_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c759bd1731e2f3cbc4da9c40cb590e0f39686de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233171"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a><span data-ttu-id="f01e7-103">IWICBitmapSource \_ CopyPixels- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="f01e7-103">IWICBitmapSource\_CopyPixels\_Proxy function</span></span>

<span data-ttu-id="f01e7-104">Funzione proxy per il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) .</span><span class="sxs-lookup"><span data-stu-id="f01e7-104">Proxy function for the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f01e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f01e7-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="f01e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f01e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f01e7-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f01e7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01e7-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="f01e7-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="f01e7-109">Puntatore a questo oggetto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="f01e7-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="f01e7-110">*Repubblica popolare cinese* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f01e7-110">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01e7-111">Tipo: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="f01e7-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="f01e7-112">Rettangolo da copiare.</span><span class="sxs-lookup"><span data-stu-id="f01e7-112">The rectangle to copy.</span></span> <span data-ttu-id="f01e7-113">Un valore NULL specifica l'intera bitmap.</span><span class="sxs-lookup"><span data-stu-id="f01e7-113">A NULL value specifies the entire bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f01e7-114">_cbStride \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f01e7-114">_cbStride\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01e7-115">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f01e7-115">Type: **UINT**</span></span>

<span data-ttu-id="f01e7-116">Stride della bitmap</span><span class="sxs-lookup"><span data-stu-id="f01e7-116">The stride of the bitmap</span></span>

</dd> <dt>

<span data-ttu-id="f01e7-117">*cbBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f01e7-117">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01e7-118">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f01e7-118">Type: **UINT**</span></span>

<span data-ttu-id="f01e7-119">Dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="f01e7-119">The size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f01e7-120">*pbBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f01e7-120">*pbBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f01e7-121">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="f01e7-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="f01e7-122">Puntatore al buffer.</span><span class="sxs-lookup"><span data-stu-id="f01e7-122">A pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f01e7-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f01e7-123">Return value</span></span>

<span data-ttu-id="f01e7-124">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f01e7-124">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f01e7-125">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f01e7-125">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f01e7-126">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f01e7-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f01e7-127">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f01e7-127">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f01e7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f01e7-128">Requirements</span></span>



| <span data-ttu-id="f01e7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f01e7-129">Requirement</span></span> | <span data-ttu-id="f01e7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f01e7-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f01e7-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f01e7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f01e7-132">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f01e7-132">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f01e7-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f01e7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f01e7-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f01e7-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f01e7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f01e7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f01e7-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f01e7-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




