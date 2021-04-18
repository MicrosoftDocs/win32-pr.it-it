---
description: Funzione proxy per il metodo GetMetadataByName.
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: Funzione IWICMetadataQueryReader_GetMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 96afa63f83e79f399b1c345d38ff2914307c2fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315978"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a><span data-ttu-id="b5a8a-103">IWICMetadataQueryReader \_ GetMetadataByName- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="b5a8a-103">IWICMetadataQueryReader\_GetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="b5a8a-104">Funzione proxy per il metodo [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="b5a8a-104">Proxy function for the [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5a8a-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="b5a8a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5a8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5a8a-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5a8a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a8a-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="b5a8a-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="b5a8a-109">Puntatore a questo oggetto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="b5a8a-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="b5a8a-110">*wzName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5a8a-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a8a-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="b5a8a-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="b5a8a-112">Nome dell'elemento di metadati richiesto.</span><span class="sxs-lookup"><span data-stu-id="b5a8a-112">The name of the requested metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="b5a8a-113">*pvarValue* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b5a8a-113">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a8a-114">Tipo: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="b5a8a-114">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="b5a8a-115">Puntatore che riceve la proprietà dei metadati.</span><span class="sxs-lookup"><span data-stu-id="b5a8a-115">Pointer that receives the metadata property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5a8a-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5a8a-116">Return value</span></span>

<span data-ttu-id="b5a8a-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b5a8a-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b5a8a-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b5a8a-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5a8a-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5a8a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5a8a-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b5a8a-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a8a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5a8a-121">Requirements</span></span>



| <span data-ttu-id="b5a8a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a8a-122">Requirement</span></span> | <span data-ttu-id="b5a8a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b5a8a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a8a-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5a8a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a8a-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5a8a-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b5a8a-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5a8a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a8a-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b5a8a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b5a8a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b5a8a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5a8a-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5a8a-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

