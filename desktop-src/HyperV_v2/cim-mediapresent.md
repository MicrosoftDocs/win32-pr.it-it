---
description: Rappresenta una relazione in cui è necessario accedere a un extent di archiviazione tramite un dispositivo di accesso multimediale.
ms.assetid: 436a7e2d-2c14-4058-aca0-669373b8004a
title: Classe CIM_MediaPresent (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Antecedent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e26c36231edaf3ca4b8accf844a3c58b3d70bc7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320467"
---
# <a name="cim_mediapresent-class-hyper-v-management"></a><span data-ttu-id="7eec3-103">Classe CIM_MediaPresent (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="7eec3-103">CIM_MediaPresent class (Hyper-V management)</span></span>

<span data-ttu-id="7eec3-104">Rappresenta una relazione in cui è necessario accedere a un extent di archiviazione tramite un dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="7eec3-104">Represents a relationship in which a storage extent must be accessed through a media access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eec3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7eec3-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageExtents"), MappingStrings("MIF.DMTF|Storage Devices|001.8"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="7eec3-106">Members</span><span class="sxs-lookup"><span data-stu-id="7eec3-106">Members</span></span>

<span data-ttu-id="7eec3-107">La classe **CIM \_ MediaPresent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7eec3-107">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="7eec3-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7eec3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7eec3-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7eec3-109">Properties</span></span>

<span data-ttu-id="7eec3-110">La classe **CIM \_ MediaPresent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7eec3-110">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7eec3-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7eec3-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec3-112">Tipo di dati: **CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="7eec3-112">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="7eec3-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eec3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eec3-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="7eec3-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7eec3-115">Il dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="7eec3-115">The media access device.</span></span>

</dd> <dt>

<span data-ttu-id="7eec3-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="7eec3-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec3-117">Tipo di dati: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="7eec3-117">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="7eec3-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eec3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eec3-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="7eec3-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7eec3-120">L'extent di archiviazione a cui si accede quando si usa il dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="7eec3-120">The storage extent that is accessed when using the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="7eec3-121">**FixedMedia**</span><span class="sxs-lookup"><span data-stu-id="7eec3-121">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec3-122">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7eec3-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eec3-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eec3-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec3-124">**true** se l'extent di archiviazione è fisso nel dispositivo di accesso multimediale e non può essere espulso; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7eec3-124">**true** if the storage extent is fixed in the media access device and can not be ejected; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7eec3-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7eec3-125">Requirements</span></span>



| <span data-ttu-id="7eec3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eec3-126">Requirement</span></span> | <span data-ttu-id="7eec3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7eec3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eec3-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7eec3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7eec3-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7eec3-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7eec3-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7eec3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7eec3-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7eec3-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7eec3-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7eec3-132">Namespace</span></span><br/>                | <span data-ttu-id="7eec3-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7eec3-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7eec3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7eec3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eec3-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7eec3-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eec3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7eec3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eec3-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7eec3-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7eec3-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7eec3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eec3-139">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="7eec3-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

