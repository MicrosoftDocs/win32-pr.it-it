---
description: Fornisce informazioni sulla connettività di rete per una macchina virtuale.
ms.assetid: 59503c1b-203b-46ec-8a65-f21a746f170f
title: Classe Msvm_NetworkConnectionDiagnosticInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticInformation
- Msvm_NetworkConnectionDiagnosticInformation.RoundTripTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 416392702e5bc06e54fe5a23b6784b87e98b7027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968466"
---
# <a name="msvm_networkconnectiondiagnosticinformation-class"></a><span data-ttu-id="fd7e2-103">\_Classe MSVM NetworkConnectionDiagnosticInformation</span><span class="sxs-lookup"><span data-stu-id="fd7e2-103">Msvm\_NetworkConnectionDiagnosticInformation class</span></span>

<span data-ttu-id="fd7e2-104">Fornisce informazioni sulla connettività di rete per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-104">Provides information about the network connectivity for a virtual machine.</span></span>

<span data-ttu-id="fd7e2-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7e2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd7e2-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticInformation
{
  uint32 RoundTripTime;
};
```

## <a name="members"></a><span data-ttu-id="fd7e2-107">Members</span><span class="sxs-lookup"><span data-stu-id="fd7e2-107">Members</span></span>

<span data-ttu-id="fd7e2-108">La **classe \_ NetworkConnectionDiagnosticInformation di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fd7e2-108">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="fd7e2-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd7e2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd7e2-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd7e2-110">Properties</span></span>

<span data-ttu-id="fd7e2-111">La **classe \_ NetworkConnectionDiagnosticInformation di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-111">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd7e2-112">**RoundTripTime**</span><span class="sxs-lookup"><span data-stu-id="fd7e2-112">**RoundTripTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd7e2-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd7e2-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd7e2-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd7e2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd7e2-115">Round trip tempo per la richiesta di ping.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-115">The round trip time for the ping request.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd7e2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd7e2-116">Requirements</span></span>



| <span data-ttu-id="fd7e2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd7e2-117">Requirement</span></span> | <span data-ttu-id="fd7e2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7e2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7e2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd7e2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7e2-120">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd7e2-120">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fd7e2-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd7e2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7e2-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fd7e2-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fd7e2-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fd7e2-123">Namespace</span></span><br/>                | <span data-ttu-id="fd7e2-124">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fd7e2-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fd7e2-125">MOF</span><span class="sxs-lookup"><span data-stu-id="fd7e2-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd7e2-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd7e2-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd7e2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fd7e2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd7e2-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fd7e2-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




