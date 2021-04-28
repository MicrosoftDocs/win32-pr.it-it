---
description: IWICBitmapEncoder_Initialize_Proxy funzione proxy per il metodo Initialize.
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d346d1379ae92f19a530c65daff07cb98b2e0e50
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100619"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a><span data-ttu-id="bd126-103">Funzione IWICBitmapEncoder \_ Initialize \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="bd126-103">IWICBitmapEncoder\_Initialize\_Proxy function</span></span>

<span data-ttu-id="bd126-104">Funzione proxy per il [**metodo Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)</span><span class="sxs-lookup"><span data-stu-id="bd126-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd126-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd126-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a><span data-ttu-id="bd126-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd126-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd126-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd126-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd126-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="bd126-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="bd126-109">Puntatore a [**questo oggetto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="bd126-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="bd126-110">*pIStream* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="bd126-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd126-111">Tipo: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***</span><span class="sxs-lookup"><span data-stu-id="bd126-111">Type: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***</span></span>

<span data-ttu-id="bd126-112">Flusso di output.</span><span class="sxs-lookup"><span data-stu-id="bd126-112">The output stream.</span></span>

</dd> <dt>

<span data-ttu-id="bd126-113">*cacheOption* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="bd126-113">*cacheOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd126-114">Tipo: **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span><span class="sxs-lookup"><span data-stu-id="bd126-114">Type: **[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span></span>

<span data-ttu-id="bd126-115">[**WiCBitmapEncoderCacheOption usato**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) durante l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="bd126-115">The [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) used on initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd126-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd126-116">Return value</span></span>

<span data-ttu-id="bd126-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bd126-117">Type: **HRESULT**</span></span>

<span data-ttu-id="bd126-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bd126-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bd126-119">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="bd126-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd126-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="bd126-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bd126-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd126-121">Requirements</span></span>



| <span data-ttu-id="bd126-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd126-122">Requirement</span></span> | <span data-ttu-id="bd126-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bd126-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd126-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd126-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bd126-125">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bd126-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bd126-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd126-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bd126-127">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd126-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bd126-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bd126-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd126-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd126-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

