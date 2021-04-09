---
description: Funzione proxy per il metodo CreateBitmapFromSource.
ms.assetid: 7d000377-1855-4971-b782-4c0bf7968c5f
title: Funzione IWICImagingFactory_CreateBitmapFromSource_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7f7be9ca9eaa8aa14dcaf3617face2dff2f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968694"
---
# <a name="iwicimagingfactory_createbitmapfromsource_proxy-function"></a><span data-ttu-id="42822-103">IWICImagingFactory \_ CreateBitmapFromSource- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="42822-103">IWICImagingFactory\_CreateBitmapFromSource\_Proxy function</span></span>

<span data-ttu-id="42822-104">Funzione proxy per il metodo [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) .</span><span class="sxs-lookup"><span data-stu-id="42822-104">Proxy function for the [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42822-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42822-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromSource_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  IWICBitmapSource           *pIBitmapSource,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="42822-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="42822-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42822-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42822-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42822-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="42822-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="42822-109">_pIBitmapSource \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42822-109">_pIBitmapSource\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42822-110">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="42822-110">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="42822-111">[_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) da cui creare la bitmap.</span><span class="sxs-lookup"><span data-stu-id="42822-111">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="42822-112">*opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42822-112">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42822-113">Tipo: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="42822-113">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="42822-114">Opzioni della cache della nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="42822-114">The cache options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="42822-115">*ppIBitmap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="42822-115">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42822-116">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="42822-116">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="42822-117">Puntatore che riceve un puntatore alla nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="42822-117">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42822-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42822-118">Return value</span></span>

<span data-ttu-id="42822-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="42822-119">Type: **HRESULT**</span></span>

<span data-ttu-id="42822-120">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="42822-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42822-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42822-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="42822-122">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="42822-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="42822-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42822-123">Requirements</span></span>



| <span data-ttu-id="42822-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="42822-124">Requirement</span></span> | <span data-ttu-id="42822-125">Valore</span><span class="sxs-lookup"><span data-stu-id="42822-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42822-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42822-126">Minimum supported client</span></span><br/> | <span data-ttu-id="42822-127">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42822-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="42822-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42822-128">Minimum supported server</span></span><br/> | <span data-ttu-id="42822-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42822-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="42822-130">DLL</span><span class="sxs-lookup"><span data-stu-id="42822-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42822-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42822-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




