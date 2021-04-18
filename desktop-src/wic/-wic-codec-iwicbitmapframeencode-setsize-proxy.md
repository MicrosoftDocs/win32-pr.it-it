---
description: Funzione proxy per il metodo sesize.
ms.assetid: 28b4967f-4c8a-475c-8f86-c19e5d424a26
title: Funzione IWICBitmapFrameEncode_SetSize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0a8046ede01cdd30d6a30eb81cbc1617531ef1d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314479"
---
# <a name="iwicbitmapframeencode_setsize_proxy-function"></a><span data-ttu-id="419d6-103">IWICBitmapFrameEncode- \_ \_ funzione proxy di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="419d6-103">IWICBitmapFrameEncode\_SetSize\_Proxy function</span></span>

<span data-ttu-id="419d6-104">Funzione proxy per il metodo [**sesize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) .</span><span class="sxs-lookup"><span data-stu-id="419d6-104">Proxy function for the [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="419d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="419d6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetSize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  uiWidth,
  _In_ UINT                  uiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="419d6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="419d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="419d6-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="419d6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="419d6-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="419d6-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="419d6-109">Puntatore a questo oggetto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="419d6-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="419d6-110">*uiWidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="419d6-110">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="419d6-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="419d6-111">Type: **UINT**</span></span>

<span data-ttu-id="419d6-112">Larghezza dell'immagine di output.</span><span class="sxs-lookup"><span data-stu-id="419d6-112">The width of the output image.</span></span>

</dd> <dt>

<span data-ttu-id="419d6-113">*uiHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="419d6-113">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="419d6-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="419d6-114">Type: **UINT**</span></span>

<span data-ttu-id="419d6-115">Altezza dell'immagine di output.</span><span class="sxs-lookup"><span data-stu-id="419d6-115">The height of the output image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="419d6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="419d6-116">Return value</span></span>

<span data-ttu-id="419d6-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="419d6-117">Type: **HRESULT**</span></span>

<span data-ttu-id="419d6-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="419d6-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="419d6-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="419d6-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="419d6-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="419d6-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="419d6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="419d6-121">Requirements</span></span>



| <span data-ttu-id="419d6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="419d6-122">Requirement</span></span> | <span data-ttu-id="419d6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="419d6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="419d6-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="419d6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="419d6-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="419d6-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="419d6-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="419d6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="419d6-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="419d6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="419d6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="419d6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="419d6-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="419d6-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




