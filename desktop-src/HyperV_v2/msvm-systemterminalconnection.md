---
description: Associa una macchina virtuale a una connessione terminale.
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Classe Msvm_SystemTerminalConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 368c25b8505ec7ddd29da3b95d95fc842602119e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306022"
---
# <a name="msvm_systemterminalconnection-class"></a><span data-ttu-id="67449-103">\_Classe MSVM SystemTerminalConnection</span><span class="sxs-lookup"><span data-stu-id="67449-103">Msvm\_SystemTerminalConnection class</span></span>

<span data-ttu-id="67449-104">Associa una macchina virtuale a una connessione terminale.</span><span class="sxs-lookup"><span data-stu-id="67449-104">Associates a virtual machine with a terminal connection.</span></span>

<span data-ttu-id="67449-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="67449-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67449-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67449-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="67449-107">Members</span><span class="sxs-lookup"><span data-stu-id="67449-107">Members</span></span>

<span data-ttu-id="67449-108">La **classe \_ SystemTerminalConnection di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="67449-108">The **Msvm\_SystemTerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="67449-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="67449-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67449-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="67449-110">Properties</span></span>

<span data-ttu-id="67449-111">La **classe \_ SystemTerminalConnection di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="67449-111">The **Msvm\_SystemTerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67449-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="67449-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67449-113">Tipo di dati: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="67449-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="67449-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="67449-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67449-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="67449-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="67449-116">Macchina virtuale a cui è collegata la connessione.</span><span class="sxs-lookup"><span data-stu-id="67449-116">The virtual machine to which the connection is attached.</span></span>

</dd> <dt>

<span data-ttu-id="67449-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="67449-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67449-118">Tipo di dati: **[ **MSVM \_ TerminalConnection**](msvm-terminalconnection.md)**</span><span class="sxs-lookup"><span data-stu-id="67449-118">Data type: **[**Msvm\_TerminalConnection**](msvm-terminalconnection.md)**</span></span>
</dt> <dt>

<span data-ttu-id="67449-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="67449-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67449-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="67449-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="67449-121">Connessione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67449-121">The connection to the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67449-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="67449-122">Remarks</span></span>

<span data-ttu-id="67449-123">L'accesso alla **classe \_ SystemTerminalConnection di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="67449-123">Access to the **Msvm\_SystemTerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="67449-124">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="67449-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="67449-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67449-125">Requirements</span></span>



| <span data-ttu-id="67449-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="67449-126">Requirement</span></span> | <span data-ttu-id="67449-127">Valore</span><span class="sxs-lookup"><span data-stu-id="67449-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67449-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67449-128">Minimum supported client</span></span><br/> | <span data-ttu-id="67449-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="67449-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="67449-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67449-130">Minimum supported server</span></span><br/> | <span data-ttu-id="67449-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="67449-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67449-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="67449-132">Namespace</span></span><br/>                | <span data-ttu-id="67449-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="67449-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="67449-134">MOF</span><span class="sxs-lookup"><span data-stu-id="67449-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67449-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67449-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67449-136">DLL</span><span class="sxs-lookup"><span data-stu-id="67449-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67449-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67449-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67449-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67449-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67449-139">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="67449-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="67449-140">[**\_HOSTEDDEPENDENCY CIM**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="67449-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="67449-141">Classi video</span><span class="sxs-lookup"><span data-stu-id="67449-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

