---
description: Funzione proxy per il metodo CreateNewFrame.
ms.assetid: b23e8689-0fdc-49a7-a004-148b50420127
title: Funzione IWICBitmapEncoder_CreateNewFrame_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_CreateNewFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0ddf0141e5b13e370f199e3f211e74c3a0e6e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316817"
---
# <a name="iwicbitmapencoder_createnewframe_proxy-function"></a><span data-ttu-id="ace8f-103">IWICBitmapEncoder \_ CreateNewFrame- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="ace8f-103">IWICBitmapEncoder\_CreateNewFrame\_Proxy function</span></span>

<span data-ttu-id="ace8f-104">Funzione proxy per il metodo [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) .</span><span class="sxs-lookup"><span data-stu-id="ace8f-104">Proxy function for the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace8f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ace8f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_CreateNewFrame_Proxy(
  _In_    IWICBitmapEncoder     *THIS_PTR,
  _Out_   IWICBitmapFrameEncode **ppIFrameEncode,
  _Inout_ IPropertyBag2         **ppIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="ace8f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ace8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace8f-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace8f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace8f-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="ace8f-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="ace8f-109">Puntatore a questo oggetto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="ace8f-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="ace8f-110">*ppIFrameEncode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ace8f-110">*ppIFrameEncode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ace8f-111">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span><span class="sxs-lookup"><span data-stu-id="ace8f-111">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span></span>

<span data-ttu-id="ace8f-112">Puntatore che riceve un puntatore alla nuova istanza di un [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="ace8f-112">A pointer that receives a pointer to the new instance of an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span>

</dd> <dt>

<span data-ttu-id="ace8f-113">*ppIEncoderOptions* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ace8f-113">*ppIEncoderOptions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ace8f-114">Tipo: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span><span class="sxs-lookup"><span data-stu-id="ace8f-114">Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span></span>

<span data-ttu-id="ace8f-115">Proprietà denominate da usare per l'inizializzazione del frame.</span><span class="sxs-lookup"><span data-stu-id="ace8f-115">The named properties to use for frame initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace8f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ace8f-116">Return value</span></span>

<span data-ttu-id="ace8f-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ace8f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="ace8f-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ace8f-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ace8f-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ace8f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ace8f-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ace8f-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ace8f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ace8f-121">Requirements</span></span>



| <span data-ttu-id="ace8f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ace8f-122">Requirement</span></span> | <span data-ttu-id="ace8f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ace8f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace8f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ace8f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ace8f-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ace8f-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ace8f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ace8f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ace8f-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ace8f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ace8f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ace8f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace8f-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ace8f-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

