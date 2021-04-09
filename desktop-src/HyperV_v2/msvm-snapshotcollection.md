---
description: Rappresenta una raccolta di snapshot del sistema virtuale.
ms.assetid: c9b64421-232c-4f32-a088-6b98602ca3f4
title: Classe Msvm_SnapshotCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotCollection
- Msvm_SnapshotCollection.CollectionID
- Msvm_SnapshotCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e24566f1f5c5500258f14f88cbe2b7c4fa29e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130694"
---
# <a name="msvm_snapshotcollection-class"></a><span data-ttu-id="c79d2-103">\_Classe MSVM snapshotcollection</span><span class="sxs-lookup"><span data-stu-id="c79d2-103">Msvm\_SnapshotCollection class</span></span>

<span data-ttu-id="c79d2-104">Rappresenta una raccolta di snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="c79d2-104">Represents a collection of virtual system snapshots.</span></span>

<span data-ttu-id="c79d2-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c79d2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c79d2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c79d2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotCollection : CIM_Collection
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="c79d2-107">Members</span><span class="sxs-lookup"><span data-stu-id="c79d2-107">Members</span></span>

<span data-ttu-id="c79d2-108">La classe **MSVM \_ snapshotcollection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c79d2-108">The **Msvm\_SnapshotCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="c79d2-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c79d2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c79d2-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c79d2-110">Properties</span></span>

<span data-ttu-id="c79d2-111">La classe **MSVM \_ snapshotcollection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c79d2-111">The **Msvm\_SnapshotCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c79d2-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="c79d2-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c79d2-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c79d2-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c79d2-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c79d2-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c79d2-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c79d2-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c79d2-116">Identificazione univoca dell'oggetto raccolta.</span><span class="sxs-lookup"><span data-stu-id="c79d2-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="c79d2-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c79d2-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c79d2-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c79d2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c79d2-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c79d2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c79d2-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="c79d2-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="c79d2-121">Nome definito dall'utente per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="c79d2-121">An user-defined name for the collection.</span></span> <span data-ttu-id="c79d2-122">Si noti che non è garantito che sia univoco.</span><span class="sxs-lookup"><span data-stu-id="c79d2-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c79d2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c79d2-123">Requirements</span></span>



| <span data-ttu-id="c79d2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c79d2-124">Requirement</span></span> | <span data-ttu-id="c79d2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c79d2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c79d2-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c79d2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c79d2-127">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c79d2-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c79d2-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c79d2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c79d2-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c79d2-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c79d2-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c79d2-130">Namespace</span></span><br/>                | <span data-ttu-id="c79d2-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c79d2-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c79d2-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c79d2-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c79d2-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c79d2-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c79d2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c79d2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c79d2-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c79d2-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c79d2-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c79d2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79d2-137">**\_Raccolta CIM**</span><span class="sxs-lookup"><span data-stu-id="c79d2-137">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

