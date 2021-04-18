---
description: Funzione proxy per il metodo CreateBitmapFlipRotator.
ms.assetid: 1dc55744-8ae1-4d8b-9ffd-735ee45ceb47
title: Funzione IWICImagingFactory_CreateBitmapFlipRotator_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFlipRotator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dea33ea75ad9d9626b327ee0173abc2f28a3e417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316809"
---
# <a name="iwicimagingfactory_createbitmapfliprotator_proxy-function"></a><span data-ttu-id="f8015-103">IWICImagingFactory \_ CreateBitmapFlipRotator- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="f8015-103">IWICImagingFactory\_CreateBitmapFlipRotator\_Proxy function</span></span>

<span data-ttu-id="f8015-104">Funzione proxy per il metodo [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="f8015-104">Proxy function for the [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8015-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8015-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFlipRotator_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _Out_ IWICBitmapFlipRotator **ppIBitmapFlipRotator
);
```



## <a name="parameters"></a><span data-ttu-id="f8015-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8015-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8015-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8015-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8015-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="f8015-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="f8015-109">_ppIBitmapFlipRotator \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f8015-109">_ppIBitmapFlipRotator\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8015-110">Tipo: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span><span class="sxs-lookup"><span data-stu-id="f8015-110">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span></span>

<span data-ttu-id="f8015-111">Puntatore che riceve un puntatore a un nuovo [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span><span class="sxs-lookup"><span data-stu-id="f8015-111">A pointer that receives a pointer to a new [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8015-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8015-112">Return value</span></span>

<span data-ttu-id="f8015-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f8015-113">Type: **HRESULT**</span></span>

<span data-ttu-id="f8015-114">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f8015-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8015-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8015-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8015-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f8015-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f8015-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8015-117">Requirements</span></span>



| <span data-ttu-id="f8015-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8015-118">Requirement</span></span> | <span data-ttu-id="f8015-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f8015-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8015-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8015-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f8015-121">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8015-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f8015-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8015-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f8015-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8015-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f8015-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f8015-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8015-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8015-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




