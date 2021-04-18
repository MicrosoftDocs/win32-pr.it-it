---
description: Rappresenta le funzionalità e la gestione di un dispositivo porta Fibre Channel (FC).
ms.assetid: 32a11971-9e18-410d-a3cd-4921a7e986f0
title: Classe CIM_FCPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FCPort
- CIM_FCPort.PortType
- CIM_FCPort.SupportedCOS
- CIM_FCPort.ActiveCOS
- CIM_FCPort.SupportedFC4Types
- CIM_FCPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6a858cbb4603743e1ddd11cac71500a9e39325a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305673"
---
# <a name="cim_fcport-class"></a><span data-ttu-id="3cacf-103">CIM \_ FCPort (classe)</span><span class="sxs-lookup"><span data-stu-id="3cacf-103">CIM\_FCPort class</span></span>

> [!NOTE]
> <span data-ttu-id="3cacf-104">Questo articolo contiene riferimenti al termine slave, che Microsoft non usa più.</span><span class="sxs-lookup"><span data-stu-id="3cacf-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="3cacf-105">Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.</span><span class="sxs-lookup"><span data-stu-id="3cacf-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="3cacf-106">Rappresenta le funzionalità e la gestione di un dispositivo porta Fibre Channel (FC).</span><span class="sxs-lookup"><span data-stu-id="3cacf-106">Represents the capabilities and management of a fibre channel (FC) port device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cacf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3cacf-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::FC"), AMENDMENT]
class CIM_FCPort : CIM_NetworkPort
{
  uint16 PortType;
  uint16 SupportedCOS[];
  uint16 ActiveCOS[];
  uint16 SupportedFC4Types[];
  uint16 ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="3cacf-108">Members</span><span class="sxs-lookup"><span data-stu-id="3cacf-108">Members</span></span>

> [!NOTE]
> <span data-ttu-id="3cacf-109">Questo articolo contiene riferimenti al termine slave, che Microsoft non usa più.</span><span class="sxs-lookup"><span data-stu-id="3cacf-109">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="3cacf-110">Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.</span><span class="sxs-lookup"><span data-stu-id="3cacf-110">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="3cacf-111">La classe **CIM \_ FCPort** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3cacf-111">The **CIM\_FCPort** class has these types of members:</span></span>

-   [<span data-ttu-id="3cacf-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3cacf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3cacf-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3cacf-113">Properties</span></span>

<span data-ttu-id="3cacf-114">La classe **CIM \_ FCPort** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3cacf-114">The **CIM\_FCPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3cacf-115">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="3cacf-115">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cacf-116">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3cacf-116">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3cacf-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3cacf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cacf-118">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ FCPort**.**SupportedCOS**")</span><span class="sxs-lookup"><span data-stu-id="3cacf-118">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedCOS**")</span></span>
</dt> </dl>

<span data-ttu-id="3cacf-119">Le impostazioni della classe attiva di Service (COS) per Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="3cacf-119">The active class of service (COS) settings for the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3cacf-120">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3cacf-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="3cacf-121">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="3cacf-121">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="3cacf-122">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="3cacf-122">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="3cacf-123">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="3cacf-123">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="3cacf-124">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="3cacf-124">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="3cacf-125">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="3cacf-125">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="3cacf-126">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="3cacf-126">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="3cacf-127">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="3cacf-127">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3cacf-128">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="3cacf-128">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cacf-129">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3cacf-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3cacf-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3cacf-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cacf-131">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ FCPort**.**SupportedFC4Types**")</span><span class="sxs-lookup"><span data-stu-id="3cacf-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedFC4Types**")</span></span>
</dt> </dl>

<span data-ttu-id="3cacf-132">Protocolli FC-4 in esecuzione sul Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="3cacf-132">The FC-4 protocols that are running on the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3cacf-133">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3cacf-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3cacf-134">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="3cacf-134">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="3cacf-135">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="3cacf-135">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="3cacf-136">**IP su FC** (5)</span><span class="sxs-lookup"><span data-stu-id="3cacf-136">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="3cacf-137">**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="3cacf-137">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="3cacf-138">**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="3cacf-138">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="3cacf-139">**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="3cacf-139">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="3cacf-140">**IPI-3 slave** (18)</span><span class="sxs-lookup"><span data-stu-id="3cacf-140">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="3cacf-141">**IPI-3 peer** (19)</span><span class="sxs-lookup"><span data-stu-id="3cacf-141">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="3cacf-142">**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="3cacf-142">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="3cacf-143">**CP IPI-3 slave** (22)</span><span class="sxs-lookup"><span data-stu-id="3cacf-143">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="3cacf-144">**CP IPI-3 peer** (23)</span><span class="sxs-lookup"><span data-stu-id="3cacf-144">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="3cacf-145">**Canale SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="3cacf-145">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="3cacf-146">**Unità di controllo SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="3cacf-146">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="3cacf-147">**Canale FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="3cacf-147">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="3cacf-148">**Unità di controllo FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="3cacf-148">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="3cacf-149">**Servizi di Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="3cacf-149">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="3cacf-150">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="3cacf-150">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="3cacf-151">**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="3cacf-151">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="3cacf-152">**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="3cacf-152">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="3cacf-153">**Controllo BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="3cacf-153">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="3cacf-154">**BBL FDDI incapsulato LAN PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="3cacf-154">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="3cacf-155">**Rete LAN incapsulata BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="3cacf-155">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="3cacf-156">**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="3cacf-156">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="3cacf-157">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="3cacf-157">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="3cacf-158">**Fornitore univoco** (255)</span><span class="sxs-lookup"><span data-stu-id="3cacf-158">**Vendor Unique** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3cacf-159">**PortType**</span><span class="sxs-lookup"><span data-stu-id="3cacf-159">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cacf-160">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3cacf-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3cacf-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3cacf-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cacf-162">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="3cacf-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="3cacf-163">Modalità abilitata per la porta.</span><span class="sxs-lookup"><span data-stu-id="3cacf-163">The enabled mode for the port.</span></span> <span data-ttu-id="3cacf-164">Le modalità porta sono definite dagli standard ANSI X3.</span><span class="sxs-lookup"><span data-stu-id="3cacf-164">The port modes are defined by ANSI X3 standards.</span></span> <span data-ttu-id="3cacf-165">Se la porta è stata connessa, questo sarà il tipo di porta negoziata. in caso contrario, verrà segnalato il tipo di porta configurata.</span><span class="sxs-lookup"><span data-stu-id="3cacf-165">If the port is logged in, this will be the negotiated port type, otherwise the configured port type will be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3cacf-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3cacf-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3cacf-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="3cacf-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3cacf-168">La proprietà correlata **OtherPortType** contiene una descrizione di stringa del tipo di porta</span><span class="sxs-lookup"><span data-stu-id="3cacf-168">The related property **OtherPortType** contains a string description of the type of port</span></span>

</dd> <dt>

<span id="N"></span><span id="n"></span>

<span data-ttu-id="3cacf-169"><span id="N"></span><span id="n"></span>**N** (10)</span><span class="sxs-lookup"><span data-stu-id="3cacf-169"><span id="N"></span><span id="n"></span>**N** (10)</span></span>


</dt> <dd>

<span data-ttu-id="3cacf-170">Porta del nodo</span><span class="sxs-lookup"><span data-stu-id="3cacf-170">Node Port</span></span>

</dd> <dt>

<span id="NL"></span><span id="nl"></span>

<span data-ttu-id="3cacf-171"><span id="NL"></span><span id="nl"></span>**Nl** (11)</span><span class="sxs-lookup"><span data-stu-id="3cacf-171"><span id="NL"></span><span id="nl"></span>**NL** (11)</span></span>


</dt> <dd>

<span data-ttu-id="3cacf-172">Porta del nodo che supporta il ciclo Arbitrated FC</span><span class="sxs-lookup"><span data-stu-id="3cacf-172">Node Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="F_NL"></span><span id="f_nl"></span>

<span data-ttu-id="3cacf-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span><span class="sxs-lookup"><span data-stu-id="3cacf-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>

<span data-ttu-id="3cacf-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**NX** (13)</span><span class="sxs-lookup"><span data-stu-id="3cacf-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**Nx** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3cacf-175">La porta può essere negoziata in modo che diventi una porta del nodo (N) o una porta del nodo che supporta FC Arbitrated Loop (NL)</span><span class="sxs-lookup"><span data-stu-id="3cacf-175">Port may negotiate to become either a node port (N) or a node port supporting FC arbitrated loop (NL)</span></span>

</dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="3cacf-176"><span id="E"></span><span id="e"></span>**E** (14)</span><span class="sxs-lookup"><span data-stu-id="3cacf-176"><span id="E"></span><span id="e"></span>**E** (14)</span></span>


</dt> <dd>

<span data-ttu-id="3cacf-177">Porta di espansione che connette gli elementi dell'infrastruttura (ad esempio, commutatori FC)</span><span class="sxs-lookup"><span data-stu-id="3cacf-177">Expansion Port connecting fabric elements (for example, FC switches)</span></span>

</dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="3cacf-178"><span id="F"></span><span id="f"></span>**F** (15)</span><span class="sxs-lookup"><span data-stu-id="3cacf-178"><span id="F"></span><span id="f"></span>**F** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3cacf-179">Porta Fabric (elemento)</span><span class="sxs-lookup"><span data-stu-id="3cacf-179">Fabric (element) Port</span></span>

</dd> <dt>

<span id="FL"></span><span id="fl"></span>

<span data-ttu-id="3cacf-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span><span class="sxs-lookup"><span data-stu-id="3cacf-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span></span>


</dt> <dd>

<span data-ttu-id="3cacf-181">Porta dell'infrastruttura (elemento) che supporta il ciclo FC Arbitrated</span><span class="sxs-lookup"><span data-stu-id="3cacf-181">Fabric (element) Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="3cacf-182"><span id="B"></span><span id="b"></span>**B** (17)</span><span class="sxs-lookup"><span data-stu-id="3cacf-182"><span id="B"></span><span id="b"></span>**B** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3cacf-183">Porta Bridge</span><span class="sxs-lookup"><span data-stu-id="3cacf-183">Bridge port</span></span>

</dd> <dt>

<span id="G"></span><span id="g"></span>

<span data-ttu-id="3cacf-184"><span id="G"></span><span id="g"></span>**G** (18)</span><span class="sxs-lookup"><span data-stu-id="3cacf-184"><span id="G"></span><span id="g"></span>**G** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3cacf-185">La porta può negoziare per diventare una porta di espansione (E) o una porta dell'infrastruttura (F)</span><span class="sxs-lookup"><span data-stu-id="3cacf-185">Port may negotiate to become either an expansion port (E), or a fabric port (F)</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3cacf-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="3cacf-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3cacf-187">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="3cacf-187">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cacf-188">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3cacf-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3cacf-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3cacf-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cacf-190">Le impostazioni della classe di servizio (COS) supportate dal Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="3cacf-190">The class of service (COS) settings that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3cacf-191">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3cacf-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="3cacf-192">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="3cacf-192">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="3cacf-193">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="3cacf-193">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="3cacf-194">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="3cacf-194">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="3cacf-195">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="3cacf-195">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="3cacf-196">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="3cacf-196">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="3cacf-197">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="3cacf-197">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="3cacf-198">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="3cacf-198">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3cacf-199">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="3cacf-199">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cacf-200">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3cacf-200">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3cacf-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3cacf-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cacf-202">Protocolli FC-4 supportati dal Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="3cacf-202">The FC-4 protocols that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3cacf-203">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3cacf-203">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3cacf-204">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="3cacf-204">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="3cacf-205">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="3cacf-205">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="3cacf-206">**IP su FC** (5)</span><span class="sxs-lookup"><span data-stu-id="3cacf-206">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="3cacf-207">**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="3cacf-207">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="3cacf-208">**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="3cacf-208">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="3cacf-209">**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="3cacf-209">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="3cacf-210">**IPI-3 slave** (18)</span><span class="sxs-lookup"><span data-stu-id="3cacf-210">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="3cacf-211">**IPI-3 peer** (19)</span><span class="sxs-lookup"><span data-stu-id="3cacf-211">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="3cacf-212">**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="3cacf-212">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="3cacf-213">**CP IPI-3 slave** (22)</span><span class="sxs-lookup"><span data-stu-id="3cacf-213">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="3cacf-214">**CP IPI-3 peer** (23)</span><span class="sxs-lookup"><span data-stu-id="3cacf-214">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="3cacf-215">**Canale SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="3cacf-215">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="3cacf-216">**Unità di controllo SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="3cacf-216">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="3cacf-217">**Canale FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="3cacf-217">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="3cacf-218">**Unità di controllo FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="3cacf-218">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="3cacf-219">**Servizi di Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="3cacf-219">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="3cacf-220">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="3cacf-220">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="3cacf-221">**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="3cacf-221">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="3cacf-222">**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="3cacf-222">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="3cacf-223">**Controllo BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="3cacf-223">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="3cacf-224">**BBL FDDI incapsulato LAN PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="3cacf-224">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="3cacf-225">**Rete LAN incapsulata BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="3cacf-225">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="3cacf-226">**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="3cacf-226">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="3cacf-227">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="3cacf-227">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="3cacf-228">**Fornitore univoco** (255)</span><span class="sxs-lookup"><span data-stu-id="3cacf-228">**Vendor Unique** (255)</span></span>


<span data-ttu-id="3cacf-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3cacf-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3cacf-230">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3cacf-230">Requirements</span></span>



| <span data-ttu-id="3cacf-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cacf-231">Requirement</span></span> | <span data-ttu-id="3cacf-232">Valore</span><span class="sxs-lookup"><span data-stu-id="3cacf-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cacf-233">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3cacf-233">Minimum supported client</span></span><br/> | <span data-ttu-id="3cacf-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3cacf-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3cacf-235">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3cacf-235">Minimum supported server</span></span><br/> | <span data-ttu-id="3cacf-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3cacf-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3cacf-237">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3cacf-237">Namespace</span></span><br/>                | <span data-ttu-id="3cacf-238">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3cacf-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3cacf-239">MOF</span><span class="sxs-lookup"><span data-stu-id="3cacf-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cacf-240"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cacf-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cacf-241">DLL</span><span class="sxs-lookup"><span data-stu-id="3cacf-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cacf-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3cacf-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3cacf-243">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3cacf-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cacf-244">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="3cacf-244">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

