---
description: Rappresenta una voce di controllo di accesso (ACE) che determina l'accesso alla sessione interattiva di una macchina virtuale.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Classe Msvm_InteractiveSessionACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307883"
---
# <a name="msvm_interactivesessionace-class"></a><span data-ttu-id="260e6-103">\_Classe MSVM InteractiveSessionACE</span><span class="sxs-lookup"><span data-stu-id="260e6-103">Msvm\_InteractiveSessionACE class</span></span>

<span data-ttu-id="260e6-104">Rappresenta una *voce di controllo di accesso* (ACE) che determina l'accesso alla sessione interattiva di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="260e6-104">Represents an *access control entry* (ACE) that determines access to the interactive session of a virtual machine.</span></span>

<span data-ttu-id="260e6-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="260e6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="260e6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="260e6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a><span data-ttu-id="260e6-107">Members</span><span class="sxs-lookup"><span data-stu-id="260e6-107">Members</span></span>

<span data-ttu-id="260e6-108">La **classe \_ InteractiveSessionACE di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="260e6-108">The **Msvm\_InteractiveSessionACE** class has these types of members:</span></span>

-   [<span data-ttu-id="260e6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="260e6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="260e6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="260e6-110">Properties</span></span>

<span data-ttu-id="260e6-111">La **classe \_ InteractiveSessionACE di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="260e6-111">The **Msvm\_InteractiveSessionACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="260e6-112">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="260e6-112">**AccessType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="260e6-113">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="260e6-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="260e6-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="260e6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="260e6-115">Indica se la voce ACE concede o nega l'accesso al trustee.</span><span class="sxs-lookup"><span data-stu-id="260e6-115">Indicates whether the ACE grants or denies access to the trustee.</span></span>

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

<span data-ttu-id="260e6-116">**Accesso consentito** (0)</span><span class="sxs-lookup"><span data-stu-id="260e6-116">**Access Allowed** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

<span data-ttu-id="260e6-117">**Accesso negato** (1)</span><span class="sxs-lookup"><span data-stu-id="260e6-117">**Access Denied** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="260e6-118">**Fiduciario**</span><span class="sxs-lookup"><span data-stu-id="260e6-118">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="260e6-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="260e6-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="260e6-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="260e6-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="260e6-121">Identifica l'entità di sicurezza a cui l'ACE concede o nega l'accesso.</span><span class="sxs-lookup"><span data-stu-id="260e6-121">Identifies the security principal that the ACE grants or denies access to.</span></span> <span data-ttu-id="260e6-122">I formati validi per questa proprietà includono il formato del nome utente compatibile con SAM di Windows e il formato stringa SID di Windows.</span><span class="sxs-lookup"><span data-stu-id="260e6-122">Valid formats for this property include the Windows SAM-compatible user name format and the Windows SID string format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="260e6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="260e6-123">Requirements</span></span>



| <span data-ttu-id="260e6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="260e6-124">Requirement</span></span> | <span data-ttu-id="260e6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="260e6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="260e6-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="260e6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="260e6-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="260e6-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="260e6-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="260e6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="260e6-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="260e6-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="260e6-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="260e6-130">Namespace</span></span><br/>                | <span data-ttu-id="260e6-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="260e6-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="260e6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="260e6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="260e6-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="260e6-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="260e6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="260e6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="260e6-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="260e6-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="260e6-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="260e6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="260e6-137">**GetInteractiveSessionACL**</span><span class="sxs-lookup"><span data-stu-id="260e6-137">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




