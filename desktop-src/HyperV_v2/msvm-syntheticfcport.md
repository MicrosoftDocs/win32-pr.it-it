---
description: Rappresenta una porta Fibre Channel sintetica.
ms.assetid: 6ca827b5-3ea0-4967-ba1f-b41e84c84009
title: Classe Msvm_SyntheticFcPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPort
- Msvm_SyntheticFcPort.SetPowerState
- Msvm_SyntheticFcPort.EnableDevice
- Msvm_SyntheticFcPort.OnlineDevice
- Msvm_SyntheticFcPort.QuiesceDevice
- Msvm_SyntheticFcPort.SaveProperties
- Msvm_SyntheticFcPort.RestoreProperties
- Msvm_SyntheticFcPort.InstanceID
- Msvm_SyntheticFcPort.Caption
- Msvm_SyntheticFcPort.Description
- Msvm_SyntheticFcPort.ElementName
- Msvm_SyntheticFcPort.InstallDate
- Msvm_SyntheticFcPort.Name
- Msvm_SyntheticFcPort.OperationalStatus
- Msvm_SyntheticFcPort.StatusDescriptions
- Msvm_SyntheticFcPort.Status
- Msvm_SyntheticFcPort.HealthState
- Msvm_SyntheticFcPort.CommunicationStatus
- Msvm_SyntheticFcPort.DetailedStatus
- Msvm_SyntheticFcPort.OperatingStatus
- Msvm_SyntheticFcPort.PrimaryStatus
- Msvm_SyntheticFcPort.EnabledState
- Msvm_SyntheticFcPort.OtherEnabledState
- Msvm_SyntheticFcPort.RequestedState
- Msvm_SyntheticFcPort.EnabledDefault
- Msvm_SyntheticFcPort.TimeOfLastStateChange
- Msvm_SyntheticFcPort.AvailableRequestedStates
- Msvm_SyntheticFcPort.TransitioningToState
- Msvm_SyntheticFcPort.SystemCreationClassName
- Msvm_SyntheticFcPort.SystemName
- Msvm_SyntheticFcPort.CreationClassName
- Msvm_SyntheticFcPort.DeviceID
- Msvm_SyntheticFcPort.PowerManagementSupported
- Msvm_SyntheticFcPort.PowerManagementCapabilities
- Msvm_SyntheticFcPort.Availability
- Msvm_SyntheticFcPort.StatusInfo
- Msvm_SyntheticFcPort.LastErrorCode
- Msvm_SyntheticFcPort.ErrorDescription
- Msvm_SyntheticFcPort.ErrorCleared
- Msvm_SyntheticFcPort.OtherIdentifyingInfo
- Msvm_SyntheticFcPort.PowerOnHours
- Msvm_SyntheticFcPort.TotalPowerOnHours
- Msvm_SyntheticFcPort.IdentifyingDescriptions
- Msvm_SyntheticFcPort.AdditionalAvailability
- Msvm_SyntheticFcPort.MaxQuiesceTime
- Msvm_SyntheticFcPort.Speed
- Msvm_SyntheticFcPort.MaxSpeed
- Msvm_SyntheticFcPort.RequestedSpeed
- Msvm_SyntheticFcPort.UsageRestriction
- Msvm_SyntheticFcPort.PortType
- Msvm_SyntheticFcPort.OtherPortType
- Msvm_SyntheticFcPort.OtherNetworkPortType
- Msvm_SyntheticFcPort.PortNumber
- Msvm_SyntheticFcPort.LinkTechnology
- Msvm_SyntheticFcPort.OtherLinkTechnology
- Msvm_SyntheticFcPort.PermanentAddress
- Msvm_SyntheticFcPort.NetworkAddresses
- Msvm_SyntheticFcPort.FullDuplex
- Msvm_SyntheticFcPort.AutoSense
- Msvm_SyntheticFcPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticFcPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticFcPort.SupportedCOS
- Msvm_SyntheticFcPort.ActiveCOS
- Msvm_SyntheticFcPort.SupportedFC4Types
- Msvm_SyntheticFcPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f28614a7c885c0cfc03d546219518cda240219a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128427"
---
# <a name="msvm_syntheticfcport-class"></a><span data-ttu-id="48027-103">\_Classe MSVM SyntheticFcPort</span><span class="sxs-lookup"><span data-stu-id="48027-103">Msvm\_SyntheticFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="48027-104">Questo articolo contiene riferimenti al termine slave, che Microsoft non usa più.</span><span class="sxs-lookup"><span data-stu-id="48027-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="48027-105">Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.</span><span class="sxs-lookup"><span data-stu-id="48027-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="48027-106">Rappresenta una porta Fibre Channel sintetica.</span><span class="sxs-lookup"><span data-stu-id="48027-106">Represents a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="48027-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="48027-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="48027-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48027-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPort : CIM_FCPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 4;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint16   SupportedCOS[];
  uint16   ActiveCOS[];
  uint16   SupportedFC4Types[];
  uint16   ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="48027-109">Members</span><span class="sxs-lookup"><span data-stu-id="48027-109">Members</span></span>

