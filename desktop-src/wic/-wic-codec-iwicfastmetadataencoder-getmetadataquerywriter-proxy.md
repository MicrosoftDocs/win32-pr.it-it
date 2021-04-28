---
description: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy funzione proxy per il metodo GetMetadataQueryWriter.
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b06bc6fbcdc65c9d1163ccb4a862d6046b455c9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097169"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="2672c-103">Funzione proxy IWICFastMetadataEncoder \_ GetMetadataQueryWriter \_</span><span class="sxs-lookup"><span data-stu-id="2672c-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="2672c-104">Funzione proxy per il [**metodo GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="2672c-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2672c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2672c-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="2672c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2672c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2672c-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2672c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2672c-108">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="2672c-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="2672c-109">Puntatore a [**questo oggetto IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="2672c-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="2672c-110">*ppIMetadataQueryWriter* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="2672c-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2672c-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="2672c-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="2672c-112">Puntatore che riceve un puntatore al writer di query dei metadati del codificatore.</span><span class="sxs-lookup"><span data-stu-id="2672c-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2672c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2672c-113">Return value</span></span>

<span data-ttu-id="2672c-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2672c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="2672c-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2672c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2672c-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="2672c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2672c-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="2672c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2672c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2672c-118">Requirements</span></span>



| <span data-ttu-id="2672c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2672c-119">Requirement</span></span> | <span data-ttu-id="2672c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2672c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2672c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2672c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2672c-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2672c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2672c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2672c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2672c-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2672c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2672c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2672c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2672c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2672c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




