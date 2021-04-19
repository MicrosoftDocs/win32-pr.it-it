---
description: La \_ classe CIM BinarySensor fornisce un output booleano.
ms.assetid: 51396a51-78ea-4c49-8dcc-7fb815f334ae
ms.tgt_platform: multiple
title: Classe CIM_BinarySensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BinarySensor
- CIM_BinarySensor.Caption
- CIM_BinarySensor.Description
- CIM_BinarySensor.InstallDate
- CIM_BinarySensor.Name
- CIM_BinarySensor.Status
- CIM_BinarySensor.Availability
- CIM_BinarySensor.ConfigManagerErrorCode
- CIM_BinarySensor.ConfigManagerUserConfig
- CIM_BinarySensor.CreationClassName
- CIM_BinarySensor.DeviceID
- CIM_BinarySensor.PowerManagementCapabilities
- CIM_BinarySensor.ErrorCleared
- CIM_BinarySensor.ErrorDescription
- CIM_BinarySensor.LastErrorCode
- CIM_BinarySensor.PNPDeviceID
- CIM_BinarySensor.PowerManagementSupported
- CIM_BinarySensor.StatusInfo
- CIM_BinarySensor.SystemCreationClassName
- CIM_BinarySensor.SystemName
- CIM_BinarySensor.CurrentReading
- CIM_BinarySensor.ExpectedReading
- CIM_BinarySensor.InterpretationOfFalse
- CIM_BinarySensor.InterpretationOfTrue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0d795f98473c09937571d415e34cf6fcb7f3486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305038"
---
# <a name="cim_binarysensor-class"></a><span data-ttu-id="2b042-103">CIM \_ BinarySensor (classe)</span><span class="sxs-lookup"><span data-stu-id="2b042-103">CIM\_BinarySensor class</span></span>

