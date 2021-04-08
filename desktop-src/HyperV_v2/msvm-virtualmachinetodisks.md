---
description: Impostazione dei dati da passare come matrice alla \_ classe CollectionReferencePointExportSettingData di MSVM.
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Classe Msvm_VirtualMachineToDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cad5de9389b9cb1d5e7db0573f3a4e3fc271ba31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878710"
---
# <a name="msvm_virtualmachinetodisks-class"></a><span data-ttu-id="bfdf0-103">\_Classe MSVM VirtualMachineToDisks</span><span class="sxs-lookup"><span data-stu-id="bfdf0-103">Msvm\_VirtualMachineToDisks class</span></span>

<span data-ttu-id="bfdf0-104">Impostazione dei dati da passare come matrice alla classe [**\_ CollectionReferencePointExportSettingData di MSVM**](msvm-collectionreferencepointexportsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="bfdf0-104">Setting data to be passed as an array to the [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) class.</span></span>

<span data-ttu-id="bfdf0-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bfdf0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfdf0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfdf0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="bfdf0-107">Members</span><span class="sxs-lookup"><span data-stu-id="bfdf0-107">Members</span></span>

<span data-ttu-id="bfdf0-108">La **classe \_ VirtualMachineToDisks di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bfdf0-108">The **Msvm\_VirtualMachineToDisks** class has these types of members:</span></span>

-   [<span data-ttu-id="bfdf0-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bfdf0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bfdf0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bfdf0-110">Properties</span></span>

<span data-ttu-id="bfdf0-111">La **classe \_ VirtualMachineToDisks di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bfdf0-111">The **Msvm\_VirtualMachineToDisks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfdf0-112">**DisksToExport**</span><span class="sxs-lookup"><span data-stu-id="bfdf0-112">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfdf0-113">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bfdf0-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bfdf0-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bfdf0-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfdf0-115">ID dell'istanza WMI dei dischi che appartengono all'ID di macchina virtuale specificato per il quale devono essere esportati i dati.</span><span class="sxs-lookup"><span data-stu-id="bfdf0-115">The WMI instance IDs of the disks those belong to given Virtual Machine ID for which data needs to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="bfdf0-116">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="bfdf0-116">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfdf0-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfdf0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfdf0-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfdf0-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfdf0-119">ID di macchina virtuale a cui sono associati i dischi virtuali.</span><span class="sxs-lookup"><span data-stu-id="bfdf0-119">A Virtual Machine ID that virtual disks are associated with.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfdf0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfdf0-120">Requirements</span></span>



| <span data-ttu-id="bfdf0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfdf0-121">Requirement</span></span> | <span data-ttu-id="bfdf0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bfdf0-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfdf0-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfdf0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bfdf0-124">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bfdf0-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bfdf0-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfdf0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bfdf0-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bfdf0-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bfdf0-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bfdf0-127">Namespace</span></span><br/>                | <span data-ttu-id="bfdf0-128">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bfdf0-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bfdf0-129">MOF</span><span class="sxs-lookup"><span data-stu-id="bfdf0-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfdf0-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfdf0-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfdf0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bfdf0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfdf0-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bfdf0-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




