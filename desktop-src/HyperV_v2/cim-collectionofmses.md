---
description: Classe astratta per le sottoclassi che rappresentano una raccolta di \_ oggetti MANAGEDSYSTEMELEMENT CIM. Queste raccolte consentono di raggruppare gli elementi di sistema gestiti a scopo di identificazione e di semplificare l'associazione delle impostazioni e delle configurazioni.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: Classe CIM_CollectionOfMSEs (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880766"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a><span data-ttu-id="0d3ce-104">Classe CIM_CollectionOfMSEs (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="0d3ce-104">CIM_CollectionOfMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="0d3ce-105">Classe astratta per le sottoclassi che rappresentano una raccolta di oggetti [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="0d3ce-105">An abstract class for subclasses that represent a collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span> <span data-ttu-id="0d3ce-106">Queste raccolte consentono di raggruppare gli elementi di sistema gestiti a scopo di identificazione e di semplificare l'associazione delle impostazioni e delle configurazioni.</span><span class="sxs-lookup"><span data-stu-id="0d3ce-106">These collections allow managed system elements to be grouped for identification purposes and to simplify the association of settings and configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3ce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d3ce-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a><span data-ttu-id="0d3ce-108">Members</span><span class="sxs-lookup"><span data-stu-id="0d3ce-108">Members</span></span>

<span data-ttu-id="0d3ce-109">La classe **CIM \_ CollectionOfMSEs** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0d3ce-109">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="0d3ce-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d3ce-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d3ce-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d3ce-111">Properties</span></span>

<span data-ttu-id="0d3ce-112">La classe **CIM \_ CollectionOfMSEs** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0d3ce-112">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d3ce-113">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="0d3ce-113">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d3ce-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d3ce-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d3ce-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d3ce-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d3ce-116">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0d3ce-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0d3ce-117">Identificazione dell'oggetto raccolta.</span><span class="sxs-lookup"><span data-stu-id="0d3ce-117">The identification of the collection object.</span></span> <span data-ttu-id="0d3ce-118">Quando è sottoclassata, la proprietà **CollectionId** può essere sottoposta a override come proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="0d3ce-118">When subclassed, the **CollectionID** property can be overridden as a key property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d3ce-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d3ce-119">Requirements</span></span>



| <span data-ttu-id="0d3ce-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d3ce-120">Requirement</span></span> | <span data-ttu-id="0d3ce-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0d3ce-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3ce-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d3ce-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3ce-123">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0d3ce-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0d3ce-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d3ce-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3ce-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0d3ce-125">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0d3ce-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d3ce-126">Namespace</span></span><br/>                | <span data-ttu-id="0d3ce-127">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0d3ce-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0d3ce-128">MOF</span><span class="sxs-lookup"><span data-stu-id="0d3ce-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d3ce-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d3ce-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d3ce-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0d3ce-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d3ce-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d3ce-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d3ce-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d3ce-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3ce-133">**\_Raccolta CIM**</span><span class="sxs-lookup"><span data-stu-id="0d3ce-133">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

