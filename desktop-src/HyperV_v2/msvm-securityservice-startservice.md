---
description: avvia il servizio.
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Metodo StartService della classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bff2721b942b6bb145f2d57492f27d1cabb722bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320004"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="50338-103">Metodo StartService della classe MSVM \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="50338-103">StartService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="50338-104">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="50338-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="50338-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50338-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="50338-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="50338-106">Parameters</span></span>

<span data-ttu-id="50338-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="50338-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50338-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50338-108">Return value</span></span>

<span data-ttu-id="50338-109">In caso di esito positivo, restituisce 0. in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="50338-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="50338-110">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="50338-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="50338-111">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="50338-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="50338-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50338-112">Requirements</span></span>



| <span data-ttu-id="50338-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="50338-113">Requirement</span></span> | <span data-ttu-id="50338-114">Valore</span><span class="sxs-lookup"><span data-stu-id="50338-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50338-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50338-115">Minimum supported client</span></span><br/> | <span data-ttu-id="50338-116">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="50338-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="50338-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50338-117">Minimum supported server</span></span><br/> | <span data-ttu-id="50338-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="50338-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="50338-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="50338-119">Namespace</span></span><br/>                | <span data-ttu-id="50338-120">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="50338-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="50338-121">MOF</span><span class="sxs-lookup"><span data-stu-id="50338-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50338-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50338-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50338-123">DLL</span><span class="sxs-lookup"><span data-stu-id="50338-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50338-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50338-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50338-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50338-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50338-126">**\_SecurityService MSVM**</span><span class="sxs-lookup"><span data-stu-id="50338-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




