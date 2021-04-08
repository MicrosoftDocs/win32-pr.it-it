---
description: Sposta un disco rigido virtuale dal percorso di origine a quello di destinazione.
ms.assetid: f51f7bf3-585a-442d-b84d-51d633c38dea
title: Classe Msvm_MoveUnmanagedVhd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MoveUnmanagedVhd
- Msvm_MoveUnmanagedVhd.VhdSourcePath
- Msvm_MoveUnmanagedVhd.VhdDestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e98139b747f4b32265e27bc84ca240f496dea715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885142"
---
# <a name="msvm_moveunmanagedvhd-class"></a><span data-ttu-id="7822b-103">\_Classe MSVM MoveUnmanagedVhd</span><span class="sxs-lookup"><span data-stu-id="7822b-103">Msvm\_MoveUnmanagedVhd class</span></span>

<span data-ttu-id="7822b-104">Sposta un disco rigido virtuale dal percorso di origine a quello di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7822b-104">Moves a virtual hard drive from the source to the destination path.</span></span>

<span data-ttu-id="7822b-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7822b-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7822b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7822b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_MoveUnmanagedVhd : CIM_ManagedElement
{
  string VhdSourcePath;
  string VhdDestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="7822b-107">Members</span><span class="sxs-lookup"><span data-stu-id="7822b-107">Members</span></span>

<span data-ttu-id="7822b-108">La **classe \_ MoveUnmanagedVhd di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7822b-108">The **Msvm\_MoveUnmanagedVhd** class has these types of members:</span></span>

-   [<span data-ttu-id="7822b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7822b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7822b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7822b-110">Properties</span></span>

<span data-ttu-id="7822b-111">La **classe \_ MoveUnmanagedVhd di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7822b-111">The **Msvm\_MoveUnmanagedVhd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7822b-112">**VhdDestinationPath**</span><span class="sxs-lookup"><span data-stu-id="7822b-112">**VhdDestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7822b-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7822b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7822b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7822b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7822b-115">Percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7822b-115">The destination path.</span></span>

</dd> <dt>

<span data-ttu-id="7822b-116">**VhdSourcePath**</span><span class="sxs-lookup"><span data-stu-id="7822b-116">**VhdSourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7822b-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7822b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7822b-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7822b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7822b-119">Percorso di origine dell'unità disco rigido virtuale da spostare.</span><span class="sxs-lookup"><span data-stu-id="7822b-119">The source path of the virtual hard drive to move.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7822b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7822b-120">Requirements</span></span>



| <span data-ttu-id="7822b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7822b-121">Requirement</span></span> | <span data-ttu-id="7822b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7822b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7822b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7822b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7822b-124">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7822b-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7822b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7822b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7822b-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7822b-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7822b-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7822b-127">Namespace</span></span><br/>                | <span data-ttu-id="7822b-128">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7822b-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7822b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="7822b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7822b-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7822b-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7822b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7822b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7822b-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7822b-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7822b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7822b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7822b-134">**\_ManagementName CIM**</span><span class="sxs-lookup"><span data-stu-id="7822b-134">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

 




