---
description: Descrive l'impostazione dei dati per un controller di visualizzazione sintetica virtuale.
ms.assetid: cea79b24-4175-49db-a8b4-a9efb1fd0b96
title: Classe Msvm_SyntheticDisplayControllerSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayControllerSettingData
- Msvm_SyntheticDisplayControllerSettingData.ResolutionType
- Msvm_SyntheticDisplayControllerSettingData.HorizontalResolution
- Msvm_SyntheticDisplayControllerSettingData.VerticalResolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 52935800eda641eb9015247e9320f33f22b40251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226866"
---
# <a name="msvm_syntheticdisplaycontrollersettingdata-class"></a><span data-ttu-id="3100d-103">\_Classe MSVM SyntheticDisplayControllerSettingData</span><span class="sxs-lookup"><span data-stu-id="3100d-103">Msvm\_SyntheticDisplayControllerSettingData class</span></span>

<span data-ttu-id="3100d-104">Descrive l'impostazione dei dati per un controller di visualizzazione sintetica virtuale.</span><span class="sxs-lookup"><span data-stu-id="3100d-104">Describes the setting data for a virtual synthetic display controller.</span></span>

<span data-ttu-id="3100d-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3100d-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3100d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3100d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  uint8  ResolutionType;
  uint16 HorizontalResolution;
  uint16 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="3100d-107">Members</span><span class="sxs-lookup"><span data-stu-id="3100d-107">Members</span></span>

<span data-ttu-id="3100d-108">La **classe \_ SyntheticDisplayControllerSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3100d-108">The **Msvm\_SyntheticDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3100d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3100d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3100d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3100d-110">Properties</span></span>

<span data-ttu-id="3100d-111">La **classe \_ SyntheticDisplayControllerSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3100d-111">The **Msvm\_SyntheticDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3100d-112">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="3100d-112">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3100d-113">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3100d-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3100d-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3100d-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3100d-115">Risoluzione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="3100d-115">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="3100d-116">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="3100d-116">**ResolutionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3100d-117">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3100d-117">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3100d-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3100d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3100d-119">Tipo di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="3100d-119">The resolution type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3100d-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3100d-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3100d-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="3100d-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="3100d-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Massimo** (2)</span><span class="sxs-lookup"><span data-stu-id="3100d-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>

<span data-ttu-id="3100d-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Singolo** (3)</span><span class="sxs-lookup"><span data-stu-id="3100d-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Single** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="3100d-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Impostazione predefinita** (4)</span><span class="sxs-lookup"><span data-stu-id="3100d-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="3100d-125">Aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="3100d-125">Added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3100d-126">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="3100d-126">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3100d-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3100d-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3100d-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3100d-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3100d-129">Risoluzione verticale.</span><span class="sxs-lookup"><span data-stu-id="3100d-129">The vertical resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3100d-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3100d-130">Requirements</span></span>



| <span data-ttu-id="3100d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3100d-131">Requirement</span></span> | <span data-ttu-id="3100d-132">Valore</span><span class="sxs-lookup"><span data-stu-id="3100d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3100d-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3100d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3100d-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3100d-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3100d-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3100d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3100d-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3100d-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3100d-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3100d-137">Namespace</span></span><br/>                | <span data-ttu-id="3100d-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3100d-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3100d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3100d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3100d-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3100d-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3100d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3100d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3100d-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3100d-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3100d-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3100d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3100d-144">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3100d-144">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




