---
description: Inserisce il servizio nello stato avviato.
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: Metodo StartService della classe CIM_Service (gestione di Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 73b89f7fc789639fb45acbde61da4c7962650177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307767"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="9b127-103">Metodo StartService della classe CIM_Service (gestione di Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="9b127-103">StartService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="9b127-104">Inserisce il servizio nello stato avviato.</span><span class="sxs-lookup"><span data-stu-id="9b127-104">Places the service in the started state.</span></span>

> [!Note]
>
> <span data-ttu-id="9b127-105">La semantica di questo metodo si sovrappone al metodo **RequestStateChange** ereditato da [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b127-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="9b127-106">Questo metodo viene mantenuto perché è stato ampiamente implementato e la semplice semantica di "avvio" è comoda da usare.</span><span class="sxs-lookup"><span data-stu-id="9b127-106">This method is maintained because it has been widely implemented, and its simple "start" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9b127-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b127-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="9b127-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b127-108">Parameters</span></span>

<span data-ttu-id="9b127-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9b127-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b127-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b127-110">Return value</span></span>

<span data-ttu-id="9b127-111">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9b127-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b127-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b127-112">Requirements</span></span>



| <span data-ttu-id="9b127-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b127-113">Requirement</span></span> | <span data-ttu-id="9b127-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9b127-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b127-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b127-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9b127-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9b127-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9b127-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b127-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9b127-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9b127-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9b127-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9b127-119">Namespace</span></span><br/>                | <span data-ttu-id="9b127-120">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9b127-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9b127-121">MOF</span><span class="sxs-lookup"><span data-stu-id="9b127-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b127-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b127-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b127-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9b127-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b127-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b127-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9b127-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b127-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b127-126">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="9b127-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




