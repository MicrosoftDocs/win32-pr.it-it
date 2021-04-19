---
description: Funzione proxy per il metodo GetThumbnail.
ms.assetid: 37a6ba78-0d1b-47f6-9b12-8ad123c8ee86
title: Funzione IWICBitmapDecoder_GetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7412999b1a685c0188e0f277e073791d753a245b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319570"
---
# <a name="iwicbitmapdecoder_getthumbnail_proxy-function"></a><span data-ttu-id="925ba-103">\_Funzione proxy IWICBitmapDecoder GetThumbnail \_</span><span class="sxs-lookup"><span data-stu-id="925ba-103">IWICBitmapDecoder\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="925ba-104">Funzione proxy per il metodo [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="925ba-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="925ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="925ba-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetThumbnail_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="925ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="925ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="925ba-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="925ba-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="925ba-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="925ba-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="925ba-109">Puntatore a questo oggetto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="925ba-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="925ba-110">*ppIThumbnail* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="925ba-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="925ba-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="925ba-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="925ba-112">Puntatore che riceve un puntatore all' [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) dell'anteprima.</span><span class="sxs-lookup"><span data-stu-id="925ba-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="925ba-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="925ba-113">Return value</span></span>

<span data-ttu-id="925ba-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="925ba-114">Type: **HRESULT**</span></span>

<span data-ttu-id="925ba-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="925ba-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="925ba-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="925ba-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="925ba-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="925ba-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="925ba-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="925ba-118">Requirements</span></span>



| <span data-ttu-id="925ba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="925ba-119">Requirement</span></span> | <span data-ttu-id="925ba-120">Valore</span><span class="sxs-lookup"><span data-stu-id="925ba-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="925ba-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="925ba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="925ba-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="925ba-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="925ba-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="925ba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="925ba-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="925ba-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="925ba-125">DLL</span><span class="sxs-lookup"><span data-stu-id="925ba-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="925ba-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="925ba-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




