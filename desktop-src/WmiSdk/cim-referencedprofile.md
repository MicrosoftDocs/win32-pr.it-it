---
description: Utilizzato per associare un'istanza CIM \_ RegisteredProfile a un'istanza di CIM \_ RegisteredProfile di un altro profilo che fa riferimento al profilo dipendente come profilo correlato.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: Classe CIM_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316573"
---
# <a name="cim_referencedprofile-class"></a><span data-ttu-id="27022-103">CIM \_ ReferencedProfile (classe)</span><span class="sxs-lookup"><span data-stu-id="27022-103">CIM\_ReferencedProfile class</span></span>

<span data-ttu-id="27022-104">Utilizzato per associare un'istanza [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) a un'istanza di **CIM \_ RegisteredProfile** di un altro profilo che fa riferimento al profilo dipendente come profilo correlato.</span><span class="sxs-lookup"><span data-stu-id="27022-104">Used to associate an instance [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) with an instance of **CIM\_RegisteredProfile** of another profile that references the dependent profile as a related profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27022-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="27022-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="27022-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="27022-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="27022-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="27022-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="27022-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27022-108">Syntax</span></span>

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="27022-109">Members</span><span class="sxs-lookup"><span data-stu-id="27022-109">Members</span></span>

<span data-ttu-id="27022-110">La classe **CIM \_ ReferencedProfile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="27022-110">The **CIM\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="27022-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="27022-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27022-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="27022-112">Properties</span></span>

<span data-ttu-id="27022-113">La classe **CIM \_ ReferencedProfile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="27022-113">The **CIM\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27022-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="27022-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27022-115">Tipo di dati: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="27022-115">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="27022-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="27022-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27022-117">Specifica l'istanza [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) a cui fa riferimento il profilo **dipendente** .</span><span class="sxs-lookup"><span data-stu-id="27022-117">Specifies the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="27022-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="27022-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27022-119">Tipo di dati: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="27022-119">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="27022-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="27022-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27022-121">Specifica un'istanza [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) che fa riferimento ad altri profili.</span><span class="sxs-lookup"><span data-stu-id="27022-121">Specifies a [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that references other profiles.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27022-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="27022-122">Remarks</span></span>

<span data-ttu-id="27022-123">L'uso delle proprietà **dipendenti** e **precedenti** nell'associazione **CIM \_ ReferencedProfile** è definito in modo che il profilo a cui viene fatto riferimento sia l'attività precedente e che il profilo che esegue il riferimento sia il dipendente.</span><span class="sxs-lookup"><span data-stu-id="27022-123">The use of the **Dependent** and **Antecedent** properties in the **CIM\_ReferencedProfile** association is defined such that the profile being referenced is the antecedent and the profile doing the referencing is the dependent.</span></span>

<span data-ttu-id="27022-124">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="27022-124">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="27022-125">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="27022-125">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="27022-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27022-126">Requirements</span></span>



| <span data-ttu-id="27022-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="27022-127">Requirement</span></span> | <span data-ttu-id="27022-128">Valore</span><span class="sxs-lookup"><span data-stu-id="27022-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27022-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27022-129">Minimum supported client</span></span><br/> | <span data-ttu-id="27022-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27022-130">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="27022-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27022-131">Minimum supported server</span></span><br/> | <span data-ttu-id="27022-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27022-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="27022-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="27022-133">Namespace</span></span><br/>                | <span data-ttu-id="27022-134">\\Interoperabilità radice</span><span class="sxs-lookup"><span data-stu-id="27022-134">Root\\interop</span></span><br/>                                                               |
| <span data-ttu-id="27022-135">MOF</span><span class="sxs-lookup"><span data-stu-id="27022-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27022-136"><dt>Interop. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27022-136"><dt>Interop.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27022-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27022-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27022-138">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="27022-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

