---
description: Funzione proxy per il metodo CreateMetadataWriterFromReader.
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: Funzione IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 31aea68f0f2d3c475368ad94b600280719261eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882446"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a><span data-ttu-id="ede55-103">IWICComponentFactory \_ CreateMetadataWriterFromReader- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="ede55-103">IWICComponentFactory\_CreateMetadataWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="ede55-104">Funzione proxy per il metodo [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) .</span><span class="sxs-lookup"><span data-stu-id="ede55-104">Proxy function for the [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ede55-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a><span data-ttu-id="ede55-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ede55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede55-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ede55-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede55-108">Tipo: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="ede55-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="ede55-109">Puntatore a questo oggetto [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .</span><span class="sxs-lookup"><span data-stu-id="ede55-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="ede55-110">*pIReader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ede55-110">*pIReader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede55-111">Tipo: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) \** _</span><span class="sxs-lookup"><span data-stu-id="ede55-111">Type: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\** _</span></span>

</dd> <dt>

<span data-ttu-id="ede55-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ede55-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede55-113">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="ede55-113">Type: \**const GUID\** _</span></span>

</dd> <dt>

<span data-ttu-id="ede55-114">_ppIWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ede55-114">_ppIWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ede55-115">Tipo: **[ **IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="ede55-115">Type: **[**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ede55-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ede55-116">Return value</span></span>

<span data-ttu-id="ede55-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ede55-117">Type: **HRESULT**</span></span>

<span data-ttu-id="ede55-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ede55-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ede55-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ede55-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ede55-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ede55-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ede55-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ede55-121">Requirements</span></span>



| <span data-ttu-id="ede55-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ede55-122">Requirement</span></span> | <span data-ttu-id="ede55-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ede55-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ede55-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ede55-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ede55-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ede55-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ede55-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ede55-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ede55-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ede55-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ede55-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ede55-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ede55-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ede55-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




