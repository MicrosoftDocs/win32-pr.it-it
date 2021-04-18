---
description: Rappresenta un'unità DVD.
ms.assetid: 6127b58d-c70f-47c7-9eeb-6aff819f672e
title: Classe CIM_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DVDDrive
- CIM_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44c69cfe537257076623e472f4bb1406f8bf7665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308348"
---
# <a name="cim_dvddrive-class"></a><span data-ttu-id="69b5b-103">CIM \_ DVDDrive (classe)</span><span class="sxs-lookup"><span data-stu-id="69b5b-103">CIM\_DVDDrive class</span></span>

<span data-ttu-id="69b5b-104">Rappresenta un'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="69b5b-104">Represents a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b5b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69b5b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_DVDDrive : CIM_MediaAccessDevice
{
  uint16 FormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="69b5b-106">Members</span><span class="sxs-lookup"><span data-stu-id="69b5b-106">Members</span></span>

<span data-ttu-id="69b5b-107">La classe **CIM \_ DVDDrive** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="69b5b-107">The **CIM\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="69b5b-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="69b5b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69b5b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="69b5b-109">Properties</span></span>

<span data-ttu-id="69b5b-110">La classe **CIM \_ DVDDrive** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="69b5b-110">The **CIM\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69b5b-111">**FormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="69b5b-111">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b5b-112">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="69b5b-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="69b5b-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="69b5b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69b5b-114">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalMedia**](/windows/desktop/CIMWin32Prov/cim-physicalmedia).**MediaType**")</span><span class="sxs-lookup"><span data-stu-id="69b5b-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMedia**](/windows/desktop/CIMWin32Prov/cim-physicalmedia).**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="69b5b-115">Formati CD e DVD supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69b5b-115">The CD and DVD formats that are supported by the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="69b5b-116">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="69b5b-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="69b5b-117">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="69b5b-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="69b5b-118">**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="69b5b-118">**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="69b5b-119">**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="69b5b-119">**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="69b5b-120">**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="69b5b-120">**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="69b5b-121">**CD registrabile** (19)</span><span class="sxs-lookup"><span data-stu-id="69b5b-121">**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="69b5b-122">**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="69b5b-122">**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW_"></span><span id="dvd-rw_"></span>

<span data-ttu-id="69b5b-123">**DVD-RW +** (23)</span><span class="sxs-lookup"><span data-stu-id="69b5b-123">**DVD-RW+** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="69b5b-124">**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="69b5b-124">**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="69b5b-125">**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="69b5b-125">**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="69b5b-126">**DVD-video** (26)</span><span class="sxs-lookup"><span data-stu-id="69b5b-126">**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="69b5b-127">**DivX** (27)</span><span class="sxs-lookup"><span data-stu-id="69b5b-127">**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="69b5b-128">**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="69b5b-128">**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="69b5b-129">**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="69b5b-129">**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="69b5b-130">**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="69b5b-130">**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="69b5b-131">**DVD registrabile** (36)</span><span class="sxs-lookup"><span data-stu-id="69b5b-131">**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="69b5b-132">**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="69b5b-132">**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="69b5b-133">**DVD-audio** (38)</span><span class="sxs-lookup"><span data-stu-id="69b5b-133">**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="69b5b-134">**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="69b5b-134">**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="69b5b-135">**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="69b5b-135">**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="69b5b-136">**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="69b5b-136">**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="69b5b-137">**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="69b5b-137">**DVD-18** (42)</span></span>


<span data-ttu-id="69b5b-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="69b5b-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="69b5b-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69b5b-139">Requirements</span></span>



| <span data-ttu-id="69b5b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b5b-140">Requirement</span></span> | <span data-ttu-id="69b5b-141">Valore</span><span class="sxs-lookup"><span data-stu-id="69b5b-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b5b-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69b5b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="69b5b-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="69b5b-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="69b5b-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69b5b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="69b5b-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69b5b-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="69b5b-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="69b5b-146">Namespace</span></span><br/>                | <span data-ttu-id="69b5b-147">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="69b5b-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="69b5b-148">MOF</span><span class="sxs-lookup"><span data-stu-id="69b5b-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69b5b-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69b5b-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69b5b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="69b5b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69b5b-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69b5b-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69b5b-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69b5b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b5b-153">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="69b5b-153">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

