---
description: Funzione proxy per il metodo GetPixelFormat.
ms.assetid: 0879bfb7-0175-4275-a093-a69b39c66a41
title: Funzione IWICBitmapSource_GetPixelFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetPixelFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff795dd028c8d8f1e18a944df60a87f1e7cee670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313431"
---
# <a name="iwicbitmapsource_getpixelformat_proxy-function"></a><span data-ttu-id="b3f6f-103">IWICBitmapSource \_ GetPixelFormat- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="b3f6f-103">IWICBitmapSource\_GetPixelFormat\_Proxy function</span></span>

<span data-ttu-id="b3f6f-104">Funzione proxy per il metodo [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) .</span><span class="sxs-lookup"><span data-stu-id="b3f6f-104">Proxy function for the [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f6f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3f6f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetPixelFormat_Proxy(
  _In_  IWICBitmapSource   *THIS_PTR,
  _Out_ WICPixelFormatGUID *pPixelFormat
);
```



## <a name="parameters"></a><span data-ttu-id="b3f6f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3f6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3f6f-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3f6f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3f6f-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="b3f6f-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="b3f6f-109">Puntatore a questo oggetto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="b3f6f-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="b3f6f-110">*pPixelFormat* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b3f6f-110">*pPixelFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3f6f-111">Tipo: \**WICPixelFormatGUID \** _</span><span class="sxs-lookup"><span data-stu-id="b3f6f-111">Type: \**WICPixelFormatGUID\** _</span></span>

<span data-ttu-id="b3f6f-112">Puntatore che riceve il GUID del formato pixel in cui è archiviata la bitmap.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-112">A pointer that receives the pixel format GUID the bitmap is stored in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3f6f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3f6f-113">Return value</span></span>

<span data-ttu-id="b3f6f-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b3f6f-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b3f6f-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3f6f-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b3f6f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3f6f-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b3f6f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b3f6f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3f6f-118">Requirements</span></span>



| <span data-ttu-id="b3f6f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3f6f-119">Requirement</span></span> | <span data-ttu-id="b3f6f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b3f6f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f6f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3f6f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b3f6f-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3f6f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b3f6f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3f6f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b3f6f-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3f6f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b3f6f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b3f6f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3f6f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3f6f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




