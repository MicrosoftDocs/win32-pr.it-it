---
title: Interfaccia IConnectionBrokerRequest (Cbclient. h)
description: Fornisce i metodi necessari per ottenere i risultati del metodo asincrono IConnectionBrokerClient GetTargetInfo.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Interfaccia IConnectionBrokerRequest Servizi Desktop remoto
- Interfaccia IConnectionBrokerRequest Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743663"
---
# <a name="iconnectionbrokerrequest-interface"></a><span data-ttu-id="c4d83-105">Interfaccia IConnectionBrokerRequest</span><span class="sxs-lookup"><span data-stu-id="c4d83-105">IConnectionBrokerRequest interface</span></span>

<span data-ttu-id="c4d83-106">Fornisce i metodi necessari per ottenere i risultati del metodo asincrono [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c4d83-106">Provides the methods needed to obtain the results of the asynchronous [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

<span data-ttu-id="c4d83-107">Questa interfaccia viene implementata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c4d83-107">This interface is implemented by the system.</span></span> <span data-ttu-id="c4d83-108">Un'istanza di questa interfaccia viene fornita al chiamante con il metodo [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c4d83-108">An instance of this interface is provided to the caller with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="c4d83-109">Membri</span><span class="sxs-lookup"><span data-stu-id="c4d83-109">Members</span></span>

<span data-ttu-id="c4d83-110">L'interfaccia **IConnectionBrokerRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c4d83-110">The **IConnectionBrokerRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c4d83-111">**IConnectionBrokerRequest** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c4d83-111">**IConnectionBrokerRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="c4d83-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="c4d83-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c4d83-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="c4d83-113">Methods</span></span>

<span data-ttu-id="c4d83-114">L'interfaccia **IConnectionBrokerRequest** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c4d83-114">The **IConnectionBrokerRequest** interface has these methods.</span></span>



| <span data-ttu-id="c4d83-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="c4d83-115">Method</span></span>                                                      | <span data-ttu-id="c4d83-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4d83-116">Description</span></span>                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="c4d83-117">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="c4d83-117">**CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md) | <span data-ttu-id="c4d83-118">Chiamato per determinare lo stato di una richiesta asincrona.</span><span class="sxs-lookup"><span data-stu-id="c4d83-118">Called to determine the status of an asynchronous request.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c4d83-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4d83-119">Requirements</span></span>



| <span data-ttu-id="c4d83-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4d83-120">Requirement</span></span> | <span data-ttu-id="c4d83-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c4d83-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d83-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4d83-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c4d83-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c4d83-123">Windows 8</span></span><br/>                                                                        |
| <span data-ttu-id="c4d83-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4d83-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c4d83-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4d83-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c4d83-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4d83-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4d83-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4d83-127"><dt>Cbclient.h</dt></span></span> </dl>       |
| <span data-ttu-id="c4d83-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4d83-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4d83-129"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4d83-129"><dt>Cbclient.lib</dt></span></span> </dl>     |
| <span data-ttu-id="c4d83-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c4d83-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4d83-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4d83-131"><dt>Cbclient.dll</dt></span></span> </dl>     |
| <span data-ttu-id="c4d83-132">IID</span><span class="sxs-lookup"><span data-stu-id="c4d83-132">IID</span></span><br/>                      | <span data-ttu-id="c4d83-133">IID \_ IConnectionBrokerRequest è definito come 25114427-ED5D-46a6-AF53-C62D33A4108E</span><span class="sxs-lookup"><span data-stu-id="c4d83-133">IID\_IConnectionBrokerRequest is defined as 25114427-ED5D-46A6-AF53-C62D33A4108E</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c4d83-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4d83-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d83-135">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="c4d83-135">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

