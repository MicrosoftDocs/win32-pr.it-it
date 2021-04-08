---
description: Funzione proxy per il metodo CreateBitmapClipper.
ms.assetid: 163a8d7b-f22b-4ab5-9dba-00b0cdaab440
title: Funzione IWICImagingFactory_CreateBitmapClipper_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapClipper_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fb722622ce9a8b3ad3144bcf9ea53942c8e611aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968248"
---
# <a name="iwicimagingfactory_createbitmapclipper_proxy-function"></a><span data-ttu-id="9b2e6-103">IWICImagingFactory \_ CreateBitmapClipper- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="9b2e6-103">IWICImagingFactory\_CreateBitmapClipper\_Proxy function</span></span>

<span data-ttu-id="9b2e6-104">Funzione proxy per il metodo [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="9b2e6-104">Proxy function for the [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b2e6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b2e6-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapClipper_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapClipper  **ppIBitmapClipper
);
```



## <a name="parameters"></a><span data-ttu-id="9b2e6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b2e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b2e6-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b2e6-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2e6-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="9b2e6-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="9b2e6-109">_ppIBitmapClipper \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9b2e6-109">_ppIBitmapClipper\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2e6-110">Tipo: **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span><span class="sxs-lookup"><span data-stu-id="9b2e6-110">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span></span>

<span data-ttu-id="9b2e6-111">Puntatore che riceve un puntatore a un nuovo [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span><span class="sxs-lookup"><span data-stu-id="9b2e6-111">A pointer that receives a pointer to a new [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b2e6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b2e6-112">Return value</span></span>

<span data-ttu-id="9b2e6-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9b2e6-113">Type: **HRESULT**</span></span>

<span data-ttu-id="9b2e6-114">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9b2e6-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b2e6-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b2e6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b2e6-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="9b2e6-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9b2e6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b2e6-117">Requirements</span></span>



| <span data-ttu-id="9b2e6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b2e6-118">Requirement</span></span> | <span data-ttu-id="9b2e6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9b2e6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b2e6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b2e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9b2e6-121">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b2e6-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9b2e6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b2e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9b2e6-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9b2e6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9b2e6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9b2e6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b2e6-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b2e6-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




