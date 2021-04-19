---
description: Rappresenta l'associazione tra gli elementi gestiti e le relative funzionalità.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Classe Msvm_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314329"
---
# <a name="msvm_elementcapabilities-class"></a><span data-ttu-id="f455b-103">\_Classe MSVM ElementCapabilities</span><span class="sxs-lookup"><span data-stu-id="f455b-103">Msvm\_ElementCapabilities class</span></span>

<span data-ttu-id="f455b-104">Rappresenta l'associazione tra gli elementi gestiti e le relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f455b-104">Represents the association between managed elements and their capabilities.</span></span>

<span data-ttu-id="f455b-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f455b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f455b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f455b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="f455b-107">Members</span><span class="sxs-lookup"><span data-stu-id="f455b-107">Members</span></span>

<span data-ttu-id="f455b-108">La **classe \_ ElementCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f455b-108">The **Msvm\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="f455b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f455b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f455b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f455b-110">Properties</span></span>

<span data-ttu-id="f455b-111">La **classe \_ ElementCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f455b-111">The **Msvm\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f455b-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="f455b-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f455b-113">Tipo di dati: **[ **\_ funzionalità CIM**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="f455b-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="f455b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f455b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f455b-115">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="f455b-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f455b-116">Oggetto funzionalità associato all'elemento.</span><span class="sxs-lookup"><span data-stu-id="f455b-116">The capabilities object associated with the element.</span></span> <span data-ttu-id="f455b-117">Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="f455b-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="f455b-118">**Caratteristiche**</span><span class="sxs-lookup"><span data-stu-id="f455b-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f455b-119">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f455b-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f455b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f455b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f455b-121">Fornisce informazioni descrittive sulle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f455b-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="f455b-122">Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="f455b-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="f455b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f455b-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="f455b-124">Significato</span><span class="sxs-lookup"><span data-stu-id="f455b-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="f455b-125"><dt>**Impostazione predefinita**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f455b-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="f455b-126">Le funzionalità associate rappresentano le funzionalità predefinite dell'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="f455b-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="f455b-127"><dt>**Corrente**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f455b-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="f455b-128">Le funzionalità associate rappresentano le funzionalità correnti dell'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="f455b-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f455b-129">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="f455b-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f455b-130">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="f455b-130">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="f455b-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f455b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f455b-132">Qualificatori: **chiave**, **min** (1)</span><span class="sxs-lookup"><span data-stu-id="f455b-132">Qualifiers: **Key**, **Min** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="f455b-133">Elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="f455b-133">The managed element.</span></span> <span data-ttu-id="f455b-134">Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="f455b-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f455b-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="f455b-135">Remarks</span></span>

<span data-ttu-id="f455b-136">L'accesso alla **classe \_ ElementCapabilities di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="f455b-136">Access to the **Msvm\_ElementCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f455b-137">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f455b-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f455b-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f455b-138">Requirements</span></span>



| <span data-ttu-id="f455b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f455b-139">Requirement</span></span> | <span data-ttu-id="f455b-140">Valore</span><span class="sxs-lookup"><span data-stu-id="f455b-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f455b-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f455b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f455b-142">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f455b-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f455b-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f455b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f455b-144">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f455b-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f455b-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f455b-145">Namespace</span></span><br/>                | <span data-ttu-id="f455b-146">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f455b-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f455b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="f455b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f455b-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f455b-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f455b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f455b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f455b-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f455b-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f455b-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f455b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f455b-152">**\_ELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="f455b-152">**CIM\_ElementCapabilities**</span></span>](cim-elementcapabilities.md)
</dt> <dt>

[<span data-ttu-id="f455b-153">**\_ELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="f455b-153">**CIM\_ElementCapabilities**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[<span data-ttu-id="f455b-154">**MSVM \_ ElementCapabilities (V1)**</span><span class="sxs-lookup"><span data-stu-id="f455b-154">**Msvm\_ElementCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

