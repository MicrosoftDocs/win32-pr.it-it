---
description: Funzione proxy per il metodo CreateStream.
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: Funzione IWICImagingFactory_CreateStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 61670dbe3c1689a3d5b8030585a2b13d281efd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317260"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a><span data-ttu-id="17d0f-103">IWICImagingFactory \_ CreateStream- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="17d0f-103">IWICImagingFactory\_CreateStream\_Proxy function</span></span>

<span data-ttu-id="17d0f-104">Funzione proxy per il metodo [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) .</span><span class="sxs-lookup"><span data-stu-id="17d0f-104">Proxy function for the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d0f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17d0f-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a><span data-ttu-id="17d0f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17d0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d0f-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17d0f-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17d0f-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="17d0f-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="17d0f-109">_ppIWICStream \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="17d0f-109">_ppIWICStream\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17d0f-110">Tipo: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span><span class="sxs-lookup"><span data-stu-id="17d0f-110">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span></span>

<span data-ttu-id="17d0f-111">Puntatore che riceve un puntatore a un nuovo [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span><span class="sxs-lookup"><span data-stu-id="17d0f-111">A pointer that receives a pointer to a new [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d0f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17d0f-112">Return value</span></span>

<span data-ttu-id="17d0f-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="17d0f-113">Type: **HRESULT**</span></span>

<span data-ttu-id="17d0f-114">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="17d0f-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17d0f-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17d0f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="17d0f-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="17d0f-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="17d0f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17d0f-117">Requirements</span></span>



| <span data-ttu-id="17d0f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="17d0f-118">Requirement</span></span> | <span data-ttu-id="17d0f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="17d0f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17d0f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17d0f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17d0f-121">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17d0f-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="17d0f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17d0f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17d0f-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17d0f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="17d0f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="17d0f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17d0f-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17d0f-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




