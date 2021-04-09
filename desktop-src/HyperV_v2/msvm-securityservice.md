---
description: Rappresenta il servizio di sicurezza. Viene usato per configurare le impostazioni di sicurezza del sistema virtuale.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967629"
---
# <a name="msvm_securityservice-class"></a><span data-ttu-id="c0e37-104">\_Classe MSVM SecurityService</span><span class="sxs-lookup"><span data-stu-id="c0e37-104">Msvm\_SecurityService class</span></span>

<span data-ttu-id="c0e37-105">Rappresenta il servizio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c0e37-105">Represents the security service.</span></span> <span data-ttu-id="c0e37-106">Viene usato per configurare le impostazioni di sicurezza del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0e37-106">It is used for configuring virtual system security settings.</span></span>

<span data-ttu-id="c0e37-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c0e37-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e37-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0e37-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="c0e37-109">Members</span><span class="sxs-lookup"><span data-stu-id="c0e37-109">Members</span></span>

<span data-ttu-id="c0e37-110">La **classe \_ SecurityService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c0e37-110">The **Msvm\_SecurityService** class has these types of members:</span></span>

-   [<span data-ttu-id="c0e37-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0e37-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0e37-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0e37-112">Methods</span></span>

<span data-ttu-id="c0e37-113">La **classe \_ SecurityService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c0e37-113">The **Msvm\_SecurityService** class has these methods.</span></span>



| <span data-ttu-id="c0e37-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="c0e37-114">Method</span></span>                                                                                            | <span data-ttu-id="c0e37-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0e37-115">Description</span></span>                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="c0e37-116">**GetKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="c0e37-116">**GetKeyProtector**</span></span>](msvm-securityservice-getkeyprotector.md)                                   | <span data-ttu-id="c0e37-117">Metodo per recuperare la protezione con chiave per un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0e37-117">Method to retrieve the key protector for a virtual system.</span></span><br/>   |
| [<span data-ttu-id="c0e37-118">**ModifySecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="c0e37-118">**ModifySecuritySettings**</span></span>](msvm-securityservice-modifysecuritysettings.md)                     | <span data-ttu-id="c0e37-119">Modifica le impostazioni di sicurezza correnti di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0e37-119">Modifies the current security settings of a virtual machine.</span></span><br/> |
| [<span data-ttu-id="c0e37-120">**RestoreLastKnownGoodKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="c0e37-120">**RestoreLastKnownGoodKeyProtector**</span></span>](msvm-securityservice-restorelastknowngoodkeyprotector.md) | <span data-ttu-id="c0e37-121">Metodo di ripristino all'ultima protezione con chiave corretta nota.</span><span class="sxs-lookup"><span data-stu-id="c0e37-121">Method to restore back to the last known good key protector.</span></span><br/> |
| [<span data-ttu-id="c0e37-122">**SetKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="c0e37-122">**SetKeyProtector**</span></span>](msvm-securityservice-setkeyprotector.md)                                   | <span data-ttu-id="c0e37-123">Metodo per impostare la protezione con chiave per un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0e37-123">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="c0e37-124">**SetSecurityPolicy**</span><span class="sxs-lookup"><span data-stu-id="c0e37-124">**SetSecurityPolicy**</span></span>](msvm-securityservice-setsecuritypolicy.md)                               | <span data-ttu-id="c0e37-125">Metodo per impostare la protezione con chiave per un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0e37-125">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="c0e37-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="c0e37-126">**StartService**</span></span>](msvm-securityservice-startservice.md)                                         | <span data-ttu-id="c0e37-127">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="c0e37-127">Starts the service.</span></span><br/>                                          |
| [<span data-ttu-id="c0e37-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="c0e37-128">**StopService**</span></span>](msvm-securityservice-stopservice.md)                                           | <span data-ttu-id="c0e37-129">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="c0e37-129">Stops the service.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="c0e37-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0e37-130">Requirements</span></span>



| <span data-ttu-id="c0e37-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0e37-131">Requirement</span></span> | <span data-ttu-id="c0e37-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c0e37-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e37-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0e37-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c0e37-134">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0e37-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c0e37-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0e37-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c0e37-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c0e37-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c0e37-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c0e37-137">Namespace</span></span><br/>                | <span data-ttu-id="c0e37-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c0e37-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c0e37-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c0e37-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0e37-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0e37-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0e37-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c0e37-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0e37-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0e37-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c0e37-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0e37-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0e37-144">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="c0e37-144">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




