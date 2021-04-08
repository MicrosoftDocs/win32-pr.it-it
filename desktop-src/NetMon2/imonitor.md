---
description: L'interfaccia IMonitor fornisce metodi che controllano l'operazione di monitoraggio. Questi metodi vengono chiamati dal servizio di controllo di monitoraggio (MCSVC).
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Interfaccia IMonitor (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879914"
---
# <a name="imonitor-interface"></a><span data-ttu-id="f33ec-104">Interfaccia IMonitor</span><span class="sxs-lookup"><span data-stu-id="f33ec-104">IMonitor interface</span></span>

<span data-ttu-id="f33ec-105">L'interfaccia **Imonitor** fornisce metodi che controllano l'operazione di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="f33ec-105">The **IMonitor** interface provides methods that control monitor operation.</span></span> <span data-ttu-id="f33ec-106">Questi metodi vengono chiamati dal [*servizio di controllo di monitoraggio*](m.md) (MCSVC).</span><span class="sxs-lookup"><span data-stu-id="f33ec-106">These methods are called by the [*Monitor Control Service*](m.md) (MCSVC).</span></span>

## <a name="members"></a><span data-ttu-id="f33ec-107">Membri</span><span class="sxs-lookup"><span data-stu-id="f33ec-107">Members</span></span>

<span data-ttu-id="f33ec-108">L'interfaccia **Imonitor** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f33ec-108">The **IMonitor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f33ec-109">**Imonitor** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f33ec-109">**IMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="f33ec-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="f33ec-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f33ec-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="f33ec-111">Methods</span></span>

<span data-ttu-id="f33ec-112">L'interfaccia **Imonitor** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f33ec-112">The **IMonitor** interface has these methods.</span></span>



| <span data-ttu-id="f33ec-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="f33ec-113">Method</span></span>                                        | <span data-ttu-id="f33ec-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33ec-114">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f33ec-115">**DoConfigure**</span><span class="sxs-lookup"><span data-stu-id="f33ec-115">**DoConfigure**</span></span>](imonitor-doconfigure.md)   | <span data-ttu-id="f33ec-116">Configurazione di monitoraggio aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="f33ec-116">Updates monitor configuration.</span></span><br/>                                                                           |
| [<span data-ttu-id="f33ec-117">**DoInitialize**</span><span class="sxs-lookup"><span data-stu-id="f33ec-117">**DoInitialize**</span></span>](imonitor-doinitialize.md) | <span data-ttu-id="f33ec-118">Inizializza un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="f33ec-118">Initializes a monitor.</span></span><br/>                                                                                   |
| [<span data-ttu-id="f33ec-119">**Onframe**</span><span class="sxs-lookup"><span data-stu-id="f33ec-119">**OnFrames**</span></span>](imonitor-onframes.md)         | <span data-ttu-id="f33ec-120">Indica lo stato di un evento frame.</span><span class="sxs-lookup"><span data-stu-id="f33ec-120">Indicates the status of a frame event.</span></span><br/>                                                                   |
| [<span data-ttu-id="f33ec-121">**OnStart**</span><span class="sxs-lookup"><span data-stu-id="f33ec-121">**OnStart**</span></span>](imonitor-onstart.md)           | <span data-ttu-id="f33ec-122">Indica che il monitoraggio è stato configurato correttamente e che l'acquisizione dei dati sta per iniziare.</span><span class="sxs-lookup"><span data-stu-id="f33ec-122">Indicates that the monitor has been configured successfully and that the data capture is about to begin.</span></span><br/> |
| [<span data-ttu-id="f33ec-123">**OnStatus**</span><span class="sxs-lookup"><span data-stu-id="f33ec-123">**OnStatus**</span></span>](imonitor-onstatus.md)         | <span data-ttu-id="f33ec-124">Indica un evento di stato NPP.</span><span class="sxs-lookup"><span data-stu-id="f33ec-124">Indicates an NPP status event.</span></span><br/>                                                                           |
| [<span data-ttu-id="f33ec-125">**OnStop**</span><span class="sxs-lookup"><span data-stu-id="f33ec-125">**OnStop**</span></span>](imonitor-onstop.md)             | <span data-ttu-id="f33ec-126">Indica il completamento dell'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="f33ec-126">Indicates data capture completion.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="f33ec-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f33ec-127">Requirements</span></span>



| <span data-ttu-id="f33ec-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f33ec-128">Requirement</span></span> | <span data-ttu-id="f33ec-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f33ec-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f33ec-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f33ec-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f33ec-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f33ec-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f33ec-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f33ec-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f33ec-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f33ec-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f33ec-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f33ec-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f33ec-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f33ec-135"><dt>Netmon.h</dt></span></span> </dl> |



 

