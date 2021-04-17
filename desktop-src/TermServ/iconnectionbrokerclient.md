---
title: Interfaccia IConnectionBrokerClient (Cbclient. h)
description: Fornisce i metodi necessari per utilizzare il client di Connessione Desktop remoto broker.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Interfaccia IConnectionBrokerClient Servizi Desktop remoto
- Interfaccia IConnectionBrokerClient Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478892"
---
# <a name="iconnectionbrokerclient-interface"></a><span data-ttu-id="aba7e-105">Interfaccia IConnectionBrokerClient</span><span class="sxs-lookup"><span data-stu-id="aba7e-105">IConnectionBrokerClient interface</span></span>

<span data-ttu-id="aba7e-106">Fornisce i metodi necessari per utilizzare il client di Connessione Desktop remoto broker.</span><span class="sxs-lookup"><span data-stu-id="aba7e-106">Provides the methods needed to use the Remote Desktop Connection Broker client.</span></span>

<span data-ttu-id="aba7e-107">Questa interfaccia viene implementata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="aba7e-107">This interface is implemented by the system.</span></span> <span data-ttu-id="aba7e-108">Per ottenere un'istanza di questa interfaccia, utilizzare la funzione [**CBCreateClientInstance**](cbcreateclientinstance.md) .</span><span class="sxs-lookup"><span data-stu-id="aba7e-108">To obtain an instance of this interface, use the [**CBCreateClientInstance**](cbcreateclientinstance.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="aba7e-109">Membri</span><span class="sxs-lookup"><span data-stu-id="aba7e-109">Members</span></span>

<span data-ttu-id="aba7e-110">L'interfaccia **IConnectionBrokerClient** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aba7e-110">The **IConnectionBrokerClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aba7e-111">**IConnectionBrokerClient** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aba7e-111">**IConnectionBrokerClient** also has these types of members:</span></span>

-   [<span data-ttu-id="aba7e-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="aba7e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aba7e-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="aba7e-113">Methods</span></span>

<span data-ttu-id="aba7e-114">L'interfaccia **IConnectionBrokerClient** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="aba7e-114">The **IConnectionBrokerClient** interface has these methods.</span></span>



| <span data-ttu-id="aba7e-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="aba7e-115">Method</span></span>                                                         | <span data-ttu-id="aba7e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aba7e-116">Description</span></span>                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aba7e-117">**GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="aba7e-117">**GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md) | <span data-ttu-id="aba7e-118">Richiede informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione.</span><span class="sxs-lookup"><span data-stu-id="aba7e-118">Requests information about the target computer where the connection should be redirected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aba7e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aba7e-119">Requirements</span></span>



| <span data-ttu-id="aba7e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aba7e-120">Requirement</span></span> | <span data-ttu-id="aba7e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="aba7e-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba7e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aba7e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aba7e-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aba7e-123">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="aba7e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aba7e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aba7e-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aba7e-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="aba7e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aba7e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="aba7e-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="aba7e-127"><dt>Cbclient.h</dt></span></span> </dl>      |
| <span data-ttu-id="aba7e-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="aba7e-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="aba7e-129"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aba7e-129"><dt>Cbclient.lib</dt></span></span> </dl>    |
| <span data-ttu-id="aba7e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="aba7e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aba7e-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aba7e-131"><dt>Cbclient.dll</dt></span></span> </dl>    |
| <span data-ttu-id="aba7e-132">IID</span><span class="sxs-lookup"><span data-stu-id="aba7e-132">IID</span></span><br/>                      | <span data-ttu-id="aba7e-133">IID \_ IConnectionBrokerClient è definito come D6818DF2-8338-4EB7-AD77-DE210817987C</span><span class="sxs-lookup"><span data-stu-id="aba7e-133">IID\_IConnectionBrokerClient is defined as D6818DF2-8338-4EB7-AD77-DE210817987C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aba7e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aba7e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba7e-135">**CBCreateClientInstance**</span><span class="sxs-lookup"><span data-stu-id="aba7e-135">**CBCreateClientInstance**</span></span>](cbcreateclientinstance.md)
</dt> </dl>

 

