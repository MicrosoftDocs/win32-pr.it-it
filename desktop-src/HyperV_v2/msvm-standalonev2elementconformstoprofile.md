---
description: Definisce i profili registrati a cui è conforme il sistema autonomo a cui si fa riferimento.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Classe Msvm_StandaloneV2ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967028"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a><span data-ttu-id="42536-103">\_Classe MSVM StandaloneV2ElementConformsToProfile</span><span class="sxs-lookup"><span data-stu-id="42536-103">Msvm\_StandaloneV2ElementConformsToProfile class</span></span>

<span data-ttu-id="42536-104">Definisce i profili registrati a cui è conforme il sistema autonomo a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="42536-104">Defines the registered profiles to which the referenced standalone system conforms.</span></span>

<span data-ttu-id="42536-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="42536-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42536-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42536-106">Syntax</span></span>

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="42536-107">Members</span><span class="sxs-lookup"><span data-stu-id="42536-107">Members</span></span>

<span data-ttu-id="42536-108">La **classe \_ StandaloneV2ElementConformsToProfile di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="42536-108">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="42536-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="42536-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42536-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="42536-110">Properties</span></span>

<span data-ttu-id="42536-111">La **classe \_ StandaloneV2ElementConformsToProfile di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="42536-111">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42536-112">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="42536-112">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42536-113">Tipo di dati: **MSVM \_ RegisteredProfile**</span><span class="sxs-lookup"><span data-stu-id="42536-113">Data type: **Msvm\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="42536-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42536-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42536-115">Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="42536-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="42536-116">Profilo registrato a cui è conforme il sistema autonomo.</span><span class="sxs-lookup"><span data-stu-id="42536-116">The registered profile to which the standalone system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="42536-117">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="42536-117">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42536-118">Tipo di dati: **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="42536-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="42536-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42536-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42536-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT \_ targetNamespace** ("root \\ \\ Virtualization \\ \\ v2")</span><span class="sxs-lookup"><span data-stu-id="42536-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT\_TargetNamespace** ("root\\\\virtualization\\\\v2")</span></span>
</dt> </dl>

<span data-ttu-id="42536-121">Sistema autonomo conforme al profilo registrato.</span><span class="sxs-lookup"><span data-stu-id="42536-121">The standalone system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42536-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42536-122">Requirements</span></span>



| <span data-ttu-id="42536-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="42536-123">Requirement</span></span> | <span data-ttu-id="42536-124">Valore</span><span class="sxs-lookup"><span data-stu-id="42536-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42536-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42536-125">Minimum supported client</span></span><br/> | <span data-ttu-id="42536-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="42536-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="42536-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42536-127">Minimum supported server</span></span><br/> | <span data-ttu-id="42536-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="42536-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="42536-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="42536-129">Namespace</span></span><br/>                | <span data-ttu-id="42536-130">\\Interoperabilità radice</span><span class="sxs-lookup"><span data-stu-id="42536-130">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="42536-131">MOF</span><span class="sxs-lookup"><span data-stu-id="42536-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42536-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42536-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42536-133">DLL</span><span class="sxs-lookup"><span data-stu-id="42536-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42536-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42536-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42536-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42536-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42536-136">**\_ElementConformsToProfile MSVM**</span><span class="sxs-lookup"><span data-stu-id="42536-136">**Msvm\_ElementConformsToProfile**</span></span>](msvm-elementconformstoprofile.md)
</dt> </dl>

 

