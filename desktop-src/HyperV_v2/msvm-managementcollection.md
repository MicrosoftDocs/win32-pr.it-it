---
description: Rappresenta una raccolta di altre raccolte.
ms.assetid: 1f7f5517-55d9-44a3-b0ca-444a9d7d5941
title: Classe Msvm_ManagementCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ManagementCollection
- Msvm_ManagementCollection.CollectionID
- Msvm_ManagementCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2d3499bb161495152b6de4b8aebd7c64d041d069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318341"
---
# <a name="msvm_managementcollection-class"></a><span data-ttu-id="5af05-103">MSVM \_ managementcollection (classe)</span><span class="sxs-lookup"><span data-stu-id="5af05-103">Msvm\_ManagementCollection class</span></span>

<span data-ttu-id="5af05-104">Rappresenta una raccolta di altre raccolte.</span><span class="sxs-lookup"><span data-stu-id="5af05-104">Represents a collection of other collections.</span></span>

<span data-ttu-id="5af05-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5af05-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af05-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5af05-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ManagementCollection : CIM_CollectionOfMSEs
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="5af05-107">Members</span><span class="sxs-lookup"><span data-stu-id="5af05-107">Members</span></span>

<span data-ttu-id="5af05-108">La classe **MSVM \_ managementcollection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5af05-108">The **Msvm\_ManagementCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="5af05-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5af05-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5af05-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5af05-110">Properties</span></span>

<span data-ttu-id="5af05-111">La classe **MSVM \_ managementcollection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5af05-111">The **Msvm\_ManagementCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5af05-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="5af05-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af05-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5af05-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af05-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5af05-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af05-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5af05-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5af05-116">Identificazione univoca dell'oggetto raccolta.</span><span class="sxs-lookup"><span data-stu-id="5af05-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="5af05-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5af05-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af05-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5af05-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af05-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5af05-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af05-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="5af05-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="5af05-121">Nome definito dall'utente per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="5af05-121">An user-defined name for the collection.</span></span> <span data-ttu-id="5af05-122">Si noti che non è garantito che sia univoco.</span><span class="sxs-lookup"><span data-stu-id="5af05-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5af05-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5af05-123">Requirements</span></span>



| <span data-ttu-id="5af05-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5af05-124">Requirement</span></span> | <span data-ttu-id="5af05-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5af05-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af05-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5af05-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5af05-127">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5af05-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5af05-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5af05-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5af05-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5af05-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5af05-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5af05-130">Namespace</span></span><br/>                | <span data-ttu-id="5af05-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5af05-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5af05-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5af05-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5af05-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5af05-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5af05-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5af05-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5af05-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5af05-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5af05-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5af05-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af05-137">**\_COLLECTIONOFMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="5af05-137">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

