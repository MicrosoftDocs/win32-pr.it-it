---
description: Connette un servizio di bridging trasparente a una voce di avanzamento dinamico (indirizzo MAC appreso).
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Classe Msvm_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 01b9d9c752d4781864c07ff24fca5f866a57ae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966938"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="6390b-103">\_Classe MSVM TransparentBridgingDynamicForwarding</span><span class="sxs-lookup"><span data-stu-id="6390b-103">Msvm\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="6390b-104">Connette un servizio di bridging trasparente a una voce di avanzamento dinamico (indirizzo MAC appreso).</span><span class="sxs-lookup"><span data-stu-id="6390b-104">Connects a transparent bridging service to a dynamic forward entry (learned MAC address).</span></span>

<span data-ttu-id="6390b-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6390b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6390b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6390b-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6390b-107">Members</span><span class="sxs-lookup"><span data-stu-id="6390b-107">Members</span></span>

<span data-ttu-id="6390b-108">La **classe \_ TransparentBridgingDynamicForwarding di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6390b-108">The **Msvm\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="6390b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6390b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6390b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6390b-110">Properties</span></span>

<span data-ttu-id="6390b-111">La **classe \_ TransparentBridgingDynamicForwarding di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6390b-111">The **Msvm\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6390b-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="6390b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6390b-113">Tipo di dati: **[ **MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span><span class="sxs-lookup"><span data-stu-id="6390b-113">Data type: **[**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6390b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6390b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6390b-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="6390b-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6390b-116">Riferimento a un'istanza della classe [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) che rappresenta il servizio bridging trasparente.</span><span class="sxs-lookup"><span data-stu-id="6390b-116">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="6390b-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="6390b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6390b-118">Tipo di dati: **[ **MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="6390b-118">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6390b-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6390b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6390b-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="6390b-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6390b-121">Riferimento a un'istanza della classe [**\_ DynamicForwardingEntry MSVM**](msvm-dynamicforwardingentry.md) che rappresenta la voce di avanzamento dinamico del database di inoltri.</span><span class="sxs-lookup"><span data-stu-id="6390b-121">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6390b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="6390b-122">Remarks</span></span>

<span data-ttu-id="6390b-123">L'accesso alla **classe \_ TransparentBridgingDynamicForwarding di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="6390b-123">Access to the **Msvm\_TransparentBridgingDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6390b-124">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6390b-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6390b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6390b-125">Requirements</span></span>



| <span data-ttu-id="6390b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6390b-126">Requirement</span></span> | <span data-ttu-id="6390b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6390b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6390b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6390b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6390b-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6390b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6390b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6390b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6390b-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6390b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6390b-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6390b-132">Namespace</span></span><br/>                | <span data-ttu-id="6390b-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6390b-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6390b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6390b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6390b-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6390b-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6390b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6390b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6390b-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6390b-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6390b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6390b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6390b-139">**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="6390b-139">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[<span data-ttu-id="6390b-140">**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="6390b-140">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

