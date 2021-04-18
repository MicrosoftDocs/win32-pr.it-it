---
description: Funzione proxy per il metodo CreateComponentInfo.
ms.assetid: 7d3b791a-d65e-4b90-8050-373a949e6d9c
title: Funzione IWICImagingFactory_CreateComponentInfo_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateComponentInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 208b8b09b402e01f59a925f3dc6de6694b196db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347861"
---
# <a name="iwicimagingfactory_createcomponentinfo_proxy-function"></a><span data-ttu-id="4933d-103">IWICImagingFactory \_ CreateComponentInfo- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="4933d-103">IWICImagingFactory\_CreateComponentInfo\_Proxy function</span></span>

<span data-ttu-id="4933d-104">Funzione proxy per il metodo [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="4933d-104">Proxy function for the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4933d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4933d-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateComponentInfo_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  REFCLSID           clsidComponent,
  _Out_ IWICComponentInfo  **ppIInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4933d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4933d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4933d-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4933d-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4933d-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="4933d-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="4933d-109">_clsidComponent \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4933d-109">_clsidComponent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4933d-110">Tipo: **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="4933d-110">Type: **REFCLSID**</span></span>

<span data-ttu-id="4933d-111">CLSID per il componente desiderato.</span><span class="sxs-lookup"><span data-stu-id="4933d-111">The CLSID for the desired component.</span></span>

</dd> <dt>

<span data-ttu-id="4933d-112">*ppIInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4933d-112">*ppIInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4933d-113">Tipo: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="4933d-113">Type: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span></span>

<span data-ttu-id="4933d-114">Puntatore che riceve un puntatore a un nuovo [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span><span class="sxs-lookup"><span data-stu-id="4933d-114">A pointer that receives a pointer to a new [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4933d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4933d-115">Return value</span></span>

<span data-ttu-id="4933d-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4933d-116">Type: **HRESULT**</span></span>

<span data-ttu-id="4933d-117">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4933d-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4933d-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4933d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4933d-119">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="4933d-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4933d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4933d-120">Requirements</span></span>



| <span data-ttu-id="4933d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4933d-121">Requirement</span></span> | <span data-ttu-id="4933d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4933d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4933d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4933d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4933d-124">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4933d-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4933d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4933d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4933d-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4933d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4933d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4933d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4933d-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4933d-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




