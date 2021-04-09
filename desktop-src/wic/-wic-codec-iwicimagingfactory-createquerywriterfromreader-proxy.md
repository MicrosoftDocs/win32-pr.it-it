---
description: Funzione proxy per il metodo CreateQueryWriterFromReader.
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: Funzione IWICImagingFactory_CreateQueryWriterFromReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4fb0d9c2346fe854cf23acee288ee1086828a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968334"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a><span data-ttu-id="de954-103">IWICImagingFactory \_ CreateQueryWriterFromReader- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="de954-103">IWICImagingFactory\_CreateQueryWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="de954-104">Funzione proxy per il metodo [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) .</span><span class="sxs-lookup"><span data-stu-id="de954-104">Proxy function for the [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de954-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de954-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="de954-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de954-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de954-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de954-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de954-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="de954-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="de954-109">_pIQueryReader \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de954-109">_pIQueryReader\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de954-110">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="de954-110">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="de954-111">Lettore di query di metadati da cui creare il writer di metadati.</span><span class="sxs-lookup"><span data-stu-id="de954-111">The metadata query reader to create the metadata writer from.</span></span>

</dd> <dt>

<span data-ttu-id="de954-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de954-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de954-113">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="de954-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="de954-114">GUID del fornitore per il writer di query dei metadati.</span><span class="sxs-lookup"><span data-stu-id="de954-114">The vendor GUID for the metadata query writer.</span></span>

</dd> <dt>

<span data-ttu-id="de954-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="de954-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de954-116">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="de954-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="de954-117">Puntatore che riceve un puntatore a un nuovo [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="de954-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de954-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de954-118">Return value</span></span>

<span data-ttu-id="de954-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="de954-119">Type: **HRESULT**</span></span>

<span data-ttu-id="de954-120">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="de954-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de954-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de954-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de954-122">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="de954-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="de954-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de954-123">Requirements</span></span>



| <span data-ttu-id="de954-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="de954-124">Requirement</span></span> | <span data-ttu-id="de954-125">Valore</span><span class="sxs-lookup"><span data-stu-id="de954-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de954-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de954-126">Minimum supported client</span></span><br/> | <span data-ttu-id="de954-127">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de954-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="de954-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de954-128">Minimum supported server</span></span><br/> | <span data-ttu-id="de954-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de954-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="de954-130">DLL</span><span class="sxs-lookup"><span data-stu-id="de954-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de954-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de954-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




