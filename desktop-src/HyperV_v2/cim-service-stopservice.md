---
description: Accelera il servizio nello stato interrotto.
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: Metodo StopService della classe CIM_Service (gestione di Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4eb354a48b074bad8adac4d5635e204844c31b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879506"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="6a4a4-103">Metodo StopService della classe CIM_Service (gestione di Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="6a4a4-103">StopService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="6a4a4-104">Accelera il servizio nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="6a4a4-104">Paces the service in the stopped state.</span></span>

> [!Note]
>
> <span data-ttu-id="6a4a4-105">La semantica di questo metodo si sovrappone al metodo **RequestStateChange** ereditato da [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6a4a4-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="6a4a4-106">Questo metodo viene mantenuto perché è stato ampiamente implementato e la semplice semantica di "arresto" è comoda da usare.</span><span class="sxs-lookup"><span data-stu-id="6a4a4-106">This method is maintained because it has been widely implemented, and its simple "stop" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6a4a4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a4a4-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="6a4a4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a4a4-108">Parameters</span></span>

<span data-ttu-id="6a4a4-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6a4a4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a4a4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a4a4-110">Return value</span></span>

<span data-ttu-id="6a4a4-111">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="6a4a4-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a4a4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a4a4-112">Requirements</span></span>



| <span data-ttu-id="6a4a4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a4a4-113">Requirement</span></span> | <span data-ttu-id="6a4a4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6a4a4-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4a4-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a4a4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6a4a4-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6a4a4-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6a4a4-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a4a4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6a4a4-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6a4a4-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6a4a4-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a4a4-119">Namespace</span></span><br/>                | <span data-ttu-id="6a4a4-120">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6a4a4-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6a4a4-121">MOF</span><span class="sxs-lookup"><span data-stu-id="6a4a4-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a4a4-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a4a4-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a4a4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6a4a4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a4a4-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a4a4-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6a4a4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a4a4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a4a4-126">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="6a4a4-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




