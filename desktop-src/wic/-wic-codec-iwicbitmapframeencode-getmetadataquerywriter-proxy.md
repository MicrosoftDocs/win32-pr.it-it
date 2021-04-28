---
description: IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy funzione proxy per il metodo GetMetadataQueryWriter.
ms.assetid: b2c61dee-b72b-408c-8cb9-de2587587f1f
title: IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy funzione
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
ms.openlocfilehash: 89eb7342277d335c78ee2bc6807f2fc4d170bb9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113609"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="abf09-103">Funzione proxy IWICBitmapFrameEncode \_ GetMetadataQueryWriter \_</span><span class="sxs-lookup"><span data-stu-id="abf09-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="abf09-104">Funzione proxy per il [**metodo GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="abf09-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf09-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abf09-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="abf09-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="abf09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abf09-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abf09-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abf09-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="abf09-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="abf09-109">Puntatore a [**questo oggetto IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="abf09-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="abf09-110">*ppIMetadataQueryWriter* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="abf09-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abf09-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="abf09-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="abf09-112">Puntatore che riceve un writer di query di metadati per il frame.</span><span class="sxs-lookup"><span data-stu-id="abf09-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abf09-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abf09-113">Return value</span></span>

<span data-ttu-id="abf09-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="abf09-114">Type: **HRESULT**</span></span>

<span data-ttu-id="abf09-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="abf09-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="abf09-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="abf09-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="abf09-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="abf09-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="abf09-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abf09-118">Requirements</span></span>



| <span data-ttu-id="abf09-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="abf09-119">Requirement</span></span> | <span data-ttu-id="abf09-120">Valore</span><span class="sxs-lookup"><span data-stu-id="abf09-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abf09-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abf09-121">Minimum supported client</span></span><br/> | <span data-ttu-id="abf09-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="abf09-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="abf09-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abf09-123">Minimum supported server</span></span><br/> | <span data-ttu-id="abf09-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="abf09-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="abf09-125">DLL</span><span class="sxs-lookup"><span data-stu-id="abf09-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abf09-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="abf09-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




