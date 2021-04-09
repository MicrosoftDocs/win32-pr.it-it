---
description: La \_ classe CIM VideoControllerResolution rappresenta le varie modalità video che un controller video può supportare.
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: Classe CIM_VideoControllerResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d448d92d79163bc6a4e1056e88434081c5878159
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878326"
---
# <a name="cim_videocontrollerresolution-class"></a><span data-ttu-id="96a3f-103">CIM \_ VideoControllerResolution (classe)</span><span class="sxs-lookup"><span data-stu-id="96a3f-103">CIM\_VideoControllerResolution class</span></span>

<span data-ttu-id="96a3f-104">La classe **CIM \_ VideoControllerResolution** rappresenta le varie modalità video che un controller video può supportare.</span><span class="sxs-lookup"><span data-stu-id="96a3f-104">The **CIM\_VideoControllerResolution** class represents the various video modes that a video controller can support.</span></span> <span data-ttu-id="96a3f-105">Le modalità video sono definite in base alle possibili risoluzioni orizzontali e verticali, alla frequenza di aggiornamento, alla modalità di analisi e al numero di impostazioni del colore supportate da un controller.</span><span class="sxs-lookup"><span data-stu-id="96a3f-105">Video modes are defined by the possible horizontal and vertical resolutions, refresh rate, scan mode, and number of color settings supported by a controller.</span></span> <span data-ttu-id="96a3f-106">Le risoluzioni effettive in uso sono i valori specificati nell'oggetto [**\_ VideoController CIM**](cim-videocontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="96a3f-106">The actual resolutions in use are the values specified in the [**CIM\_VideoController**](cim-videocontroller.md) object.</span></span>

<span data-ttu-id="96a3f-107">L'hardware non compatibile con Windows Display Driver Model (WDDM) restituisce valori di proprietà non accurati per le istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="96a3f-107">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96a3f-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="96a3f-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="96a3f-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="96a3f-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="96a3f-110">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="96a3f-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="96a3f-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="96a3f-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a3f-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96a3f-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="96a3f-113">Members</span><span class="sxs-lookup"><span data-stu-id="96a3f-113">Members</span></span>

<span data-ttu-id="96a3f-114">La classe **CIM \_ VideoControllerResolution** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="96a3f-114">The **CIM\_VideoControllerResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="96a3f-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96a3f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96a3f-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96a3f-116">Properties</span></span>

<span data-ttu-id="96a3f-117">La classe **CIM \_ VideoControllerResolution** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="96a3f-117">The **CIM\_VideoControllerResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96a3f-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="96a3f-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96a3f-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="96a3f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96a3f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="96a3f-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="96a3f-122">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="96a3f-122">Short textual description of the current object.</span></span>

<span data-ttu-id="96a3f-123">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="96a3f-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="96a3f-124">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="96a3f-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96a3f-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="96a3f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96a3f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96a3f-127">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="96a3f-127">Textual description of the current object.</span></span>

<span data-ttu-id="96a3f-128">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="96a3f-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="96a3f-129">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="96a3f-129">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96a3f-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96a3f-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96a3f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-132">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="96a3f-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="96a3f-133">Risoluzione orizzontale in pixel.</span><span class="sxs-lookup"><span data-stu-id="96a3f-133">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="96a3f-134">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="96a3f-134">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96a3f-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96a3f-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96a3f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-137">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,7 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="96a3f-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="96a3f-138">Frequenza di aggiornamento massima quando un intervallo di frequenze è supportato alle risoluzioni specificate, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="96a3f-138">Maximum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="96a3f-139">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="96a3f-139">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96a3f-140">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96a3f-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96a3f-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-142">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,6 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="96a3f-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="96a3f-143">Frequenza di aggiornamento minima quando un intervallo di frequenze è supportato alle risoluzioni specificate, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="96a3f-143">Minimum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="96a3f-144">**NumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="96a3f-144">**NumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96a3f-145">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="96a3f-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96a3f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-147">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")</span><span class="sxs-lookup"><span data-stu-id="96a3f-147">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")</span></span>
</dt> </dl>

