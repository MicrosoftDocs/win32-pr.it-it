---
description: Rappresenta una porta di Fibre Channel esterna.
ms.assetid: bab3a243-5ebd-43e0-948e-ea8112e09d0a
title: Classe Msvm_ExternalFcPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalFcPort
- Msvm_ExternalFcPort.SetPowerState
- Msvm_ExternalFcPort.EnableDevice
- Msvm_ExternalFcPort.OnlineDevice
- Msvm_ExternalFcPort.QuiesceDevice
- Msvm_ExternalFcPort.SaveProperties
- Msvm_ExternalFcPort.RestoreProperties
- Msvm_ExternalFcPort.InstanceID
- Msvm_ExternalFcPort.Caption
- Msvm_ExternalFcPort.Description
- Msvm_ExternalFcPort.ElementName
- Msvm_ExternalFcPort.InstallDate
- Msvm_ExternalFcPort.Name
- Msvm_ExternalFcPort.OperationalStatus
- Msvm_ExternalFcPort.StatusDescriptions
- Msvm_ExternalFcPort.Status
- Msvm_ExternalFcPort.HealthState
- Msvm_ExternalFcPort.CommunicationStatus
- Msvm_ExternalFcPort.DetailedStatus
- Msvm_ExternalFcPort.OperatingStatus
- Msvm_ExternalFcPort.PrimaryStatus
- Msvm_ExternalFcPort.EnabledState
- Msvm_ExternalFcPort.OtherEnabledState
- Msvm_ExternalFcPort.RequestedState
- Msvm_ExternalFcPort.EnabledDefault
- Msvm_ExternalFcPort.TimeOfLastStateChange
- Msvm_ExternalFcPort.AvailableRequestedStates
- Msvm_ExternalFcPort.TransitioningToState
- Msvm_ExternalFcPort.SystemCreationClassName
- Msvm_ExternalFcPort.SystemName
- Msvm_ExternalFcPort.CreationClassName
- Msvm_ExternalFcPort.DeviceID
- Msvm_ExternalFcPort.PowerManagementSupported
- Msvm_ExternalFcPort.PowerManagementCapabilities
- Msvm_ExternalFcPort.Availability
- Msvm_ExternalFcPort.StatusInfo
- Msvm_ExternalFcPort.LastErrorCode
- Msvm_ExternalFcPort.ErrorDescription
- Msvm_ExternalFcPort.ErrorCleared
- Msvm_ExternalFcPort.OtherIdentifyingInfo
- Msvm_ExternalFcPort.PowerOnHours
- Msvm_ExternalFcPort.TotalPowerOnHours
- Msvm_ExternalFcPort.IdentifyingDescriptions
- Msvm_ExternalFcPort.AdditionalAvailability
- Msvm_ExternalFcPort.MaxQuiesceTime
- Msvm_ExternalFcPort.Speed
- Msvm_ExternalFcPort.MaxSpeed
- Msvm_ExternalFcPort.RequestedSpeed
- Msvm_ExternalFcPort.UsageRestriction
- Msvm_ExternalFcPort.PortType
- Msvm_ExternalFcPort.OtherPortType
- Msvm_ExternalFcPort.OtherNetworkPortType
- Msvm_ExternalFcPort.PortNumber
- Msvm_ExternalFcPort.LinkTechnology
- Msvm_ExternalFcPort.OtherLinkTechnology
- Msvm_ExternalFcPort.PermanentAddress
- Msvm_ExternalFcPort.NetworkAddresses
- Msvm_ExternalFcPort.FullDuplex
- Msvm_ExternalFcPort.AutoSense
- Msvm_ExternalFcPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalFcPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalFcPort.SupportedCOS
- Msvm_ExternalFcPort.ActiveCOS
- Msvm_ExternalFcPort.SupportedFC4Types
- Msvm_ExternalFcPort.ActiveFC4Types
- Msvm_ExternalFcPort.IsHyperVCapable
- Msvm_ExternalFcPort.WWNN
- Msvm_ExternalFcPort.WWPN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f883afd2447c90c3167e8cf3145f8fd50ef2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307925"
---
# <a name="msvm_externalfcport-class"></a><span data-ttu-id="bec35-103">\_Classe MSVM ExternalFcPort</span><span class="sxs-lookup"><span data-stu-id="bec35-103">Msvm\_ExternalFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="bec35-104">Questo articolo contiene riferimenti al termine slave, che Microsoft non usa più.</span><span class="sxs-lookup"><span data-stu-id="bec35-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="bec35-105">Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.</span><span class="sxs-lookup"><span data-stu-id="bec35-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="bec35-106">Rappresenta una porta di Fibre Channel esterna.</span><span class="sxs-lookup"><span data-stu-id="bec35-106">Represents an external Fibre Channel port.</span></span>

