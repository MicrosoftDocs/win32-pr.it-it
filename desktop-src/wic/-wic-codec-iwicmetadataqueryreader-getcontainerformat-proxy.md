---
description: Funzione proxy per il metodo GetContainerFormat.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: Funzione IWICMetadataQueryReader_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d8138a1217611ff60be9001ce038f9ecfbe7e34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312978"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="c7acb-103">IWICMetadataQueryReader \_ GetContainerFormat- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="c7acb-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="c7acb-104">Funzione proxy per il metodo [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="c7acb-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7acb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7acb-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="c7acb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7acb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7acb-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7acb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7acb-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="c7acb-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="c7acb-109">Puntatore a questo oggetto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="c7acb-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="c7acb-110">*pguidContainerFormat* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c7acb-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7acb-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="c7acb-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="c7acb-112">Puntatore che riceve il GUID del formato cointainer.</span><span class="sxs-lookup"><span data-stu-id="c7acb-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7acb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7acb-113">Return value</span></span>

<span data-ttu-id="c7acb-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c7acb-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c7acb-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c7acb-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c7acb-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7acb-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7acb-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c7acb-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c7acb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7acb-118">Requirements</span></span>



| <span data-ttu-id="c7acb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7acb-119">Requirement</span></span> | <span data-ttu-id="c7acb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c7acb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7acb-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7acb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c7acb-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7acb-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c7acb-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7acb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c7acb-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7acb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c7acb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c7acb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7acb-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7acb-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




