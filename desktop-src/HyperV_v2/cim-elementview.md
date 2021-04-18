---
description: Rappresenta un'associazione tra una vista e un'istanza di che rappresenta la visualizzazione normalizzata di una risorsa gestita.
ms.assetid: 9c6eb3d5-7366-4954-9e64-12f889c64114
title: Classe CIM_ElementView
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementView
- CIM_ElementView.Antecedent
- CIM_ElementView.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ffc0e4b69667800b1880cae1a992a207cc95a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312931"
---
# <a name="cim_elementview-class"></a><span data-ttu-id="01456-103">CIM \_ ElementView (classe)</span><span class="sxs-lookup"><span data-stu-id="01456-103">CIM\_ElementView class</span></span>

<span data-ttu-id="01456-104">Rappresenta un'associazione tra una vista e un'istanza di che rappresenta la visualizzazione normalizzata di una risorsa gestita.</span><span class="sxs-lookup"><span data-stu-id="01456-104">Represents and association between a view, and an instance that represents the normalized view of a managed resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="01456-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01456-105">Syntax</span></span>

``` syntax
[Abstract, Association, Experimental, Version("2.21.1"), UMLPackagePath("CIM::Core::CoreElements")]
class CIM_ElementView : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_View           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="01456-106">Members</span><span class="sxs-lookup"><span data-stu-id="01456-106">Members</span></span>

<span data-ttu-id="01456-107">La classe **CIM \_ ElementView** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="01456-107">The **CIM\_ElementView** class has these types of members:</span></span>

-   [<span data-ttu-id="01456-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="01456-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01456-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="01456-109">Properties</span></span>

<span data-ttu-id="01456-110">La classe **CIM \_ ElementView** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="01456-110">The **CIM\_ElementView** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01456-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="01456-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01456-112">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="01456-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="01456-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01456-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01456-114">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="01456-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="01456-115">Istanza di che rappresenta la visualizzazione normalizzata della risorsa gestita.</span><span class="sxs-lookup"><span data-stu-id="01456-115">The instance that represents the normalized view of the managed resource.</span></span>

</dd> <dt>

<span data-ttu-id="01456-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="01456-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01456-117">Tipo di dati **: \_ visualizzazione CIM**</span><span class="sxs-lookup"><span data-stu-id="01456-117">Data type: **CIM\_View**</span></span>
</dt> <dt>

<span data-ttu-id="01456-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01456-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01456-119">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="01456-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="01456-120">Visualizzazione che rappresenta una vista denormalizzata o aggregata della risorsa gestita.</span><span class="sxs-lookup"><span data-stu-id="01456-120">The view that represents a de-normalized or aggregate view of the managed resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01456-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01456-121">Requirements</span></span>



| <span data-ttu-id="01456-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="01456-122">Requirement</span></span> | <span data-ttu-id="01456-123">Valore</span><span class="sxs-lookup"><span data-stu-id="01456-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01456-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01456-124">Minimum supported client</span></span><br/> | <span data-ttu-id="01456-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="01456-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="01456-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01456-126">Minimum supported server</span></span><br/> | <span data-ttu-id="01456-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="01456-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="01456-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="01456-128">Namespace</span></span><br/>                | <span data-ttu-id="01456-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="01456-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="01456-130">MOF</span><span class="sxs-lookup"><span data-stu-id="01456-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01456-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01456-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="01456-132">DLL</span><span class="sxs-lookup"><span data-stu-id="01456-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01456-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="01456-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="01456-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01456-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01456-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="01456-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