<span data-ttu-id="96a3f-148">Numero di colori supportati nella risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="96a3f-148">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="96a3f-149">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="96a3f-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="96a3f-150">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="96a3f-150">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96a3f-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96a3f-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96a3f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-153">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="96a3f-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="96a3f-154">Frequenza di aggiornamento, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="96a3f-154">Refresh rate, in hertz.</span></span> <span data-ttu-id="96a3f-155">Se è supportato un intervallo di frequenze, usare le proprietà **MinRefreshRate** e **MaxRefreshRate** e impostare questa proprietà su 0.</span><span class="sxs-lookup"><span data-stu-id="96a3f-155">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="96a3f-156">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="96a3f-156">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96a3f-157">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="96a3f-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96a3f-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-159">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Risoluzioni di \| monitoraggio DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="96a3f-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="96a3f-160">Modalità di analisi in cui opera il controller.</span><span class="sxs-lookup"><span data-stu-id="96a3f-160">Scan mode at which the controller operates.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="96a3f-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="96a3f-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="96a3f-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="96a3f-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="96a3f-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (3)</span><span class="sxs-lookup"><span data-stu-id="96a3f-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="96a3f-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Operazione non interlacciata** (4)</span><span class="sxs-lookup"><span data-stu-id="96a3f-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (4)</span></span>


</dt> <dd>

<span data-ttu-id="96a3f-165">Operazione non interlacciata</span><span class="sxs-lookup"><span data-stu-id="96a3f-165">Noninterlaced operation</span></span>

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="96a3f-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Operazione interlacciata** (5)</span><span class="sxs-lookup"><span data-stu-id="96a3f-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="96a3f-167">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="96a3f-167">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96a3f-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="96a3f-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96a3f-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-170">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("settingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="96a3f-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="96a3f-171">ID che funge da parte della chiave per l'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="96a3f-171">An ID that serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="96a3f-172">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="96a3f-172">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96a3f-173">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96a3f-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96a3f-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96a3f-175">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,3 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="96a3f-175">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="96a3f-176">Risoluzione verticale del controller, in pixel.</span><span class="sxs-lookup"><span data-stu-id="96a3f-176">Controller's vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96a3f-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="96a3f-177">Remarks</span></span>

<span data-ttu-id="96a3f-178">WMI implementa la classe **CIM \_ VideoControllerResolution** .</span><span class="sxs-lookup"><span data-stu-id="96a3f-178">WMI implements the **CIM\_VideoControllerResolution** class.</span></span> <span data-ttu-id="96a3f-179">La classe **CIM \_ VideoControllerResolution** è una classe dinamica.</span><span class="sxs-lookup"><span data-stu-id="96a3f-179">The **CIM\_VideoControllerResolution** class is a dynamic class.</span></span>

<span data-ttu-id="96a3f-180">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="96a3f-180">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="96a3f-181">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="96a3f-181">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="96a3f-182">Si noti che questa classe è una classe di base.</span><span class="sxs-lookup"><span data-stu-id="96a3f-182">Note that this class is a base class.</span></span> <span data-ttu-id="96a3f-183">Se si sta tentando di accedere al controller video tramite WMI, è possibile utilizzare [**Win32 \_ VideoController**](win32-videocontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="96a3f-183">If you are attempting to access your video controller through WMI, you may wish to use [**Win32\_VideoController**](win32-videocontroller.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="96a3f-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96a3f-184">Requirements</span></span>



| <span data-ttu-id="96a3f-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="96a3f-185">Requirement</span></span> | <span data-ttu-id="96a3f-186">Valore</span><span class="sxs-lookup"><span data-stu-id="96a3f-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96a3f-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96a3f-187">Minimum supported client</span></span><br/> | <span data-ttu-id="96a3f-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96a3f-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96a3f-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96a3f-189">Minimum supported server</span></span><br/> | <span data-ttu-id="96a3f-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96a3f-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96a3f-191">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="96a3f-191">Namespace</span></span><br/>                | <span data-ttu-id="96a3f-192">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="96a3f-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="96a3f-193">MOF</span><span class="sxs-lookup"><span data-stu-id="96a3f-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96a3f-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96a3f-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="96a3f-195">DLL</span><span class="sxs-lookup"><span data-stu-id="96a3f-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96a3f-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96a3f-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96a3f-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96a3f-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a3f-198">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="96a3f-198">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

