---
description: Funzione proxy per il metodo WriteSource.
ms.assetid: d95ad80f-7a26-45a7-8103-2673989143b7
title: Funzione IWICBitmapFrameEncode_WriteSource_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_WriteSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9eb5ab9db9341d138c72d350304407966a6293d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234207"
---
# <a name="iwicbitmapframeencode_writesource_proxy-function"></a><span data-ttu-id="45587-103">IWICBitmapFrameEncode \_ WriteSource- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="45587-103">IWICBitmapFrameEncode\_WriteSource\_Proxy function</span></span>

<span data-ttu-id="45587-104">Funzione proxy per il metodo [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .</span><span class="sxs-lookup"><span data-stu-id="45587-104">Proxy function for the [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="45587-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45587-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_WriteSource_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ WICRect               *prc
);
```



## <a name="parameters"></a><span data-ttu-id="45587-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="45587-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45587-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45587-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45587-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="45587-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="45587-109">Puntatore a questo oggetto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="45587-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="45587-110">*pIBitmapSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45587-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45587-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="45587-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="45587-112">Origine della bitmap da codificare.</span><span class="sxs-lookup"><span data-stu-id="45587-112">The bitmap source to encode.</span></span>

</dd> <dt>

<span data-ttu-id="45587-113">_prc \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45587-113">_prc\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45587-114">Tipo: \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="45587-114">Type: \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="45587-115">Rettangolo delle dimensioni dell'origine della bitmap.</span><span class="sxs-lookup"><span data-stu-id="45587-115">The size rectangle of the bitmap source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45587-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45587-116">Return value</span></span>

<span data-ttu-id="45587-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="45587-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="45587-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="45587-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="45587-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="45587-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="45587-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="45587-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="45587-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45587-121">Requirements</span></span>



| <span data-ttu-id="45587-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="45587-122">Requirement</span></span> | <span data-ttu-id="45587-123">Valore</span><span class="sxs-lookup"><span data-stu-id="45587-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45587-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45587-124">Minimum supported client</span></span><br/> | <span data-ttu-id="45587-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45587-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="45587-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45587-126">Minimum supported server</span></span><br/> | <span data-ttu-id="45587-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45587-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="45587-128">DLL</span><span class="sxs-lookup"><span data-stu-id="45587-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45587-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45587-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




