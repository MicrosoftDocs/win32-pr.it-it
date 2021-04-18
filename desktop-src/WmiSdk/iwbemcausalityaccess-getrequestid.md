---
description: Il metodo GetRequestId restituisce un valore GUID (Globally Unique Identifier) per una richiesta. Un GUID è un numero univoco a 128 bit.
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'Metodo IWbemCausalityAccess:: GetRequestId (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315204"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a><span data-ttu-id="1550a-104">Metodo IWbemCausalityAccess:: GetRequestId</span><span class="sxs-lookup"><span data-stu-id="1550a-104">IWbemCausalityAccess::GetRequestId method</span></span>

<span data-ttu-id="1550a-105">Il metodo **GetRequestiD** restituisce un valore GUID (Globally Unique Identifier) per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="1550a-105">The **GetRequestId** method returns a Globally Unique Identifier (GUID) value for a request.</span></span> <span data-ttu-id="1550a-106">Un GUID è un numero univoco a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="1550a-106">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1550a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1550a-107">Syntax</span></span>


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="1550a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1550a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1550a-109">*PID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1550a-109">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1550a-110">Valore GUID che identifica in modo univoco una richiesta.</span><span class="sxs-lookup"><span data-stu-id="1550a-110">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="1550a-111">Ad esempio, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="1550a-111">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1550a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1550a-112">Return value</span></span>

<span data-ttu-id="1550a-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1550a-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1550a-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1550a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1550a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1550a-115">Requirements</span></span>



| <span data-ttu-id="1550a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1550a-116">Requirement</span></span> | <span data-ttu-id="1550a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1550a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1550a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1550a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1550a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1550a-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1550a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1550a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1550a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1550a-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1550a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1550a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1550a-123"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="1550a-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="1550a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1550a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1550a-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1550a-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1550a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1550a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1550a-127">**IWbemCausalityAccess**</span><span class="sxs-lookup"><span data-stu-id="1550a-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




