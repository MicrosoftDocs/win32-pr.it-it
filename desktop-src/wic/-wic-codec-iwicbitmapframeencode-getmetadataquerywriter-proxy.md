---
description: Funzione proxy per il metodo GetMetadataQueryWriter.
ms.assetid: b2c61dee-b72b-408c-8cb9-de2587587f1f
title: Funzione IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b6668ffc4261310bfa76424afcae92e14c4ed921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751223"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="6234c-103">IWICBitmapFrameEncode \_ GetMetadataQueryWriter- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="6234c-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="6234c-104">Funzione proxy per il metodo [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="6234c-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6234c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6234c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="6234c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6234c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6234c-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6234c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6234c-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="6234c-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="6234c-109">Puntatore a questo oggetto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="6234c-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="6234c-110">*ppIMetadataQueryWriter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6234c-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6234c-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="6234c-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="6234c-112">Puntatore che riceve un writer di query dei metadati per il frame.</span><span class="sxs-lookup"><span data-stu-id="6234c-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6234c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6234c-113">Return value</span></span>

<span data-ttu-id="6234c-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6234c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6234c-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6234c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6234c-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6234c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6234c-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="6234c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6234c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6234c-118">Requirements</span></span>



| <span data-ttu-id="6234c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6234c-119">Requirement</span></span> | <span data-ttu-id="6234c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6234c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6234c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6234c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6234c-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6234c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6234c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6234c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6234c-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6234c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6234c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6234c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6234c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6234c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




