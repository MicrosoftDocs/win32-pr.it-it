---
title: Metodo IConnectionBrokerRequest CheckStatus (Cbclient. h)
description: Chiamato per determinare lo stato di una richiesta asincrona.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CheckStatus
- Metodo CheckStatus Servizi Desktop remoto, interfaccia IConnectionBrokerRequest
- Interfaccia IConnectionBrokerRequest Servizi Desktop remoto, metodo CheckStatus
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400884"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a><span data-ttu-id="60ac2-106">Metodo IConnectionBrokerRequest:: CheckStatus</span><span class="sxs-lookup"><span data-stu-id="60ac2-106">IConnectionBrokerRequest::CheckStatus method</span></span>

<span data-ttu-id="60ac2-107">Chiamato per determinare lo stato di una richiesta asincrona.</span><span class="sxs-lookup"><span data-stu-id="60ac2-107">Called to determine the status of an asynchronous request.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ac2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60ac2-108">Syntax</span></span>


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a><span data-ttu-id="60ac2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="60ac2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ac2-110">*pReqStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="60ac2-110">*pReqStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60ac2-111">Indirizzo di una variabile che riceve un valore dell'enumerazione [**\_ \_ dello stato della richiesta CB**](cb-request-status.md) che indica lo stato della richiesta.</span><span class="sxs-lookup"><span data-stu-id="60ac2-111">The address of a variable that receives a value of the [**CB\_REQUEST\_STATUS**](cb-request-status.md) enumeration that indicates the status of the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ac2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60ac2-112">Return value</span></span>

<span data-ttu-id="60ac2-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="60ac2-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="60ac2-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60ac2-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="60ac2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60ac2-115">Requirements</span></span>



| <span data-ttu-id="60ac2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="60ac2-116">Requirement</span></span> | <span data-ttu-id="60ac2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="60ac2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60ac2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60ac2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="60ac2-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="60ac2-119">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="60ac2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60ac2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="60ac2-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60ac2-121">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="60ac2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60ac2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="60ac2-123"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="60ac2-123"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="60ac2-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="60ac2-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="60ac2-125"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60ac2-125"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="60ac2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="60ac2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60ac2-127"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60ac2-127"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60ac2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60ac2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ac2-129">**IConnectionBrokerRequest**</span><span class="sxs-lookup"><span data-stu-id="60ac2-129">**IConnectionBrokerRequest**</span></span>](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





