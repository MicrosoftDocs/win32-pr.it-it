---
description: arresta il servizio.
ms.assetid: cf100cea-b0e1-42e9-831e-6422aded47c5
title: Metodo StopService della classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 68e88e2c88d4f75f4d7671c389bab0cd81d0deb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232273"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="37057-103">Metodo StopService della classe MSVM \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="37057-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="37057-104">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="37057-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="37057-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37057-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="37057-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37057-106">Parameters</span></span>

<span data-ttu-id="37057-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="37057-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37057-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37057-108">Return value</span></span>

<span data-ttu-id="37057-109">In caso di esito positivo, restituisce 0. in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="37057-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="37057-110">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="37057-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="37057-111">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="37057-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="37057-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37057-112">Requirements</span></span>



| <span data-ttu-id="37057-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="37057-113">Requirement</span></span> | <span data-ttu-id="37057-114">Valore</span><span class="sxs-lookup"><span data-stu-id="37057-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37057-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37057-115">Minimum supported client</span></span><br/> | <span data-ttu-id="37057-116">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="37057-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="37057-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37057-117">Minimum supported server</span></span><br/> | <span data-ttu-id="37057-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="37057-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="37057-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="37057-119">Namespace</span></span><br/>                | <span data-ttu-id="37057-120">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="37057-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37057-121">MOF</span><span class="sxs-lookup"><span data-stu-id="37057-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37057-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37057-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37057-123">DLL</span><span class="sxs-lookup"><span data-stu-id="37057-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37057-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37057-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37057-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37057-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37057-126">**\_SecurityService MSVM**</span><span class="sxs-lookup"><span data-stu-id="37057-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