<span data-ttu-id="48027-110">La **classe \_ SyntheticFcPort di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="48027-110">The **Msvm\_SyntheticFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="48027-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="48027-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="48027-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48027-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="48027-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="48027-113">Methods</span></span>

<span data-ttu-id="48027-114">La **classe \_ SyntheticFcPort di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="48027-114">The **Msvm\_SyntheticFcPort** class has these methods.</span></span>



| <span data-ttu-id="48027-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="48027-115">Method</span></span>                                                                | <span data-ttu-id="48027-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48027-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="48027-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="48027-117">**EnableDevice**</span></span>                                                      | <span data-ttu-id="48027-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="48027-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="48027-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="48027-119">**OnlineDevice**</span></span>                                                      | <span data-ttu-id="48027-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="48027-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="48027-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="48027-121">**QuiesceDevice**</span></span>                                                     | <span data-ttu-id="48027-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="48027-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="48027-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="48027-123">**RequestStateChange**</span></span>](msvm-syntheticfcport-requeststatechange.md) | <span data-ttu-id="48027-124">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="48027-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="48027-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="48027-125">**Reset**</span></span>](msvm-syntheticfcport-reset.md)                           | <span data-ttu-id="48027-126">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="48027-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="48027-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="48027-127">**RestoreProperties**</span></span>                                                 | <span data-ttu-id="48027-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="48027-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="48027-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="48027-129">**SaveProperties**</span></span>                                                    | <span data-ttu-id="48027-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="48027-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="48027-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="48027-131">**SetPowerState**</span></span>                                                     | <span data-ttu-id="48027-132">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="48027-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="48027-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48027-133">Properties</span></span>

