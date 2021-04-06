---
description: Funzione proxy per il metodo CreateQueryWriter.
ms.assetid: 7f925117-6244-4be6-bcef-fa852672ac64
title: Funzione IWICImagingFactory_CreateQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ae0d41b9ceb652f23084c026b130bf711c44f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759062"
---
# <a name="iwicimagingfactory_createquerywriter_proxy-function"></a><span data-ttu-id="bb63c-103">IWICImagingFactory \_ CreateQueryWriter- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="bb63c-103">IWICImagingFactory\_CreateQueryWriter\_Proxy function</span></span>

<span data-ttu-id="bb63c-104">Funzione proxy per il metodo [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="bb63c-104">Proxy function for the [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb63c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb63c-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriter_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        REFGUID                 guidMetadataFormat,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="bb63c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb63c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb63c-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb63c-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb63c-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="bb63c-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="bb63c-109">_guidMetadataFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb63c-109">_guidMetadataFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb63c-110">Tipo: **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="bb63c-110">Type: **REFGUID**</span></span>

<span data-ttu-id="bb63c-111">GUID per il formato dei metadati desiderato.</span><span class="sxs-lookup"><span data-stu-id="bb63c-111">The GUID for the desired metadata format.</span></span>

</dd> <dt>

<span data-ttu-id="bb63c-112">*pguidVendor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb63c-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb63c-113">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="bb63c-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="bb63c-114">GUID del fornitore del writer di metadati.</span><span class="sxs-lookup"><span data-stu-id="bb63c-114">The vendor GUID of the metadata writer.</span></span>

</dd> <dt>

<span data-ttu-id="bb63c-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bb63c-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb63c-116">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="bb63c-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="bb63c-117">Puntatore che riceve un puntatore a un nuovo [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="bb63c-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb63c-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb63c-118">Return value</span></span>

<span data-ttu-id="bb63c-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bb63c-119">Type: **HRESULT**</span></span>

<span data-ttu-id="bb63c-120">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bb63c-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb63c-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb63c-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb63c-122">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="bb63c-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bb63c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb63c-123">Requirements</span></span>



| <span data-ttu-id="bb63c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb63c-124">Requirement</span></span> | <span data-ttu-id="bb63c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="bb63c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb63c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb63c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bb63c-127">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb63c-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bb63c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb63c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bb63c-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bb63c-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bb63c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bb63c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb63c-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb63c-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




