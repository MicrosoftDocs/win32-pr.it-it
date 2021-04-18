---
description: Funzione proxy per il metodo GetSize.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: Funzione IWICBitmapSource_GetSize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313432"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a><span data-ttu-id="9d018-103">\_Funzione proxy IWICBitmapSource GetSize \_</span><span class="sxs-lookup"><span data-stu-id="9d018-103">IWICBitmapSource\_GetSize\_Proxy function</span></span>

<span data-ttu-id="9d018-104">Funzione proxy per il metodo [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) .</span><span class="sxs-lookup"><span data-stu-id="9d018-104">Proxy function for the [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d018-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d018-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="9d018-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d018-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d018-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d018-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d018-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="9d018-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="9d018-109">Puntatore a questo oggetto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="9d018-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="9d018-110">*puiWidth* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d018-110">*puiWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d018-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="9d018-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="9d018-112">Puntatore che riceve la larghezza in pixel della bitmap.</span><span class="sxs-lookup"><span data-stu-id="9d018-112">A pointer that receives the pixel width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="9d018-113">_puiHeight \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d018-113">_puiHeight\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d018-114">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="9d018-114">Type: \**UINT\** _</span></span>

<span data-ttu-id="9d018-115">Puntatore che riceve l'altezza in pixel della bitmap</span><span class="sxs-lookup"><span data-stu-id="9d018-115">A pointer that receives the pixel height of the bitmap</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d018-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d018-116">Return value</span></span>

<span data-ttu-id="9d018-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9d018-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9d018-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9d018-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d018-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d018-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d018-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="9d018-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9d018-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d018-121">Requirements</span></span>



| <span data-ttu-id="9d018-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d018-122">Requirement</span></span> | <span data-ttu-id="9d018-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9d018-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d018-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d018-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9d018-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d018-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9d018-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d018-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9d018-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d018-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9d018-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9d018-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d018-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d018-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




