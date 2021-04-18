---
description: Funzione proxy per il metodo CreatePalette.
ms.assetid: c83b4239-ce6b-4a4c-ab70-df31dfcdd26c
title: Funzione IWICImagingFactory_CreatePalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreatePalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 626c05ec5e4e365cf61304c4b33e621967cea5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319119"
---
# <a name="iwicimagingfactory_createpalette_proxy-function"></a><span data-ttu-id="fbea4-103">IWICImagingFactory \_ CreatePalette- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="fbea4-103">IWICImagingFactory\_CreatePalette\_Proxy function</span></span>

<span data-ttu-id="fbea4-104">Funzione proxy per il metodo [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) .</span><span class="sxs-lookup"><span data-stu-id="fbea4-104">Proxy function for the [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbea4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbea4-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreatePalette_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICPalette        **ppIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="fbea4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbea4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbea4-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbea4-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbea4-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="fbea4-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="fbea4-109">_ppIPalette \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fbea4-109">_ppIPalette\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbea4-110">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span><span class="sxs-lookup"><span data-stu-id="fbea4-110">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span></span>

<span data-ttu-id="fbea4-111">Puntatore che riceve un puntatore a un nuovo [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span><span class="sxs-lookup"><span data-stu-id="fbea4-111">A pointer that receives a pointer to a new [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbea4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbea4-112">Return value</span></span>

<span data-ttu-id="fbea4-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fbea4-113">Type: **HRESULT**</span></span>

<span data-ttu-id="fbea4-114">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fbea4-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbea4-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fbea4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbea4-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="fbea4-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fbea4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbea4-117">Requirements</span></span>



| <span data-ttu-id="fbea4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbea4-118">Requirement</span></span> | <span data-ttu-id="fbea4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fbea4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbea4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbea4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fbea4-121">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbea4-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fbea4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbea4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fbea4-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fbea4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fbea4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fbea4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbea4-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbea4-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




