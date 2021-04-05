---
description: Funzione proxy per il metodo Initialize.
ms.assetid: af9e204c-7072-47b8-84eb-47a754968d5b
title: Funzione IWICBitmapFrameEncode_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: da9192409636de96dbd9d35d9614df2c926c9032
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751218"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a><span data-ttu-id="7f529-103">IWICBitmapFrameEncode \_ Inizializza la \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="7f529-103">IWICBitmapFrameEncode\_Initialize\_Proxy function</span></span>

<span data-ttu-id="7f529-104">Funzione proxy per il metodo [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="7f529-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f529-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f529-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="7f529-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f529-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f529-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f529-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f529-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="7f529-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="7f529-109">Puntatore a questo oggetto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="7f529-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="7f529-110">*pIEncoderOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f529-110">*pIEncoderOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f529-111">Tipo: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="7f529-111">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="7f529-112">Set di proprietà da utilizzare per l'inizializzazione [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="7f529-112">The set of properties to use for [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f529-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f529-113">Return value</span></span>

<span data-ttu-id="7f529-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7f529-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7f529-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7f529-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f529-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f529-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f529-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7f529-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7f529-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f529-118">Requirements</span></span>



| <span data-ttu-id="7f529-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f529-119">Requirement</span></span> | <span data-ttu-id="7f529-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7f529-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f529-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f529-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7f529-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f529-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7f529-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f529-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7f529-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f529-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7f529-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7f529-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f529-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f529-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

