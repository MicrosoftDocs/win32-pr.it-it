---
description: Funzione proxy per il metodo Initialize.
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: Funzione IWICBitmapEncoder_Initialize_Proxy
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
ms.openlocfilehash: c1a2e684059b75e41c1d89e2d3dd5379cc208b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316390"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a><span data-ttu-id="21f07-103">IWICBitmapEncoder \_ Inizializza la \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="21f07-103">IWICBitmapEncoder\_Initialize\_Proxy function</span></span>

<span data-ttu-id="21f07-104">Funzione proxy per il metodo [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) .</span><span class="sxs-lookup"><span data-stu-id="21f07-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f07-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21f07-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a><span data-ttu-id="21f07-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="21f07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f07-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f07-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f07-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="21f07-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="21f07-109">Puntatore a questo oggetto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="21f07-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="21f07-110">*pIStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f07-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f07-111">Tipo: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="21f07-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="21f07-112">Flusso di output.</span><span class="sxs-lookup"><span data-stu-id="21f07-112">The output stream.</span></span>

</dd> <dt>

<span data-ttu-id="21f07-113">_cacheOption \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f07-113">_cacheOption\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f07-114">Tipo: **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span><span class="sxs-lookup"><span data-stu-id="21f07-114">Type: **[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span></span>

<span data-ttu-id="21f07-115">[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) utilizzato per l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="21f07-115">The [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) used on initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f07-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21f07-116">Return value</span></span>

<span data-ttu-id="21f07-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="21f07-117">Type: **HRESULT**</span></span>

<span data-ttu-id="21f07-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="21f07-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21f07-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21f07-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f07-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="21f07-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="21f07-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21f07-121">Requirements</span></span>



| <span data-ttu-id="21f07-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="21f07-122">Requirement</span></span> | <span data-ttu-id="21f07-123">Valore</span><span class="sxs-lookup"><span data-stu-id="21f07-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21f07-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21f07-124">Minimum supported client</span></span><br/> | <span data-ttu-id="21f07-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21f07-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="21f07-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21f07-126">Minimum supported server</span></span><br/> | <span data-ttu-id="21f07-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="21f07-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="21f07-128">DLL</span><span class="sxs-lookup"><span data-stu-id="21f07-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21f07-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21f07-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