<span data-ttu-id="bec35-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bec35-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bec35-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bec35-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalFcPort : CIM_FCPort
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
  uint16   LinkTechnology;
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
  boolean  IsHyperVCapable;
  string   WWNN;
  string   WWPN;
};
```

## <a name="members"></a><span data-ttu-id="bec35-109">Members</span><span class="sxs-lookup"><span data-stu-id="bec35-109">Members</span></span>

<span data-ttu-id="bec35-110">La **classe \_ ExternalFcPort di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bec35-110">The **Msvm\_ExternalFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="bec35-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="bec35-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="bec35-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bec35-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bec35-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="bec35-113">Methods</span></span>

<span data-ttu-id="bec35-114">La **classe \_ ExternalFcPort di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bec35-114">The **Msvm\_ExternalFcPort** class has these methods.</span></span>



| <span data-ttu-id="bec35-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="bec35-115">Method</span></span>                                                               | <span data-ttu-id="bec35-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bec35-116">Description</span></span>                              |
|:---------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="bec35-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="bec35-117">**EnableDevice**</span></span>                                                     | <span data-ttu-id="bec35-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bec35-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bec35-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="bec35-119">**OnlineDevice**</span></span>                                                     | <span data-ttu-id="bec35-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bec35-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bec35-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="bec35-121">**QuiesceDevice**</span></span>                                                    | <span data-ttu-id="bec35-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bec35-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="bec35-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="bec35-123">**RequestStateChange**</span></span>](msvm-externalfcport-requeststatechange.md) | <span data-ttu-id="bec35-124">Richiede una modifica dello stato</span><span class="sxs-lookup"><span data-stu-id="bec35-124">Requests a state change</span></span><br/>       |
| [<span data-ttu-id="bec35-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="bec35-125">**Reset**</span></span>](msvm-externalfcport-reset.md)                           | <span data-ttu-id="bec35-126">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="bec35-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="bec35-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="bec35-127">**RestoreProperties**</span></span>                                                | <span data-ttu-id="bec35-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bec35-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bec35-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="bec35-129">**SaveProperties**</span></span>                                                   | <span data-ttu-id="bec35-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bec35-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bec35-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bec35-131">**SetPowerState**</span></span>                                                    | <span data-ttu-id="bec35-132">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bec35-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bec35-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bec35-133">Properties</span></span>

<span data-ttu-id="bec35-134">La **classe \_ ExternalFcPort di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bec35-134">The **Msvm\_ExternalFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bec35-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="bec35-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-136">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-138">Matrice di Integer che indica le classi del servizio attive.</span><span class="sxs-lookup"><span data-stu-id="bec35-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="bec35-139">I COS supportati sono specificati dalla proprietà **SupportedCOS** .</span><span class="sxs-lookup"><span data-stu-id="bec35-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="bec35-140">Questa proprietà viene ereditata da **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="bec35-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="bec35-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="bec35-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="bec35-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="bec35-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="bec35-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="bec35-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="bec35-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="bec35-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="bec35-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-150">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-152">Matrice di numeri interi che indica il Fibre Channel i protocolli FC-4 attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bec35-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="bec35-153">Un elenco di tutti i protocolli supportati viene specificato dalla proprietà **SupportedFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="bec35-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="bec35-154">Questa proprietà viene ereditata da **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="bec35-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="bec35-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bec35-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="bec35-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP su FC** (5)</span><span class="sxs-lookup"><span data-stu-id="bec35-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="bec35-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="bec35-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="bec35-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 slave** (18)</span><span class="sxs-lookup"><span data-stu-id="bec35-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 peer** (19)</span><span class="sxs-lookup"><span data-stu-id="bec35-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="bec35-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 slave** (22)</span><span class="sxs-lookup"><span data-stu-id="bec35-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 peer** (23)</span><span class="sxs-lookup"><span data-stu-id="bec35-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canale SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="bec35-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unità di controllo SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="bec35-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canale FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="bec35-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unità di controllo FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="bec35-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Servizi di Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="bec35-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="bec35-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="bec35-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="bec35-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controllo BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="bec35-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI incapsulato LAN PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="bec35-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Rete LAN incapsulata BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="bec35-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="bec35-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="bec35-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Fornitore univoco** (255)</span><span class="sxs-lookup"><span data-stu-id="bec35-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="bec35-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-182">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bec35-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bec35-184">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="bec35-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bec35-185">Unità di trasmissione massima (MTU) attiva o negoziata che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="bec35-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="bec35-186">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bec35-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="bec35-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-188">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-190">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bec35-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="bec35-191">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-192">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="bec35-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-193">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bec35-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-195">Indica se la porta è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato.</span><span class="sxs-lookup"><span data-stu-id="bec35-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="bec35-196">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bec35-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-197">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="bec35-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-198">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-200">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bec35-200">The primary availability and status of the device.</span></span> <span data-ttu-id="bec35-201">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="bec35-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-203">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-205">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="bec35-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="bec35-206">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="bec35-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-207">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="bec35-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-210">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bec35-210">A short description of the object.</span></span> <span data-ttu-id="bec35-211">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="bec35-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-213">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-215">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="bec35-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="bec35-216">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="bec35-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bec35-217">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bec35-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="bec35-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="bec35-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="bec35-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="bec35-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bec35-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bec35-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bec35-225">)</span><span class="sxs-lookup"><span data-stu-id="bec35-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bec35-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-229">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="bec35-229">The scoping system's creation class name.</span></span> <span data-ttu-id="bec35-230">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="bec35-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-231">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="bec35-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-234">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="bec35-234">A description of the object.</span></span> <span data-ttu-id="bec35-235">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="bec35-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-237">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-239">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="bec35-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="bec35-240">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="bec35-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bec35-241">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bec35-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="bec35-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="bec35-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="bec35-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="bec35-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="bec35-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bec35-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bec35-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bec35-250">)</span><span class="sxs-lookup"><span data-stu-id="bec35-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bec35-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-254">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bec35-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="bec35-255">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="bec35-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bec35-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-259">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bec35-259">A display name for the object.</span></span> <span data-ttu-id="bec35-260">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="bec35-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-262">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-264">Configurazione predefinita o di avvio di un amministratore per la proprietà **EnabledState** di un elemento.</span><span class="sxs-lookup"><span data-stu-id="bec35-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="bec35-265">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="bec35-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="bec35-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-267">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-269">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="bec35-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="bec35-270">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bec35-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="bec35-271">Valore</span><span class="sxs-lookup"><span data-stu-id="bec35-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="bec35-272">Significato</span><span class="sxs-lookup"><span data-stu-id="bec35-272">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="bec35-273"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="bec35-274">Non è stato possibile determinare lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="bec35-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="bec35-275"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="bec35-276"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="bec35-277">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bec35-277">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="bec35-278"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="bec35-279">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="bec35-279">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="bec35-280"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="bec35-281">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bec35-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="bec35-282"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="bec35-283">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="bec35-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="bec35-284"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="bec35-285">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="bec35-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="bec35-286"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="bec35-287">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="bec35-287">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="bec35-288"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="bec35-289">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="bec35-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="bec35-290"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="bec35-291">L'elemento è abilitato, ma è in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="bec35-291">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="bec35-292">Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="bec35-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="bec35-293">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="bec35-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="bec35-294"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="bec35-295">L'elemento è in corso di attivazione dello stato abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="bec35-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="bec35-296">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="bec35-296">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="bec35-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="bec35-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-298">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bec35-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-300">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="bec35-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="bec35-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bec35-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-305">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="bec35-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="bec35-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="bec35-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-308">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bec35-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-310">Indica se la porta funziona in modalità full duplex.</span><span class="sxs-lookup"><span data-stu-id="bec35-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="bec35-311">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bec35-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="bec35-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-313">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-315">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="bec35-315">The current health of the element.</span></span> <span data-ttu-id="bec35-316">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bec35-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-318">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bec35-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-320">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="bec35-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="bec35-321">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bec35-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-323">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bec35-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-325">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bec35-325">The date and time when the object was installed.</span></span> <span data-ttu-id="bec35-326">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="bec35-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="bec35-327">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bec35-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-329">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bec35-331">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="bec35-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bec35-332">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="bec35-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="bec35-333">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-334">**IsHyperVCapable**</span><span class="sxs-lookup"><span data-stu-id="bec35-334">**IsHyperVCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-335">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bec35-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-337">Se questa proprietà è impostata su **true**, la porta Fibre Channel può essere connessa alle opzioni e pertanto può fornire connettività a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bec35-337">If this property is **True**, this Fibre Channel port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="bec35-338">Se questa proprietà è **false**, questa porta non può essere utilizzata dall'architettura Fibre Channel della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bec35-338">If this property is **False**, then this port cannot be used by the virtual machine Fibre Channel architecture.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-339">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bec35-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-340">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bec35-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-342">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bec35-342">The last error code reported by the logical device.</span></span> <span data-ttu-id="bec35-343">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-344">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="bec35-344">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-345">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-347">Specifica il tipo di tecnologia di collegamento per la porta.</span><span class="sxs-lookup"><span data-stu-id="bec35-347">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="bec35-348">Quando è impostata su 1 (other), la proprietà **OtherLinkTechnology** contiene una descrizione di stringa del tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="bec35-348">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="bec35-349">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bec35-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="bec35-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-351"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bec35-351"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-352"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="bec35-352"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-353"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="bec35-353"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-354"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="bec35-354"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-355"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="bec35-355"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-356"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="bec35-356"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-357"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="bec35-357"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-358"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="bec35-358"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-359"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarossi** (9)</span><span class="sxs-lookup"><span data-stu-id="bec35-359"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-360"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="bec35-360"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-361"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN wireless** (11)</span><span class="sxs-lookup"><span data-stu-id="bec35-361"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-362">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="bec35-362">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-363">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bec35-363">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-365">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="bec35-365">This property has been deprecated.</span></span> <span data-ttu-id="bec35-366">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-367">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="bec35-367">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-368">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bec35-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bec35-370">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="bec35-370">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="bec35-371">Larghezza di banda massima della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="bec35-371">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="bec35-372">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bec35-372">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-373">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bec35-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-376">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="bec35-376">The label by which the object is known.</span></span> <span data-ttu-id="bec35-377">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-378">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="bec35-378">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-379">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bec35-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bec35-381">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="bec35-381">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="bec35-382">Matrice di stringhe che contengono gli indirizzi MAC per la porta.</span><span class="sxs-lookup"><span data-stu-id="bec35-382">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="bec35-383">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bec35-383">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-384">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="bec35-384">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-385">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-385">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-386">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-387">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="bec35-387">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="bec35-388">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="bec35-388">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bec35-389">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bec35-390"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-390"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-391"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="bec35-391"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-392"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="bec35-392"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-393"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="bec35-393"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-394"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="bec35-394"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-395"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="bec35-395"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-396"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="bec35-396"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-397"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="bec35-397"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-398"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="bec35-398"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-399"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="bec35-399"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-400"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="bec35-400"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-401"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="bec35-401"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-402"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="bec35-402"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-403"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="bec35-403"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-404"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="bec35-404"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-405"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="bec35-405"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-406"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="bec35-406"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-407"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bec35-407"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-408"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bec35-408"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bec35-409">)</span><span class="sxs-lookup"><span data-stu-id="bec35-409">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-410">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="bec35-410">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-411">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-412">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-413">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bec35-413">The current statuses of the object.</span></span> <span data-ttu-id="bec35-414">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-415">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="bec35-415">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-416">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-417">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-418">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="bec35-418">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="bec35-419">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="bec35-419">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="bec35-420">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="bec35-420">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-421">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="bec35-421">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-422">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bec35-422">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-423">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-424">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bec35-424">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="bec35-425">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-425">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-426">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="bec35-426">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-427">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-429">Valore stringa che descrive **LinkTechnology** quando è impostato su 1, (other).</span><span class="sxs-lookup"><span data-stu-id="bec35-429">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="bec35-430">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bec35-430">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-431">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="bec35-431">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-432">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-433">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-434">L'utilizzo di questa proprietà è deprecato al posto della proprietà **portType** .</span><span class="sxs-lookup"><span data-stu-id="bec35-434">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="bec35-435">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bec35-435">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-436">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="bec35-436">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-437">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-438">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-439">Descrive il tipo di modulo, quando **portType** è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="bec35-439">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="bec35-440">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bec35-440">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-441">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="bec35-441">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-442">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-443">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bec35-444">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="bec35-444">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="bec35-445">Indirizzo di rete hardcoded in una porta.</span><span class="sxs-lookup"><span data-stu-id="bec35-445">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="bec35-446">Questo indirizzo hardcoded può essere modificato usando un aggiornamento del firmware o una configurazione software.</span><span class="sxs-lookup"><span data-stu-id="bec35-446">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="bec35-447">Quando questa modifica viene apportata, il campo deve essere aggiornato nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="bec35-447">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="bec35-448">Questa proprietà deve essere **null** se non esiste alcun indirizzo hardcoded per la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="bec35-448">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="bec35-449">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bec35-449">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-450">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="bec35-450">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-451">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-452">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-453">Il numero della porta.</span><span class="sxs-lookup"><span data-stu-id="bec35-453">The port number.</span></span> <span data-ttu-id="bec35-454">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bec35-454">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-455">**PortType**</span><span class="sxs-lookup"><span data-stu-id="bec35-455">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-456">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-457">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-458">Modalità specifica attualmente abilitata per la porta.</span><span class="sxs-lookup"><span data-stu-id="bec35-458">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="bec35-459">Quando è impostata su 1 (other), la proprietà **OtherPortType** correlata contiene una descrizione di stringa del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="bec35-459">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="bec35-460">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bec35-460">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="bec35-461"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-461"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-462"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bec35-462"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-463"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 rame 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="bec35-463"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-464"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="bec35-464"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-465"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="bec35-465"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-466"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="bec35-466"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-467"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="bec35-467"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-468"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="bec35-468"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-469"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="bec35-469"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-470"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="bec35-470"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-471"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="bec35-471"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-472"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="bec35-472"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-473"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="bec35-473"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-474"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="bec35-474"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-475"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="bec35-475"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-476"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="bec35-476"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-477"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="bec35-477"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-478"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="bec35-478"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-479"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="bec35-479"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-480"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="bec35-480"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-481"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="bec35-481"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-482"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="bec35-482"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-483">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bec35-483">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-484">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-484">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-485">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-486">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bec35-486">The power management capabilities of the device.</span></span> <span data-ttu-id="bec35-487">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-488">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="bec35-488">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-489">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bec35-489">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-490">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-491">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="bec35-491">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="bec35-492">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-493">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="bec35-493">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-494">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bec35-494">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-495">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-496">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="bec35-496">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="bec35-497">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-498">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="bec35-498">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-499">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-499">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-500">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-501">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="bec35-501">Provides high level status information.</span></span> <span data-ttu-id="bec35-502">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="bec35-502">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="bec35-503">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="bec35-503">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bec35-504">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-504">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bec35-505"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-505"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-506"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="bec35-506"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-507"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="bec35-507"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-508"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="bec35-508"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-509"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bec35-509"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-510"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bec35-510"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bec35-511">)</span><span class="sxs-lookup"><span data-stu-id="bec35-511">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-512">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="bec35-512">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-513">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bec35-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-514">Tipo di accesso: sola scrittura</span><span class="sxs-lookup"><span data-stu-id="bec35-514">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="bec35-515">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="bec35-515">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="bec35-516">Larghezza di banda richiesta della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="bec35-516">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="bec35-517">La larghezza di banda effettiva viene segnalata nella proprietà **velocità** .</span><span class="sxs-lookup"><span data-stu-id="bec35-517">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="bec35-518">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bec35-518">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-519">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="bec35-519">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-520">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-521">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-522">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="bec35-522">The last requested or desired state for the element.</span></span> <span data-ttu-id="bec35-523">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="bec35-523">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-524">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="bec35-524">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-525">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bec35-525">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-526">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-526">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bec35-527">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="bec35-527">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="bec35-528">Larghezza di banda della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="bec35-528">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="bec35-529">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bec35-529">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-530">**Status**</span><span class="sxs-lookup"><span data-stu-id="bec35-530">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-531">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-532">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-533">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bec35-533">The current status of the object.</span></span> <span data-ttu-id="bec35-534">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-535">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bec35-535">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-536">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bec35-536">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-537">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-538">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="bec35-538">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="bec35-539">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bec35-539">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-540">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bec35-540">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-541">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-541">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-542">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-543">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bec35-543">The current state of the logical device.</span></span> <span data-ttu-id="bec35-544">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-544">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-545">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="bec35-545">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-546">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-546">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-547">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-547">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-548">Matrice di Integer che indica le classi di Fibre Channel di servizio (COS) supportate.</span><span class="sxs-lookup"><span data-stu-id="bec35-548">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="bec35-549">Il COS attivo viene specificato dalla proprietà **ActiveCOS** .</span><span class="sxs-lookup"><span data-stu-id="bec35-549">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="bec35-550">Questa proprietà viene ereditata da **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="bec35-550">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="bec35-551"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-551"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-552"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="bec35-552"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-553"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="bec35-553"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-554"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="bec35-554"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-555"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="bec35-555"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-556"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="bec35-556"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-557"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="bec35-557"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-558"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="bec35-558"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-559">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="bec35-559">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-560">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-560">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bec35-561">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-561">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-562">Matrice di Integer che indica i protocolli Fibre Channel FC-4 supportati.</span><span class="sxs-lookup"><span data-stu-id="bec35-562">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="bec35-563">I protocolli attivi e in esecuzione sono specificati dalla proprietà **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="bec35-563">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="bec35-564">Questa proprietà viene ereditata da **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="bec35-564">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="bec35-565"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-565"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-566"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bec35-566"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-567"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="bec35-567"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-568"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP su FC** (5)</span><span class="sxs-lookup"><span data-stu-id="bec35-568"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-569"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="bec35-569"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-570"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="bec35-570"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-571"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="bec35-571"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-572"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 slave** (18)</span><span class="sxs-lookup"><span data-stu-id="bec35-572"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-573"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 peer** (19)</span><span class="sxs-lookup"><span data-stu-id="bec35-573"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-574"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="bec35-574"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-575"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 slave** (22)</span><span class="sxs-lookup"><span data-stu-id="bec35-575"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-576"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 peer** (23)</span><span class="sxs-lookup"><span data-stu-id="bec35-576"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-577"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canale SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="bec35-577"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-578"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unità di controllo SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="bec35-578"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-579"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canale FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="bec35-579"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-580"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unità di controllo FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="bec35-580"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-581"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Servizi di Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="bec35-581"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-582"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="bec35-582"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-583"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="bec35-583"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-584"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="bec35-584"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-585"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controllo BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="bec35-585"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-586"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI incapsulato LAN PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="bec35-586"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-587"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Rete LAN incapsulata BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="bec35-587"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-588"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="bec35-588"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-589"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="bec35-589"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-590"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Fornitore univoco** (255)</span><span class="sxs-lookup"><span data-stu-id="bec35-590"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-591">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="bec35-591">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-592">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bec35-592">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-593">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bec35-594">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="bec35-594">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bec35-595">Unità di trasmissione massima (MTU) che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="bec35-595">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="bec35-596">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bec35-596">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-597">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bec35-597">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-598">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-599">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-599">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-600">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="bec35-600">The scoping system's creation class name.</span></span> <span data-ttu-id="bec35-601">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="bec35-601">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-602">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bec35-602">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-603">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-604">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-604">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-605">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="bec35-605">The scoping system's name.</span></span> <span data-ttu-id="bec35-606">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="bec35-606">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bec35-607">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="bec35-607">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-608">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bec35-608">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-609">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-609">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-610">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="bec35-610">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="bec35-611">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="bec35-611">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-612">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="bec35-612">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-613">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bec35-613">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-614">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-615">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="bec35-615">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="bec35-616">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bec35-616">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-617">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="bec35-617">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-618">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-618">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-619">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-619">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-620">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="bec35-620">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="bec35-621">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="bec35-621">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-622">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="bec35-622">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-623">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bec35-623">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-624">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-624">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-625">In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="bec35-625">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="bec35-626">Un esempio di questa situazione è costituito da un array di archiviazione che può avere porte back-end per comunicare con le unità disco e le porte front-end per comunicare con gli host.</span><span class="sxs-lookup"><span data-stu-id="bec35-626">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="bec35-627">Se non esiste alcuna restrizione sull'uso della porta, il valore deve essere impostato su 4 (senza restrizioni).</span><span class="sxs-lookup"><span data-stu-id="bec35-627">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="bec35-628">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bec35-628">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="bec35-629"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bec35-629"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-630"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="bec35-630"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-631"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="bec35-631"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bec35-632"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Senza restrizioni** (4)</span><span class="sxs-lookup"><span data-stu-id="bec35-632"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bec35-633">**WWNN**</span><span class="sxs-lookup"><span data-stu-id="bec35-633">**WWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-634">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-635">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-635">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-636">Nome del nodo universale per la porta Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="bec35-636">The world wide node name for this Fibre Channel port.</span></span>

</dd> <dt>

<span data-ttu-id="bec35-637">**WWPN**</span><span class="sxs-lookup"><span data-stu-id="bec35-637">**WWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bec35-638">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bec35-638">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bec35-639">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bec35-639">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bec35-640">Nome della porta universale per la porta Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="bec35-640">The world wide port name for this Fibre Channel port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bec35-641">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bec35-641">Requirements</span></span>



| <span data-ttu-id="bec35-642">Requisito</span><span class="sxs-lookup"><span data-stu-id="bec35-642">Requirement</span></span> | <span data-ttu-id="bec35-643">Valore</span><span class="sxs-lookup"><span data-stu-id="bec35-643">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec35-644">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bec35-644">Minimum supported client</span></span><br/> | <span data-ttu-id="bec35-645">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bec35-645">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bec35-646">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bec35-646">Minimum supported server</span></span><br/> | <span data-ttu-id="bec35-647">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bec35-647">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bec35-648">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bec35-648">Namespace</span></span><br/>                | <span data-ttu-id="bec35-649">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bec35-649">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bec35-650">MOF</span><span class="sxs-lookup"><span data-stu-id="bec35-650">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bec35-651"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-651"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bec35-652">DLL</span><span class="sxs-lookup"><span data-stu-id="bec35-652">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bec35-653"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bec35-653"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

