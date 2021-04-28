---
description: IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy funzione proxy per il metodo GetMetadataQueryReader.
ms.assetid: 2a3e0a59-3524-4da4-993a-607a3727faba
title: IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c6c00cc4463bd8540e5baeb41a10577e9f67e85c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091139"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="b8522-103">Funzione proxy IWICBitmapFrameDecode \_ GetMetadataQueryReader \_</span><span class="sxs-lookup"><span data-stu-id="b8522-103">IWICBitmapFrameDecode\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="b8522-104">Funzione proxy per il [**metodo GetMetadataQueryReader.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)</span><span class="sxs-lookup"><span data-stu-id="b8522-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8522-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8522-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="b8522-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8522-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8522-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8522-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8522-108">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="b8522-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="b8522-109">Puntatore a [**questo oggetto IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="b8522-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="b8522-110">*ppIMetadataQueryReader* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b8522-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8522-111">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="b8522-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="b8522-112">Puntatore che riceve un puntatore a [**un oggetto IWICMetadataQueryReader.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)</span><span class="sxs-lookup"><span data-stu-id="b8522-112">A pointer that receives a pointer to an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8522-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8522-113">Return value</span></span>

<span data-ttu-id="b8522-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b8522-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b8522-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b8522-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b8522-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="b8522-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8522-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b8522-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b8522-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8522-118">Requirements</span></span>



| <span data-ttu-id="b8522-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8522-119">Requirement</span></span> | <span data-ttu-id="b8522-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b8522-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8522-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8522-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b8522-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b8522-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b8522-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8522-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b8522-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8522-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b8522-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b8522-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8522-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8522-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