<span data-ttu-id="2b042-104">La classe **CIM \_ BinarySensor** fornisce un output booleano.</span><span class="sxs-lookup"><span data-stu-id="2b042-104">The **CIM\_BinarySensor** class provides a Boolean output.</span></span> <span data-ttu-id="2b042-105">Sono state aggiunte le proprietà **CurrentState** e **PossibleStates** per i sensori, rendendo la sottoclasse **CIM \_ BinarySensor** non più necessaria, sebbene venga mantenuta per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="2b042-105">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="2b042-106">È possibile creare un sensore binario creando un'istanza di un sensore con due stati possibili.</span><span class="sxs-lookup"><span data-stu-id="2b042-106">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b042-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2b042-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2b042-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2b042-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2b042-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2b042-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2b042-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2b042-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b042-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b042-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{11140D44-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_BinarySensor : CIM_Sensor
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  CurrentReading;
  boolean  ExpectedReading;
  string   InterpretationOfFalse;
  string   InterpretationOfTrue;
};
```

## <a name="members"></a><span data-ttu-id="2b042-112">Members</span><span class="sxs-lookup"><span data-stu-id="2b042-112">Members</span></span>

<span data-ttu-id="2b042-113">La classe **CIM \_ BinarySensor** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2b042-113">The **CIM\_BinarySensor** class has these types of members:</span></span>

-   [<span data-ttu-id="2b042-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="2b042-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2b042-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b042-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2b042-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="2b042-116">Methods</span></span>

<span data-ttu-id="2b042-117">La classe **CIM \_ BinarySensor** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2b042-117">The **CIM\_BinarySensor** class has these methods.</span></span>



| <span data-ttu-id="2b042-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="2b042-118">Method</span></span>                                                                  | <span data-ttu-id="2b042-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b042-119">Description</span></span>                                                                                                                                |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b042-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2b042-120">**Reset**</span></span>](reset-method-in-class-cim-binarysensor.md)                 | <span data-ttu-id="2b042-121">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2b042-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="2b042-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="2b042-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="2b042-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2b042-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-binarysensor.md) | <span data-ttu-id="2b042-124">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="2b042-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="2b042-125">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="2b042-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2b042-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b042-126">Properties</span></span>

<span data-ttu-id="2b042-127">La classe **CIM \_ BinarySensor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b042-127">The **CIM\_BinarySensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b042-128">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="2b042-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b042-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-131">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2b042-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2b042-132">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b042-132">Availability and status of the device.</span></span>

<span data-ttu-id="2b042-133">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2b042-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2b042-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b042-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2b042-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2b042-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="2b042-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2b042-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="2b042-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2b042-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="2b042-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2b042-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="2b042-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2b042-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="2b042-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2b042-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="2b042-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2b042-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="2b042-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2b042-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="2b042-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2b042-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="2b042-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2b042-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="2b042-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2b042-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="2b042-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-147">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2b042-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2b042-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="2b042-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-149">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="2b042-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2b042-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="2b042-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-151">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="2b042-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2b042-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="2b042-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2b042-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="2b042-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-154">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2b042-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2b042-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="2b042-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-156">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="2b042-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2b042-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="2b042-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-158">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="2b042-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2b042-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="2b042-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-160">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="2b042-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2b042-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="2b042-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-162">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="2b042-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2b042-163">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2b042-163">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-166">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2b042-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2b042-167">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b042-167">A short textual description of the object.</span></span>

<span data-ttu-id="2b042-168">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-169">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2b042-169">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b042-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-172">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2b042-172">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2b042-173">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2b042-173">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2b042-174">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-174">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2b042-175">**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="2b042-175">**This device is working properly.**</span></span> <span data-ttu-id="2b042-176"> (0)</span><span class="sxs-lookup"><span data-stu-id="2b042-176">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2b042-177">**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="2b042-177">**This device is not configured correctly.**</span></span> <span data-ttu-id="2b042-178">(1)</span><span class="sxs-lookup"><span data-stu-id="2b042-178">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2b042-179">**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-179">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2b042-180">(2)</span><span class="sxs-lookup"><span data-stu-id="2b042-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2b042-181">**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="2b042-181">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2b042-182">(3)</span><span class="sxs-lookup"><span data-stu-id="2b042-182">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2b042-183">**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="2b042-183">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2b042-184">(4)</span><span class="sxs-lookup"><span data-stu-id="2b042-184">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2b042-185">**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="2b042-185">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2b042-186">(5)</span><span class="sxs-lookup"><span data-stu-id="2b042-186">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2b042-187">**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="2b042-187">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2b042-188"> (6)</span><span class="sxs-lookup"><span data-stu-id="2b042-188">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2b042-189">**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="2b042-189">**Cannot filter.**</span></span> <span data-ttu-id="2b042-190">(7)</span><span class="sxs-lookup"><span data-stu-id="2b042-190">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2b042-191">**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="2b042-191">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2b042-192">(8)</span><span class="sxs-lookup"><span data-stu-id="2b042-192">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2b042-193">**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="2b042-193">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2b042-194">(9)</span><span class="sxs-lookup"><span data-stu-id="2b042-194">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2b042-195">**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-195">**This device cannot start.**</span></span> <span data-ttu-id="2b042-196">(10)</span><span class="sxs-lookup"><span data-stu-id="2b042-196">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2b042-197">**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-197">**This device failed.**</span></span> <span data-ttu-id="2b042-198">(11)</span><span class="sxs-lookup"><span data-stu-id="2b042-198">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2b042-199">**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="2b042-199">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2b042-200">12</span><span class="sxs-lookup"><span data-stu-id="2b042-200">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2b042-201">**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-201">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2b042-202">(13)</span><span class="sxs-lookup"><span data-stu-id="2b042-202">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2b042-203">**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="2b042-203">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2b042-204">(14)</span><span class="sxs-lookup"><span data-stu-id="2b042-204">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2b042-205">**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="2b042-205">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2b042-206">(15)</span><span class="sxs-lookup"><span data-stu-id="2b042-206">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2b042-207">**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-207">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2b042-208">(16)</span><span class="sxs-lookup"><span data-stu-id="2b042-208">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2b042-209">**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="2b042-209">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2b042-210">(17)</span><span class="sxs-lookup"><span data-stu-id="2b042-210">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2b042-211">**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-211">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2b042-212">(18)</span><span class="sxs-lookup"><span data-stu-id="2b042-212">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2b042-213">**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="2b042-213">**Failure using the VxD loader.**</span></span> <span data-ttu-id="2b042-214">(19)</span><span class="sxs-lookup"><span data-stu-id="2b042-214">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2b042-215">**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="2b042-215">**Your registry might be corrupted.**</span></span> <span data-ttu-id="2b042-216">(20)</span><span class="sxs-lookup"><span data-stu-id="2b042-216">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2b042-217">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-217">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2b042-218">(21)</span><span class="sxs-lookup"><span data-stu-id="2b042-218">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2b042-219">**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="2b042-219">**This device is disabled.**</span></span> <span data-ttu-id="2b042-220">(22)</span><span class="sxs-lookup"><span data-stu-id="2b042-220">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2b042-221">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="2b042-221">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2b042-222">(23)</span><span class="sxs-lookup"><span data-stu-id="2b042-222">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2b042-223">**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="2b042-223">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2b042-224">(24)</span><span class="sxs-lookup"><span data-stu-id="2b042-224">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2b042-225">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-225">**Windows is still setting up this device.**</span></span> <span data-ttu-id="2b042-226">(25)</span><span class="sxs-lookup"><span data-stu-id="2b042-226">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2b042-227">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-227">**Windows is still setting up this device.**</span></span> <span data-ttu-id="2b042-228">(26)</span><span class="sxs-lookup"><span data-stu-id="2b042-228">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2b042-229">**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="2b042-229">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2b042-230">(27)</span><span class="sxs-lookup"><span data-stu-id="2b042-230">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2b042-231">**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="2b042-231">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2b042-232">(28)</span><span class="sxs-lookup"><span data-stu-id="2b042-232">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2b042-233">**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="2b042-233">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2b042-234">(29)</span><span class="sxs-lookup"><span data-stu-id="2b042-234">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2b042-235">**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-235">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2b042-236">(30)</span><span class="sxs-lookup"><span data-stu-id="2b042-236">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2b042-237">**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2b042-237">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2b042-238">31</span><span class="sxs-lookup"><span data-stu-id="2b042-238">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2b042-239">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2b042-239">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-240">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b042-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-242">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2b042-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2b042-243">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2b042-243">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2b042-244">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-244">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-245">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2b042-245">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-248">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2b042-248">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2b042-249">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="2b042-249">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2b042-250">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="2b042-250">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2b042-251">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-251">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-252">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="2b042-252">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-253">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b042-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b042-255">Valore corrente indicato dal sensore.</span><span class="sxs-lookup"><span data-stu-id="2b042-255">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="2b042-256">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2b042-256">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-259">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2b042-259">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2b042-260">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b042-260">A textual description of the object.</span></span>

<span data-ttu-id="2b042-261">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-261">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-262">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2b042-262">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-263">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-265">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2b042-265">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2b042-266">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2b042-266">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2b042-267">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-267">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-268">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2b042-268">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-269">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b042-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b042-271">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="2b042-271">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2b042-272">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-273">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2b042-273">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b042-276">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2b042-276">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2b042-277">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-278">**ExpectedReading**</span><span class="sxs-lookup"><span data-stu-id="2b042-278">**ExpectedReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-279">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b042-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b042-281">Valore ' Normal ' del sensore.</span><span class="sxs-lookup"><span data-stu-id="2b042-281">'Normal' value for the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="2b042-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2b042-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-283">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2b042-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-285">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="2b042-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2b042-286">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="2b042-286">Indicates when the object was installed.</span></span> <span data-ttu-id="2b042-287">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="2b042-287">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2b042-288">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-289">**InterpretationOfFalse**</span><span class="sxs-lookup"><span data-stu-id="2b042-289">**InterpretationOfFalse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-290">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-292">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2b042-292">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2b042-293">Descrizione di un valore ' false ' dal sensore binario.</span><span class="sxs-lookup"><span data-stu-id="2b042-293">Description of a 'False' value from the binary sensor.</span></span> <span data-ttu-id="2b042-294">Queste informazioni possono essere visualizzate a un utente.</span><span class="sxs-lookup"><span data-stu-id="2b042-294">This information can be displayed to a user.</span></span>

</dd> <dt>

<span data-ttu-id="2b042-295">**InterpretationOfTrue**</span><span class="sxs-lookup"><span data-stu-id="2b042-295">**InterpretationOfTrue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-296">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-298">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2b042-298">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2b042-299">Descrizione di un valore ' true ' dal sensore binario.</span><span class="sxs-lookup"><span data-stu-id="2b042-299">Description of a 'True' value from the binary sensor.</span></span> <span data-ttu-id="2b042-300">Queste informazioni possono essere visualizzate a un utente.</span><span class="sxs-lookup"><span data-stu-id="2b042-300">This information can be displayed to a user.</span></span>

</dd> <dt>

<span data-ttu-id="2b042-301">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2b042-301">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-302">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b042-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b042-304">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2b042-304">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2b042-305">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-306">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2b042-306">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-309">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2b042-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2b042-310">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="2b042-310">Label by which the object is known.</span></span> <span data-ttu-id="2b042-311">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="2b042-311">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2b042-312">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-313">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2b042-313">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-314">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-316">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2b042-316">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2b042-317">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2b042-317">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2b042-318">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2b042-318">Example: "\*PNP030b"</span></span>

<span data-ttu-id="2b042-319">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-320">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2b042-320">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-321">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b042-321">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b042-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b042-323">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2b042-323">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="2b042-324">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b042-325"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2b042-325"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-326">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="2b042-326">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2b042-327"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2b042-327"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-328">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b042-328">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2b042-329"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="2b042-329"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-330">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="2b042-330">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2b042-331"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2b042-331"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-332">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="2b042-332">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2b042-333"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="2b042-333"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-334">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="2b042-334">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2b042-335"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="2b042-335"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-336">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="2b042-336">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="2b042-337">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="2b042-337">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="2b042-338">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2b042-338">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2b042-339"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="2b042-339"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-340">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="2b042-340">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2b042-341"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="2b042-341"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2b042-342">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="2b042-342">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2b042-343">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2b042-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-344">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b042-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b042-346">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2b042-346">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2b042-347">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2b042-347">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2b042-348">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="2b042-348">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2b042-349">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2b042-349">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2b042-350">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-351">**Status**</span><span class="sxs-lookup"><span data-stu-id="2b042-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-354">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2b042-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2b042-355">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b042-355">String that indicates the current status of the object.</span></span> <span data-ttu-id="2b042-356">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="2b042-356">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2b042-357">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="2b042-357">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2b042-358">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="2b042-358">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2b042-359">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="2b042-359">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2b042-360">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="2b042-360">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2b042-361">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="2b042-361">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2b042-362">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2b042-363">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b042-363">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2b042-364">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2b042-364">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2b042-365">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="2b042-365">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2b042-366">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="2b042-366">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b042-367">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="2b042-367">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2b042-368">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="2b042-368">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2b042-369">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="2b042-369">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2b042-370">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="2b042-370">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2b042-371">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="2b042-371">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2b042-372">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="2b042-372">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2b042-373">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="2b042-373">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2b042-374">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="2b042-374">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2b042-375">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="2b042-375">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2b042-376">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2b042-376">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-377">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b042-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-379">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2b042-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2b042-380">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2b042-380">State of the logical device.</span></span> <span data-ttu-id="2b042-381">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="2b042-381">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="2b042-382">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-382">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2b042-383">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2b042-383">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b042-384">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2b042-384">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2b042-385">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2b042-385">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2b042-386">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="2b042-386">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2b042-387">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="2b042-387">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2b042-388">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2b042-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-389">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-391">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2b042-391">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2b042-392">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2b042-392">The scoping system's creation class name.</span></span>

<span data-ttu-id="2b042-393">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b042-394">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2b042-394">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b042-395">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b042-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b042-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b042-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b042-397">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2b042-397">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2b042-398">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2b042-398">The scoping system's name.</span></span>

<span data-ttu-id="2b042-399">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b042-400">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b042-400">Remarks</span></span>

<span data-ttu-id="2b042-401">La classe **CIM \_ BinarySensor** è derivata dal [**\_ sensore CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="2b042-401">The **CIM\_BinarySensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="2b042-402">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="2b042-402">WMI does not implement this class.</span></span>

<span data-ttu-id="2b042-403">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="2b042-403">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2b042-404">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2b042-404">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b042-405">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b042-405">Requirements</span></span>



| <span data-ttu-id="2b042-406">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b042-406">Requirement</span></span> | <span data-ttu-id="2b042-407">Valore</span><span class="sxs-lookup"><span data-stu-id="2b042-407">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b042-408">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b042-408">Minimum supported client</span></span><br/> | <span data-ttu-id="2b042-409">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b042-409">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b042-410">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b042-410">Minimum supported server</span></span><br/> | <span data-ttu-id="2b042-411">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b042-411">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b042-412">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2b042-412">Namespace</span></span><br/>                | <span data-ttu-id="2b042-413">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2b042-413">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2b042-414">MOF</span><span class="sxs-lookup"><span data-stu-id="2b042-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b042-415"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b042-415"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b042-416">DLL</span><span class="sxs-lookup"><span data-stu-id="2b042-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b042-417"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b042-417"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b042-418">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b042-418">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b042-419">**\_Sensore CIM**</span><span class="sxs-lookup"><span data-stu-id="2b042-419">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

