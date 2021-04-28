---
description: IWICBitmapFrameDecode_GetThumbnail_Proxy funzione proxy per il metodo GetThumbnail.
ms.assetid: 377f8aac-3cdc-44dc-8c60-9b6bce915486
title: IWICBitmapFrameDecode_GetThumbnail_Proxy funzione
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
ms.openlocfilehash: 7f3c94461ac13aa39d14b97f13fe5e9e8d7569a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113639"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="a5a3f-103">Funzione proxy IWICBitmapFrameDecode \_ GetThumbnail \_</span><span class="sxs-lookup"><span data-stu-id="a5a3f-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="a5a3f-104">Funzione proxy per [**il metodo GetThumbnail.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)</span><span class="sxs-lookup"><span data-stu-id="a5a3f-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5a3f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5a3f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="a5a3f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5a3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5a3f-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5a3f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a3f-108">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="a5a3f-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="a5a3f-109">Puntatore a [**questo oggetto IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="a5a3f-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="a5a3f-110">*ppIThumbnail* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="a5a3f-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a3f-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="a5a3f-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="a5a3f-112">Puntatore che riceve un puntatore [**all'oggetto IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) dell'anteprima.</span><span class="sxs-lookup"><span data-stu-id="a5a3f-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5a3f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5a3f-113">Return value</span></span>

<span data-ttu-id="a5a3f-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a5a3f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a5a3f-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a5a3f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a5a3f-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a5a3f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5a3f-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a5a3f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a5a3f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5a3f-118">Requirements</span></span>



| <span data-ttu-id="a5a3f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5a3f-119">Requirement</span></span> | <span data-ttu-id="a5a3f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a5a3f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a3f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5a3f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5a3f-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a5a3f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a5a3f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5a3f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5a3f-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5a3f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a5a3f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a5a3f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5a3f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5a3f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




