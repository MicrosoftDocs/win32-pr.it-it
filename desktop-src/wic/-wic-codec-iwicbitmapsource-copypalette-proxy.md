---
description: IWICBitmapSource_CopyPalette_Proxy funzione proxy per il metodo CopyPalette.
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: IWICBitmapSource_CopyPalette_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ad9f5096aff7770a0b1624495c5c717440b6bd39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100499"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="a4b65-103">Funzione proxy IWICBitmapSource \_ CopyPalette \_</span><span class="sxs-lookup"><span data-stu-id="a4b65-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="a4b65-104">Funzione proxy per il [**metodo CopyPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)</span><span class="sxs-lookup"><span data-stu-id="a4b65-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b65-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4b65-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="a4b65-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4b65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b65-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4b65-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b65-108">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="a4b65-108">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="a4b65-109">Puntatore a [**questo oggetto IWICBitmapSource.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)</span><span class="sxs-lookup"><span data-stu-id="a4b65-109">Pointer to this [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="a4b65-110">*pIPalette* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a4b65-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b65-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="a4b65-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="a4b65-112">Tavolozza.</span><span class="sxs-lookup"><span data-stu-id="a4b65-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b65-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4b65-113">Return value</span></span>

<span data-ttu-id="a4b65-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a4b65-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a4b65-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a4b65-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4b65-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a4b65-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b65-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a4b65-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b65-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4b65-118">Requirements</span></span>



| <span data-ttu-id="a4b65-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4b65-119">Requirement</span></span> | <span data-ttu-id="a4b65-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a4b65-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b65-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4b65-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b65-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a4b65-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a4b65-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4b65-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b65-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a4b65-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a4b65-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b65-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4b65-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4b65-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




