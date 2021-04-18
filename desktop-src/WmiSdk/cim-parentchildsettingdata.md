---
description: Un'associazione tra un'istanza di CIM \_ VirtualSystemSettingData e l' \_ istanza CIM VirtualSystemSettingData che rappresenta lo snapshot più recente su cui si basa questo oggetto.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: Classe CIM_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329649"
---
# <a name="cim_parentchildsettingdata-class"></a><span data-ttu-id="680c6-103">CIM \_ ParentChildSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="680c6-103">CIM\_ParentChildSettingData class</span></span>

<span data-ttu-id="680c6-104">Un'associazione tra un'istanza di [**CIM \_ VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) e l'istanza **CIM \_ VirtualSystemSettingData** che rappresenta lo snapshot più recente su cui si basa questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="680c6-104">An association between an instance of [**CIM\_VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) and the **CIM\_VirtualSystemSettingData** instance which represents the most recent snapshot upon which this object is based.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="680c6-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="680c6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="680c6-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="680c6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="680c6-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="680c6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="680c6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="680c6-108">Syntax</span></span>

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a><span data-ttu-id="680c6-109">Members</span><span class="sxs-lookup"><span data-stu-id="680c6-109">Members</span></span>

<span data-ttu-id="680c6-110">La classe **CIM \_ ParentChildSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="680c6-110">The **CIM\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="680c6-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="680c6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="680c6-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="680c6-112">Properties</span></span>

<span data-ttu-id="680c6-113">La classe **CIM \_ ParentChildSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="680c6-113">The **CIM\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="680c6-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="680c6-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680c6-115">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="680c6-115">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="680c6-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="680c6-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="680c6-117">Riferimento all'oggetto indipendente in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="680c6-117">Reference to the independent object in this association.</span></span>

<span data-ttu-id="680c6-118">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="680c6-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="680c6-119">**Figlio**</span><span class="sxs-lookup"><span data-stu-id="680c6-119">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680c6-120">Tipo di dati: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="680c6-120">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="680c6-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="680c6-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="680c6-122">Dati di impostazione per il sistema virtuale che rappresenta l'elemento figlio dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="680c6-122">The setting data for the virtual system which represents the child of the Parent.</span></span>

</dd> <dt>

<span data-ttu-id="680c6-123">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="680c6-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680c6-124">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="680c6-124">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="680c6-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="680c6-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="680c6-126">Riferimento all'oggetto che dipende dalla proprietà **precedente** .</span><span class="sxs-lookup"><span data-stu-id="680c6-126">Reference to the object that is dependent on the **Antecedent** property.</span></span>

<span data-ttu-id="680c6-127">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="680c6-127">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="680c6-128">**Parent**</span><span class="sxs-lookup"><span data-stu-id="680c6-128">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680c6-129">Tipo di dati: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="680c6-129">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="680c6-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="680c6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="680c6-131">I dati di impostazione dello snapshot su cui si basano i dati delle impostazioni figlio.</span><span class="sxs-lookup"><span data-stu-id="680c6-131">The snapshot setting data upon which the Child setting data is based.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="680c6-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="680c6-132">Requirements</span></span>



| <span data-ttu-id="680c6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="680c6-133">Requirement</span></span> | <span data-ttu-id="680c6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="680c6-134">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="680c6-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="680c6-135">Namespace</span></span><br/> | <span data-ttu-id="680c6-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="680c6-136">Root\\CIMV2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="680c6-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="680c6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="680c6-138">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="680c6-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

