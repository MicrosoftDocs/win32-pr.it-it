---
description: Funzione proxy per il metodo di risoluzione.
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: Funzione IWICBitmapFrameEncode_SetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9801384e305f2449c6a31b80cb238fc92f7b63b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313434"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="e6167-103">IWICBitmapFrameEncode- \_ \_ funzione proxy di risoluzione</span><span class="sxs-lookup"><span data-stu-id="e6167-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="e6167-104">Funzione proxy per il metodo di [**risoluzione**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="e6167-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6167-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6167-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="e6167-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6167-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6167-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6167-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6167-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="e6167-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="e6167-109">Puntatore a questo oggetto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="e6167-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="e6167-110">*DpiX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6167-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6167-111">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="e6167-111">Type: **double**</span></span>

<span data-ttu-id="e6167-112">Valore di risoluzione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="e6167-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="e6167-113">*DpiY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6167-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6167-114">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="e6167-114">Type: **double**</span></span>

<span data-ttu-id="e6167-115">Valore di risoluzione verticale.</span><span class="sxs-lookup"><span data-stu-id="e6167-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6167-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6167-116">Return value</span></span>

<span data-ttu-id="e6167-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e6167-117">Type: **HRESULT**</span></span>

<span data-ttu-id="e6167-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e6167-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6167-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6167-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6167-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e6167-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e6167-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6167-121">Requirements</span></span>



| <span data-ttu-id="e6167-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6167-122">Requirement</span></span> | <span data-ttu-id="e6167-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e6167-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6167-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6167-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6167-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6167-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e6167-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6167-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6167-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6167-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e6167-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e6167-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6167-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6167-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




