---
description: Funzione proxy per il metodo GetThumbnail.
ms.assetid: 377f8aac-3cdc-44dc-8c60-9b6bce915486
title: Funzione IWICBitmapFrameDecode_GetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c29b62b4d3839b7cd3db51574f38ab824b215310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306668"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="bd6a7-103">\_Funzione proxy IWICBitmapFrameDecode GetThumbnail \_</span><span class="sxs-lookup"><span data-stu-id="bd6a7-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="bd6a7-104">Funzione proxy per il metodo [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="bd6a7-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd6a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd6a7-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="bd6a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd6a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd6a7-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd6a7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd6a7-108">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="bd6a7-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="bd6a7-109">Puntatore a questo oggetto [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="bd6a7-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="bd6a7-110">*ppIThumbnail* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bd6a7-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd6a7-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="bd6a7-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="bd6a7-112">Puntatore che riceve un puntatore all' [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) dell'anteprima.</span><span class="sxs-lookup"><span data-stu-id="bd6a7-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd6a7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd6a7-113">Return value</span></span>

<span data-ttu-id="bd6a7-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bd6a7-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bd6a7-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bd6a7-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bd6a7-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd6a7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd6a7-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="bd6a7-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bd6a7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd6a7-118">Requirements</span></span>



| <span data-ttu-id="bd6a7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd6a7-119">Requirement</span></span> | <span data-ttu-id="bd6a7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bd6a7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6a7-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd6a7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6a7-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd6a7-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bd6a7-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd6a7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6a7-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd6a7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bd6a7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bd6a7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd6a7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd6a7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




