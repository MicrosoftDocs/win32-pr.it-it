---
description: Funzione proxy per il metodo getsolution.
ms.assetid: 5e261c2b-534a-4875-a84f-7251d54f15c6
title: Funzione IWICBitmapSource_GetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0bcd63c01bf99e426cdbf5044223a40308fb5e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231898"
---
# <a name="iwicbitmapsource_getresolution_proxy-function"></a><span data-ttu-id="afa02-103">\_Funzione proxy Getsolution IWICBitmapSource \_</span><span class="sxs-lookup"><span data-stu-id="afa02-103">IWICBitmapSource\_GetResolution\_Proxy function</span></span>

<span data-ttu-id="afa02-104">Funzione proxy per il metodo [**getsolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) .</span><span class="sxs-lookup"><span data-stu-id="afa02-104">Proxy function for the [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa02-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afa02-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetResolution_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ double           *pDpiX,
  _Out_ double           *pDpiY
);
```



## <a name="parameters"></a><span data-ttu-id="afa02-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="afa02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afa02-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afa02-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afa02-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="afa02-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="afa02-109">Puntatore a questo oggetto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="afa02-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="afa02-110">*pDpiX* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="afa02-110">*pDpiX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afa02-111">Tipo: \**Double \** _</span><span class="sxs-lookup"><span data-stu-id="afa02-111">Type: \**double\** _</span></span>

<span data-ttu-id="afa02-112">Puntatore che riceve la risoluzione dpi dell'asse x.</span><span class="sxs-lookup"><span data-stu-id="afa02-112">A pointer that receives the x-axis dpi resolution.</span></span>

</dd> <dt>

<span data-ttu-id="afa02-113">_pDpiY \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="afa02-113">_pDpiY\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afa02-114">Tipo: \**Double \** _</span><span class="sxs-lookup"><span data-stu-id="afa02-114">Type: \**double\** _</span></span>

<span data-ttu-id="afa02-115">Puntatore che riceve la risoluzione dpi dell'asse y.</span><span class="sxs-lookup"><span data-stu-id="afa02-115">A pointer that receives the y-axis dpi resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afa02-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="afa02-116">Return value</span></span>

<span data-ttu-id="afa02-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="afa02-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="afa02-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="afa02-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="afa02-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="afa02-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="afa02-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="afa02-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="afa02-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afa02-121">Requirements</span></span>



| <span data-ttu-id="afa02-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="afa02-122">Requirement</span></span> | <span data-ttu-id="afa02-123">Valore</span><span class="sxs-lookup"><span data-stu-id="afa02-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa02-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afa02-124">Minimum supported client</span></span><br/> | <span data-ttu-id="afa02-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="afa02-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="afa02-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afa02-126">Minimum supported server</span></span><br/> | <span data-ttu-id="afa02-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="afa02-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="afa02-128">DLL</span><span class="sxs-lookup"><span data-stu-id="afa02-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afa02-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afa02-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




