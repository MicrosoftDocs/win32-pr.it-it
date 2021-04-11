---
description: Rappresenta un dispositivo utilizzato per puntare alle aree di una visualizzazione.
ms.assetid: ffc675c3-29bd-4c54-8e54-8b6212daf66d
title: Classe CIM_PointingDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.Resolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57cca8c81a2d363e9e31bfc958a75b71e1b910d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132102"
---
# <a name="cim_pointingdevice-class-hyper-v-management"></a><span data-ttu-id="c7523-103">Classe CIM_PointingDevice (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="c7523-103">CIM_PointingDevice class (Hyper-V management)</span></span>

<span data-ttu-id="c7523-104">Rappresenta un dispositivo utilizzato per puntare alle aree di una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c7523-104">Represents a device used to point to regions of a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7523-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7523-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16 PointingType;
  uint8  NumberOfButtons;
  uint16 Handedness;
  uint32 Resolution;
};
```

## <a name="members"></a><span data-ttu-id="c7523-106">Members</span><span class="sxs-lookup"><span data-stu-id="c7523-106">Members</span></span>

<span data-ttu-id="c7523-107">La classe **CIM \_ PointingDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c7523-107">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="c7523-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c7523-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7523-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c7523-109">Properties</span></span>

<span data-ttu-id="c7523-110">La classe **CIM \_ PointingDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c7523-110">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7523-111">**Mano**</span><span class="sxs-lookup"><span data-stu-id="c7523-111">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7523-112">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7523-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7523-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c7523-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7523-114">Indica se il dispositivo di puntamento è configurato per l'operazione a destra o a sinistra.</span><span class="sxs-lookup"><span data-stu-id="c7523-114">Indicates whether the pointing device is configured for right or left handed operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7523-115">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="c7523-115">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c7523-116">**Non applicabile** (1)</span><span class="sxs-lookup"><span data-stu-id="c7523-116">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="c7523-117">**Operazione gestita a destra** (2)</span><span class="sxs-lookup"><span data-stu-id="c7523-117">**Right Handed Operation** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="c7523-118">**Operazione a sinistra** (3)</span><span class="sxs-lookup"><span data-stu-id="c7523-118">**Left Handed Operation** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7523-119">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="c7523-119">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7523-120">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c7523-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c7523-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c7523-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7523-122">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF che \| punta al dispositivo \| 003,4 ")</span><span class="sxs-lookup"><span data-stu-id="c7523-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.4")</span></span>
</dt> </dl>

<span data-ttu-id="c7523-123">Il numero di pulsanti sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7523-123">The number of buttons on the device.</span></span> <span data-ttu-id="c7523-124">Se il dispositivo di puntamento non ha pulsanti, questo valore deve essere impostato su "0".</span><span class="sxs-lookup"><span data-stu-id="c7523-124">If the pointing device has no buttons, this value should be set to "0".</span></span>

</dd> <dt>

<span data-ttu-id="c7523-125">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="c7523-125">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7523-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7523-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7523-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c7523-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7523-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF che \| punta al dispositivo \| 003,1 ")</span><span class="sxs-lookup"><span data-stu-id="c7523-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.1")</span></span>
</dt> </dl>

<span data-ttu-id="c7523-129">Tipo del dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="c7523-129">The type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7523-130">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c7523-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7523-131">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="c7523-131">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="c7523-132">**Mouse** (3)</span><span class="sxs-lookup"><span data-stu-id="c7523-132">**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="c7523-133">**Track Ball** (4)</span><span class="sxs-lookup"><span data-stu-id="c7523-133">**Track Ball** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="c7523-134">**Track point** (5)</span><span class="sxs-lookup"><span data-stu-id="c7523-134">**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="c7523-135">**Punto di scorrimento** (6)</span><span class="sxs-lookup"><span data-stu-id="c7523-135">**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="c7523-136">**Touch pad** (7)</span><span class="sxs-lookup"><span data-stu-id="c7523-136">**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="c7523-137">**Touchscreen** (8)</span><span class="sxs-lookup"><span data-stu-id="c7523-137">**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="c7523-138">**Sensore ottico del mouse** (9)</span><span class="sxs-lookup"><span data-stu-id="c7523-138">**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7523-139">**Risoluzione**</span><span class="sxs-lookup"><span data-stu-id="c7523-139">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7523-140">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7523-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7523-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c7523-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7523-142">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("conteggi per pollice"), **punito** ("conteggio/pollice")</span><span class="sxs-lookup"><span data-stu-id="c7523-142">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Counts per Inch"), **PUnit** ("count / inch")</span></span>
</dt> </dl>

<span data-ttu-id="c7523-143">Risoluzione del rilevamento del dispositivo di puntamento, in conteggi per pollice.</span><span class="sxs-lookup"><span data-stu-id="c7523-143">The tracking resolution of the pointing device, in counts per inch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7523-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7523-144">Requirements</span></span>



| <span data-ttu-id="c7523-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7523-145">Requirement</span></span> | <span data-ttu-id="c7523-146">Valore</span><span class="sxs-lookup"><span data-stu-id="c7523-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7523-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7523-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c7523-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c7523-148">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c7523-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7523-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c7523-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7523-150">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c7523-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c7523-151">Namespace</span></span><br/>                | <span data-ttu-id="c7523-152">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c7523-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c7523-153">MOF</span><span class="sxs-lookup"><span data-stu-id="c7523-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7523-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7523-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7523-155">DLL</span><span class="sxs-lookup"><span data-stu-id="c7523-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7523-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7523-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7523-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7523-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7523-158">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c7523-158">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

