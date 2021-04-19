---
description: Funzione proxy per il metodo GetEnumerator.
ms.assetid: b45b240d-7540-4115-ac8b-401aaf400a9d
title: Funzione IWICMetadataQueryReader_GetEnumerator_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetEnumerator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a549cfb31691a32d1a7be76e1b051740ecf64e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317256"
---
# <a name="iwicmetadataqueryreader_getenumerator_proxy-function"></a><span data-ttu-id="47f79-103">\_ \_ Funzione proxy IWICMetadataQueryReader GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="47f79-103">IWICMetadataQueryReader\_GetEnumerator\_Proxy function</span></span>

<span data-ttu-id="47f79-104">Funzione proxy per il metodo [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) .</span><span class="sxs-lookup"><span data-stu-id="47f79-104">Proxy function for the [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f79-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47f79-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetEnumerator_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ IEnumString             **ppIEnumString
);
```



## <a name="parameters"></a><span data-ttu-id="47f79-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="47f79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f79-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47f79-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f79-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="47f79-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="47f79-109">Puntatore a questo oggetto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="47f79-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="47f79-110">*ppIEnumString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="47f79-110">*ppIEnumString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47f79-111">Tipo: **IEnumString \* \***</span><span class="sxs-lookup"><span data-stu-id="47f79-111">Type: **IEnumString\*\***</span></span>

<span data-ttu-id="47f79-112">Puntatore che riceve un puntatore a un enumeratore di metadati.</span><span class="sxs-lookup"><span data-stu-id="47f79-112">A pointer that receives a pointer to a metadata enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f79-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47f79-113">Return value</span></span>

<span data-ttu-id="47f79-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="47f79-114">Type: **HRESULT**</span></span>

<span data-ttu-id="47f79-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="47f79-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="47f79-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="47f79-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="47f79-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="47f79-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="47f79-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47f79-118">Requirements</span></span>



| <span data-ttu-id="47f79-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="47f79-119">Requirement</span></span> | <span data-ttu-id="47f79-120">Valore</span><span class="sxs-lookup"><span data-stu-id="47f79-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f79-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47f79-121">Minimum supported client</span></span><br/> | <span data-ttu-id="47f79-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47f79-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="47f79-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47f79-123">Minimum supported server</span></span><br/> | <span data-ttu-id="47f79-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="47f79-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="47f79-125">DLL</span><span class="sxs-lookup"><span data-stu-id="47f79-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47f79-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47f79-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




