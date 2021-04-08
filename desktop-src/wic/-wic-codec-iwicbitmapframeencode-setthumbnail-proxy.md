---
description: Funzione proxy per il metodo sethumbnail.
ms.assetid: 3ad473ec-9218-4ed1-961d-a2aa0d542119
title: Funzione IWICBitmapFrameEncode_SetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 052e73911178ef0db957c5dd8edcf6e9d6892ace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883413"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="94f6b-103">IWICBitmapFrameEncode \_ \_ funzione proxy di anteprima</span><span class="sxs-lookup"><span data-stu-id="94f6b-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="94f6b-104">Funzione proxy per il metodo [**sethumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="94f6b-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f6b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94f6b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="94f6b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="94f6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94f6b-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94f6b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94f6b-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="94f6b-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="94f6b-109">Puntatore a questo oggetto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="94f6b-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="94f6b-110">*pIThumbnail* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94f6b-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94f6b-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="94f6b-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="94f6b-112">Origine della bitmap da utilizzare come anteprima.</span><span class="sxs-lookup"><span data-stu-id="94f6b-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94f6b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94f6b-113">Return value</span></span>

<span data-ttu-id="94f6b-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="94f6b-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="94f6b-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="94f6b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="94f6b-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94f6b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="94f6b-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="94f6b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="94f6b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94f6b-118">Requirements</span></span>



| <span data-ttu-id="94f6b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="94f6b-119">Requirement</span></span> | <span data-ttu-id="94f6b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="94f6b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94f6b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94f6b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="94f6b-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94f6b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="94f6b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94f6b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="94f6b-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94f6b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="94f6b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="94f6b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94f6b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94f6b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




