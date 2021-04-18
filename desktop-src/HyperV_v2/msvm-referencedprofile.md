---
description: Descrive un profilo a cui fa riferimento un altro profilo registrato.
ms.assetid: 36FC0161-C57F-488A-9B4A-C86C6EB481D7
title: Classe Msvm_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencedProfile
- Msvm_ReferencedProfile.Antecedent
- Msvm_ReferencedProfile.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbe95658556be8a15bed0e7e5b5b32dda23ff21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312900"
---
# <a name="msvm_referencedprofile-class"></a><span data-ttu-id="552c6-103">\_Classe MSVM ReferencedProfile</span><span class="sxs-lookup"><span data-stu-id="552c6-103">Msvm\_ReferencedProfile class</span></span>

<span data-ttu-id="552c6-104">Descrive un profilo a cui fa riferimento un altro profilo registrato.</span><span class="sxs-lookup"><span data-stu-id="552c6-104">Describes a profile that is referenced by another registered profile.</span></span>

<span data-ttu-id="552c6-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="552c6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="552c6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="552c6-106">Syntax</span></span>

``` syntax
class Msvm_ReferencedProfile : CIM_ReferencedProfile
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="552c6-107">Members</span><span class="sxs-lookup"><span data-stu-id="552c6-107">Members</span></span>

<span data-ttu-id="552c6-108">La **classe \_ ReferencedProfile di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="552c6-108">The **Msvm\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="552c6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="552c6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="552c6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="552c6-110">Properties</span></span>

<span data-ttu-id="552c6-111">La **classe \_ ReferencedProfile di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="552c6-111">The **Msvm\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="552c6-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="552c6-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="552c6-113">Tipo di dati: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="552c6-113">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="552c6-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="552c6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="552c6-115">Profilo registrato a cui fa riferimento il profilo **dipendente** .</span><span class="sxs-lookup"><span data-stu-id="552c6-115">The registered profile that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="552c6-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="552c6-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="552c6-117">Tipo di dati: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="552c6-117">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="552c6-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="552c6-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="552c6-119">Profilo registrato che fa riferimento ad altri profili.</span><span class="sxs-lookup"><span data-stu-id="552c6-119">A registered profile that references other profiles.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="552c6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="552c6-120">Requirements</span></span>



| <span data-ttu-id="552c6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="552c6-121">Requirement</span></span> | <span data-ttu-id="552c6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="552c6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552c6-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="552c6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="552c6-124">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="552c6-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="552c6-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="552c6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="552c6-126">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="552c6-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="552c6-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="552c6-127">Namespace</span></span><br/>                | <span data-ttu-id="552c6-128">\\Interoperabilità radice</span><span class="sxs-lookup"><span data-stu-id="552c6-128">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="552c6-129">MOF</span><span class="sxs-lookup"><span data-stu-id="552c6-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="552c6-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="552c6-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="552c6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="552c6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="552c6-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="552c6-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