<span data-ttu-id="48027-134">La **classe \_ SyntheticFcPort di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="48027-134">The **Msvm\_SyntheticFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48027-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="48027-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-136">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-138">Matrice di Integer che indica le classi del servizio attive.</span><span class="sxs-lookup"><span data-stu-id="48027-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="48027-139">I COS supportati sono specificati dalla proprietà **SupportedCOS** .</span><span class="sxs-lookup"><span data-stu-id="48027-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="48027-140">Questa proprietà viene ereditata da **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="48027-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="48027-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="48027-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48027-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="48027-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="48027-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="48027-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="48027-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="48027-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="48027-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="48027-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="48027-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="48027-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="48027-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="48027-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="48027-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="48027-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48027-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="48027-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-150">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-152">Matrice di numeri interi che indica il Fibre Channel i protocolli FC-4 attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="48027-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="48027-153">Un elenco di tutti i protocolli supportati viene specificato dalla proprietà **SupportedFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="48027-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="48027-154">Questa proprietà viene ereditata da **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="48027-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="48027-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="48027-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48027-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="48027-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="48027-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="48027-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="48027-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP su FC** (5)</span><span class="sxs-lookup"><span data-stu-id="48027-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="48027-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="48027-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="48027-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="48027-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="48027-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="48027-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="48027-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 slave** (18)</span><span class="sxs-lookup"><span data-stu-id="48027-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="48027-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 peer** (19)</span><span class="sxs-lookup"><span data-stu-id="48027-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="48027-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="48027-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="48027-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 slave** (22)</span><span class="sxs-lookup"><span data-stu-id="48027-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="48027-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 peer** (23)</span><span class="sxs-lookup"><span data-stu-id="48027-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="48027-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canale SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="48027-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="48027-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unità di controllo SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="48027-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="48027-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canale FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="48027-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="48027-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unità di controllo FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="48027-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="48027-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Servizi di Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="48027-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="48027-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="48027-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="48027-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="48027-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="48027-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="48027-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="48027-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controllo BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="48027-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="48027-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI incapsulato LAN PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="48027-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="48027-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Rete LAN incapsulata BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="48027-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="48027-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="48027-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="48027-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="48027-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="48027-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Fornitore univoco** (255)</span><span class="sxs-lookup"><span data-stu-id="48027-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48027-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="48027-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-182">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48027-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48027-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48027-184">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="48027-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="48027-185">Unità di trasmissione massima (MTU) attiva o negoziata che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="48027-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="48027-186">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="48027-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="48027-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="48027-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-188">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-190">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48027-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="48027-191">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-192">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="48027-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-193">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="48027-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48027-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-195">Indica se la porta è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato.</span><span class="sxs-lookup"><span data-stu-id="48027-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="48027-196">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="48027-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="48027-197">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="48027-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-198">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-200">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48027-200">The primary availability and status of the device.</span></span> <span data-ttu-id="48027-201">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="48027-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-203">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-205">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="48027-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="48027-206">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="48027-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="48027-207">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="48027-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-210">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="48027-210">A short description of the object.</span></span> <span data-ttu-id="48027-211">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="48027-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="48027-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="48027-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-213">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-215">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="48027-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="48027-216">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="48027-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="48027-217">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="48027-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="48027-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="48027-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48027-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="48027-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="48027-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="48027-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="48027-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="48027-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="48027-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="48027-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="48027-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="48027-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="48027-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="48027-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="48027-225">)</span><span class="sxs-lookup"><span data-stu-id="48027-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48027-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="48027-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-229">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="48027-229">The scoping system's creation class name.</span></span> <span data-ttu-id="48027-230">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="48027-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="48027-231">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="48027-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-234">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="48027-234">A description of the object.</span></span> <span data-ttu-id="48027-235">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="48027-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="48027-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="48027-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-237">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-239">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="48027-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="48027-240">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="48027-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="48027-241">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="48027-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="48027-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="48027-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48027-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="48027-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="48027-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="48027-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="48027-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="48027-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="48027-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="48027-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="48027-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="48027-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="48027-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="48027-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="48027-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="48027-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="48027-250">)</span><span class="sxs-lookup"><span data-stu-id="48027-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48027-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="48027-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-254">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="48027-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="48027-255">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="48027-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="48027-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="48027-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-259">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="48027-259">A display name for the object.</span></span> <span data-ttu-id="48027-260">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="48027-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="48027-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="48027-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-262">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-264">Configurazione predefinita o di avvio di un amministratore per la proprietà **EnabledState** di un elemento.</span><span class="sxs-lookup"><span data-stu-id="48027-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="48027-265">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="48027-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="48027-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="48027-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-267">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-269">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="48027-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="48027-270">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="48027-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="48027-271">Valore</span><span class="sxs-lookup"><span data-stu-id="48027-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="48027-272">Significato</span><span class="sxs-lookup"><span data-stu-id="48027-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="48027-273"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="48027-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="48027-274">Non è stato possibile determinare lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="48027-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="48027-275"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="48027-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="48027-276"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="48027-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="48027-277">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="48027-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="48027-278"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="48027-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="48027-279">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="48027-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="48027-280"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="48027-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="48027-281">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="48027-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="48027-282"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="48027-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="48027-283">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="48027-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="48027-284"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="48027-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="48027-285">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="48027-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="48027-286"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="48027-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="48027-287">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="48027-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="48027-288"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="48027-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="48027-289">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="48027-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="48027-290"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="48027-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="48027-291">L'elemento è abilitato ma in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="48027-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="48027-292">Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="48027-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="48027-293">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="48027-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="48027-294"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="48027-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="48027-295">L'elemento è in corso di attivazione dello stato abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="48027-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="48027-296">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="48027-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="48027-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="48027-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-298">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="48027-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48027-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-300">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="48027-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="48027-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="48027-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-305">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="48027-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="48027-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="48027-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-308">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="48027-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48027-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-310">Indica se la porta funziona in modalità full duplex.</span><span class="sxs-lookup"><span data-stu-id="48027-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="48027-311">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="48027-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="48027-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="48027-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-313">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-315">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="48027-315">The current health of the element.</span></span> <span data-ttu-id="48027-316">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="48027-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="48027-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="48027-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-318">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="48027-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-320">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="48027-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="48027-321">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="48027-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-323">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="48027-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="48027-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-325">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="48027-325">The date and time when the object was installed.</span></span> <span data-ttu-id="48027-326">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="48027-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="48027-327">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="48027-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="48027-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="48027-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-329">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48027-331">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="48027-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="48027-332">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="48027-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="48027-333">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="48027-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="48027-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="48027-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-335">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48027-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48027-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-337">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="48027-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="48027-338">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-339">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="48027-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-340">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-342">Specifica il tipo di tecnologia di collegamento per la porta.</span><span class="sxs-lookup"><span data-stu-id="48027-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="48027-343">Quando è impostata su 1 (other), la proprietà **OtherLinkTechnology** contiene una descrizione di stringa del tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="48027-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="48027-344">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="48027-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="48027-345">Valore</span><span class="sxs-lookup"><span data-stu-id="48027-345">Value</span></span>                                                                                                                                                                              | <span data-ttu-id="48027-346">Significato</span><span class="sxs-lookup"><span data-stu-id="48027-346">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC"></span><span id="fc"></span><dl> <span data-ttu-id="48027-347"><dt>**FC**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="48027-347"><dt>**FC**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="48027-348">Fibre Channel</span><span class="sxs-lookup"><span data-stu-id="48027-348">Fibre channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="48027-349">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="48027-349">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-350">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48027-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48027-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-352">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="48027-352">This property has been deprecated.</span></span> <span data-ttu-id="48027-353">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-354">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="48027-354">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-355">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48027-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48027-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48027-357">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="48027-357">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="48027-358">Larghezza di banda massima della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="48027-358">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="48027-359">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48027-359">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="48027-360">**Nome**</span><span class="sxs-lookup"><span data-stu-id="48027-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-361">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-363">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="48027-363">The label by which the object is known.</span></span> <span data-ttu-id="48027-364">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="48027-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="48027-365">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="48027-365">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-366">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="48027-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48027-368">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="48027-368">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="48027-369">Matrice di stringhe che contengono gli indirizzi MAC per la porta.</span><span class="sxs-lookup"><span data-stu-id="48027-369">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="48027-370">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="48027-370">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="48027-371">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="48027-371">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-372">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-374">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="48027-374">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="48027-375">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="48027-375">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="48027-376">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="48027-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="48027-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="48027-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48027-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="48027-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="48027-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="48027-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="48027-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="48027-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="48027-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="48027-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="48027-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="48027-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="48027-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="48027-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="48027-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="48027-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="48027-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="48027-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="48027-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="48027-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="48027-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="48027-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="48027-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="48027-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="48027-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="48027-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="48027-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="48027-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="48027-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="48027-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="48027-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="48027-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="48027-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="48027-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="48027-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="48027-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="48027-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="48027-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="48027-396">)</span><span class="sxs-lookup"><span data-stu-id="48027-396">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48027-397">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="48027-397">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-398">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-400">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="48027-400">The current statuses of the object.</span></span> <span data-ttu-id="48027-401">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="48027-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="48027-402">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="48027-402">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-403">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-405">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="48027-405">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="48027-406">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="48027-406">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="48027-407">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="48027-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="48027-408">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="48027-408">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-409">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="48027-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-411">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="48027-411">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="48027-412">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-413">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="48027-413">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-414">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-416">Valore stringa che descrive **LinkTechnology** quando è impostato su 1, (other).</span><span class="sxs-lookup"><span data-stu-id="48027-416">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="48027-417">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="48027-417">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="48027-418">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="48027-418">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-419">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-420">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-421">L'utilizzo di questa proprietà è deprecato al posto della proprietà **portType** .</span><span class="sxs-lookup"><span data-stu-id="48027-421">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="48027-422">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="48027-422">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="48027-423">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="48027-423">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-424">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-426">Descrive il tipo di modulo, quando **portType** è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="48027-426">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="48027-427">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48027-427">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="48027-428">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="48027-428">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-429">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48027-431">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="48027-431">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="48027-432">Indirizzo di rete hardcoded in una porta.</span><span class="sxs-lookup"><span data-stu-id="48027-432">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="48027-433">Questo indirizzo hardcoded può essere modificato usando un aggiornamento del firmware o una configurazione software.</span><span class="sxs-lookup"><span data-stu-id="48027-433">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="48027-434">Quando questa modifica viene apportata, il campo deve essere aggiornato nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="48027-434">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="48027-435">Questa proprietà deve essere **null** se non esiste alcun indirizzo hardcoded per la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="48027-435">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="48027-436">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="48027-436">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="48027-437">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="48027-437">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-438">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-439">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-440">Il numero della porta.</span><span class="sxs-lookup"><span data-stu-id="48027-440">The port number.</span></span> <span data-ttu-id="48027-441">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="48027-441">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="48027-442">**PortType**</span><span class="sxs-lookup"><span data-stu-id="48027-442">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-443">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-444">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-445">Modalità specifica attualmente abilitata per la porta.</span><span class="sxs-lookup"><span data-stu-id="48027-445">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="48027-446">Quando è impostata su 1 (other), la proprietà **OtherPortType** correlata contiene una descrizione di stringa del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="48027-446">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="48027-447">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48027-447">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="48027-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="48027-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48027-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="48027-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="48027-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 rame 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="48027-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="48027-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="48027-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="48027-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="48027-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="48027-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="48027-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="48027-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="48027-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="48027-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="48027-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="48027-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="48027-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="48027-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="48027-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="48027-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="48027-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="48027-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="48027-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="48027-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="48027-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="48027-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="48027-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="48027-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="48027-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="48027-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="48027-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="48027-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="48027-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="48027-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="48027-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="48027-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="48027-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="48027-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="48027-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="48027-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="48027-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="48027-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="48027-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48027-470">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="48027-470">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-471">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-471">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-473">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48027-473">The power management capabilities of the device.</span></span> <span data-ttu-id="48027-474">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-474">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-475">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="48027-475">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-476">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="48027-476">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48027-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-478">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="48027-478">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="48027-479">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-479">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-480">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="48027-480">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-481">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48027-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48027-482">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-483">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="48027-483">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="48027-484">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-485">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="48027-485">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-486">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-488">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="48027-488">Provides high level status information.</span></span> <span data-ttu-id="48027-489">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="48027-489">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="48027-490">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="48027-490">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="48027-491">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="48027-491">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="48027-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="48027-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48027-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="48027-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="48027-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="48027-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="48027-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="48027-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="48027-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="48027-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="48027-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="48027-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="48027-498">)</span><span class="sxs-lookup"><span data-stu-id="48027-498">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48027-499">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="48027-499">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-500">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48027-500">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48027-501">Tipo di accesso: sola scrittura</span><span class="sxs-lookup"><span data-stu-id="48027-501">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="48027-502">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="48027-502">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="48027-503">Larghezza di banda richiesta della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="48027-503">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="48027-504">La larghezza di banda effettiva viene segnalata nella proprietà **velocità** .</span><span class="sxs-lookup"><span data-stu-id="48027-504">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="48027-505">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48027-505">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="48027-506">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="48027-506">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-507">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-507">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-508">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-509">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="48027-509">The last requested or desired state for the element.</span></span> <span data-ttu-id="48027-510">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="48027-510">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="48027-511">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="48027-511">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-512">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48027-512">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48027-513">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48027-514">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="48027-514">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="48027-515">Larghezza di banda della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="48027-515">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="48027-516">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48027-516">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="48027-517">**Status**</span><span class="sxs-lookup"><span data-stu-id="48027-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-518">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-520">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="48027-520">The current status of the object.</span></span> <span data-ttu-id="48027-521">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-521">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-522">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="48027-522">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-523">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="48027-523">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-524">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-524">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-525">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="48027-525">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="48027-526">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="48027-526">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="48027-527">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="48027-527">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-528">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-529">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-530">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="48027-530">The current state of the logical device.</span></span> <span data-ttu-id="48027-531">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-531">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-532">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="48027-532">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-533">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-533">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-534">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-535">Matrice di Integer che indica le classi di Fibre Channel di servizio (COS) supportate.</span><span class="sxs-lookup"><span data-stu-id="48027-535">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="48027-536">Il COS attivo viene specificato dalla proprietà **ActiveCOS** .</span><span class="sxs-lookup"><span data-stu-id="48027-536">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="48027-537">Questa proprietà viene ereditata da **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="48027-537">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="48027-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="48027-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48027-539"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="48027-539"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="48027-540"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="48027-540"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="48027-541"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="48027-541"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="48027-542"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="48027-542"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="48027-543"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="48027-543"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="48027-544"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="48027-544"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="48027-545"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="48027-545"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48027-546">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="48027-546">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-547">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-547">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48027-548">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-549">Matrice di Integer che indica i protocolli Fibre Channel FC-4 supportati.</span><span class="sxs-lookup"><span data-stu-id="48027-549">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="48027-550">I protocolli attivi e in esecuzione sono specificati dalla proprietà **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="48027-550">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="48027-551">Questa proprietà viene ereditata da **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="48027-551">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="48027-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="48027-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48027-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="48027-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="48027-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="48027-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="48027-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP su FC** (5)</span><span class="sxs-lookup"><span data-stu-id="48027-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="48027-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="48027-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="48027-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="48027-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="48027-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="48027-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="48027-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 slave** (18)</span><span class="sxs-lookup"><span data-stu-id="48027-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="48027-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 peer** (19)</span><span class="sxs-lookup"><span data-stu-id="48027-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="48027-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="48027-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="48027-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 slave** (22)</span><span class="sxs-lookup"><span data-stu-id="48027-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="48027-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 peer** (23)</span><span class="sxs-lookup"><span data-stu-id="48027-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="48027-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canale SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="48027-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="48027-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unità di controllo SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="48027-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="48027-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canale FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="48027-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="48027-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unità di controllo FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="48027-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="48027-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Servizi di Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="48027-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="48027-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="48027-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="48027-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="48027-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="48027-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="48027-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="48027-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controllo BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="48027-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="48027-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI incapsulato LAN PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="48027-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="48027-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Rete LAN incapsulata BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="48027-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="48027-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="48027-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="48027-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="48027-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="48027-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Fornitore univoco** (255)</span><span class="sxs-lookup"><span data-stu-id="48027-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48027-578">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="48027-578">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-579">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48027-579">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48027-580">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48027-581">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="48027-581">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="48027-582">Unità di trasmissione massima (MTU) che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="48027-582">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="48027-583">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="48027-583">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="48027-584">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="48027-584">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-585">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-586">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-587">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="48027-587">The scoping system's creation class name.</span></span> <span data-ttu-id="48027-588">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="48027-588">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="48027-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="48027-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-590">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="48027-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48027-591">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-592">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="48027-592">The scoping system's name.</span></span> <span data-ttu-id="48027-593">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="48027-593">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="48027-594">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="48027-594">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-595">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="48027-595">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="48027-596">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-596">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-597">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="48027-597">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="48027-598">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="48027-598">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="48027-599">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="48027-599">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-600">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48027-600">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48027-601">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-601">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-602">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="48027-602">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="48027-603">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="48027-603">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48027-604">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="48027-604">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-605">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-605">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-606">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-607">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="48027-607">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="48027-608">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="48027-608">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="48027-609">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="48027-609">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48027-610">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48027-610">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48027-611">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48027-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48027-612">In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="48027-612">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="48027-613">Un esempio di questa situazione è costituito da un array di archiviazione che può avere porte back-end per comunicare con le unità disco e le porte front-end per comunicare con gli host.</span><span class="sxs-lookup"><span data-stu-id="48027-613">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="48027-614">Se non esiste alcuna restrizione sull'uso della porta, il valore deve essere impostato su 4 (senza restrizioni).</span><span class="sxs-lookup"><span data-stu-id="48027-614">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="48027-615">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48027-615">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="48027-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="48027-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48027-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="48027-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="48027-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="48027-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="48027-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Senza restrizioni** (4)</span><span class="sxs-lookup"><span data-stu-id="48027-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48027-620">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48027-620">Requirements</span></span>



| <span data-ttu-id="48027-621">Requisito</span><span class="sxs-lookup"><span data-stu-id="48027-621">Requirement</span></span> | <span data-ttu-id="48027-622">Valore</span><span class="sxs-lookup"><span data-stu-id="48027-622">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48027-623">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48027-623">Minimum supported client</span></span><br/> | <span data-ttu-id="48027-624">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="48027-624">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="48027-625">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48027-625">Minimum supported server</span></span><br/> | <span data-ttu-id="48027-626">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="48027-626">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="48027-627">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="48027-627">Namespace</span></span><br/>                | <span data-ttu-id="48027-628">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="48027-628">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="48027-629">MOF</span><span class="sxs-lookup"><span data-stu-id="48027-629">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48027-630"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48027-630"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48027-631">DLL</span><span class="sxs-lookup"><span data-stu-id="48027-631">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48027-632"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48027-632"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

