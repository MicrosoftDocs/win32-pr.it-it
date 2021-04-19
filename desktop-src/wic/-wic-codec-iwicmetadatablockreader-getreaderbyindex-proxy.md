---
description: Funzione proxy per il metodo GetReaderByIndex.
ms.assetid: 9d70b339-9772-4c13-949e-109f354f9986
title: Funzione IWICMetadataBlockReader_GetReaderByIndex_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetReaderByIndex_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e2fc967f810b9ac8e43ad7da543bb1723500da48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317259"
---
# <a name="iwicmetadatablockreader_getreaderbyindex_proxy-function"></a><span data-ttu-id="9a29d-103">IWICMetadataBlockReader \_ GetReaderByIndex- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="9a29d-103">IWICMetadataBlockReader\_GetReaderByIndex\_Proxy function</span></span>

<span data-ttu-id="9a29d-104">Funzione proxy per il metodo [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) .</span><span class="sxs-lookup"><span data-stu-id="9a29d-104">Proxy function for the [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a29d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a29d-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetReaderByIndex_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _In_  UINT                    nIndex,
  _Out_ IWICMetadataReader      **ppIMetadataReader
);
```



## <a name="parameters"></a><span data-ttu-id="9a29d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a29d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a29d-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a29d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a29d-108">Tipo: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="9a29d-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="9a29d-109">Puntatore a questo oggetto [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="9a29d-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="9a29d-110">*nIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a29d-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a29d-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9a29d-111">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="9a29d-112">*ppIMetadataReader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9a29d-112">*ppIMetadataReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a29d-113">Tipo: **[ **IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span><span class="sxs-lookup"><span data-stu-id="9a29d-113">Type: **[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a29d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a29d-114">Return value</span></span>

<span data-ttu-id="9a29d-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9a29d-115">Type: **HRESULT**</span></span>

<span data-ttu-id="9a29d-116">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9a29d-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a29d-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a29d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a29d-118">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="9a29d-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9a29d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a29d-119">Requirements</span></span>



| <span data-ttu-id="9a29d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a29d-120">Requirement</span></span> | <span data-ttu-id="9a29d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9a29d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a29d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a29d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9a29d-123">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a29d-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9a29d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a29d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9a29d-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9a29d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9a29d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9a29d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a29d-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a29d-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




