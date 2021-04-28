---
description: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy funzione proxy per il metodo GetMetadataQueryWriter.
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 798a9b5bafb2f5011e42e603b8b2c98b0ba79b37
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091169"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="64faa-103">Funzione proxy IWICBitmapEncoder \_ GetMetadataQueryWriter \_</span><span class="sxs-lookup"><span data-stu-id="64faa-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="64faa-104">Funzione proxy per il [**metodo GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="64faa-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="64faa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64faa-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="64faa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64faa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64faa-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64faa-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64faa-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="64faa-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="64faa-109">Puntatore a [**questo oggetto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="64faa-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="64faa-110">*ppIMetadataQueryWriter* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="64faa-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64faa-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="64faa-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="64faa-112">Puntatore che riceve un puntatore a [**un oggetto IWICMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="64faa-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64faa-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64faa-113">Return value</span></span>

<span data-ttu-id="64faa-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="64faa-114">Type: **HRESULT**</span></span>

<span data-ttu-id="64faa-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="64faa-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="64faa-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="64faa-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="64faa-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="64faa-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="64faa-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64faa-118">Requirements</span></span>



| <span data-ttu-id="64faa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="64faa-119">Requirement</span></span> | <span data-ttu-id="64faa-120">Valore</span><span class="sxs-lookup"><span data-stu-id="64faa-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64faa-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64faa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="64faa-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="64faa-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="64faa-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64faa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="64faa-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="64faa-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="64faa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="64faa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64faa-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="64faa-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




