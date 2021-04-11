---
description: Funzione proxy per il metodo CreateQueryWriterFromBlockWriter.
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: Funzione IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c8c94b351e72fd7de367e5dd74a0c7ed62ce84f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232891"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a><span data-ttu-id="7fc7a-103">IWICComponentFactory \_ CreateQueryWriterFromBlockWriter- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="7fc7a-103">IWICComponentFactory\_CreateQueryWriterFromBlockWriter\_Proxy function</span></span>

<span data-ttu-id="7fc7a-104">Funzione proxy per il metodo [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) .</span><span class="sxs-lookup"><span data-stu-id="7fc7a-104">Proxy function for the [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fc7a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fc7a-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="7fc7a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fc7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fc7a-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fc7a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fc7a-108">Tipo: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="7fc7a-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="7fc7a-109">Puntatore a questo oggetto [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .</span><span class="sxs-lookup"><span data-stu-id="7fc7a-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="7fc7a-110">*pIBlockWriter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fc7a-110">*pIBlockWriter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fc7a-111">Tipo: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) \** _</span><span class="sxs-lookup"><span data-stu-id="7fc7a-111">Type: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)\** _</span></span>

</dd> <dt>

<span data-ttu-id="7fc7a-112">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7fc7a-112">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fc7a-113">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="7fc7a-113">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fc7a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fc7a-114">Return value</span></span>

<span data-ttu-id="7fc7a-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7fc7a-115">Type: **HRESULT**</span></span>

<span data-ttu-id="7fc7a-116">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7fc7a-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7fc7a-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7fc7a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fc7a-118">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7fc7a-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7fc7a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fc7a-119">Requirements</span></span>



| <span data-ttu-id="7fc7a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fc7a-120">Requirement</span></span> | <span data-ttu-id="7fc7a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7fc7a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc7a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fc7a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7fc7a-123">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fc7a-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7fc7a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fc7a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7fc7a-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7fc7a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7fc7a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7fc7a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fc7a-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fc7a-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




