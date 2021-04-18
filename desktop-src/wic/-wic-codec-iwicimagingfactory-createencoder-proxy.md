---
description: Funzione proxy per il metodo CreateEncoder.
ms.assetid: e3ffad7f-eb0e-481d-81ee-caf18e14ba59
title: Funzione IWICImagingFactory_CreateEncoder_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateEncoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 38e5dd19ddc07de42f8be9e8c887a4f412a853b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313424"
---
# <a name="iwicimagingfactory_createencoder_proxy-function"></a><span data-ttu-id="cc6fc-103">IWICImagingFactory \_ CreateEncoder- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="cc6fc-103">IWICImagingFactory\_CreateEncoder\_Proxy function</span></span>

<span data-ttu-id="cc6fc-104">Funzione proxy per il metodo [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) .</span><span class="sxs-lookup"><span data-stu-id="cc6fc-104">Proxy function for the [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc6fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc6fc-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateEncoder_Proxy(
  _In_           IWICImagingFactory *pFactory,
  _In_           REFGUID            guidContainerFormat,
  _In_opt_ const GUID               *pguidVendor,
  _Out_          IWICBitmapEncoder  **ppIEncoder
);
```



## <a name="parameters"></a><span data-ttu-id="cc6fc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc6fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc6fc-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc6fc-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6fc-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="cc6fc-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="cc6fc-109">_guidContainerFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc6fc-109">_guidContainerFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6fc-110">Tipo: **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="cc6fc-110">Type: **REFGUID**</span></span>

<span data-ttu-id="cc6fc-111">GUID per il formato del contenitore desiderato.</span><span class="sxs-lookup"><span data-stu-id="cc6fc-111">The GUID for the desired container format.</span></span>

</dd> <dt>

<span data-ttu-id="cc6fc-112">*pguidVendor* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="cc6fc-112">*pguidVendor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6fc-113">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="cc6fc-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="cc6fc-114">GUID del fornitore per il codificatore.</span><span class="sxs-lookup"><span data-stu-id="cc6fc-114">The vendor GUID for the encoder.</span></span>

</dd> <dt>

<span data-ttu-id="cc6fc-115">_ppIEncoder \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cc6fc-115">_ppIEncoder\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6fc-116">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="cc6fc-116">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span></span>

<span data-ttu-id="cc6fc-117">Puntatore che riceve un puntatore a un nuovo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="cc6fc-117">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc6fc-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc6fc-118">Return value</span></span>

<span data-ttu-id="cc6fc-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cc6fc-119">Type: **HRESULT**</span></span>

<span data-ttu-id="cc6fc-120">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc6fc-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc6fc-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc6fc-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc6fc-122">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="cc6fc-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cc6fc-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc6fc-123">Requirements</span></span>



| <span data-ttu-id="cc6fc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc6fc-124">Requirement</span></span> | <span data-ttu-id="cc6fc-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cc6fc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc6fc-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc6fc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cc6fc-127">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc6fc-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cc6fc-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc6fc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cc6fc-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc6fc-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cc6fc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="cc6fc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc6fc-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc6fc-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




