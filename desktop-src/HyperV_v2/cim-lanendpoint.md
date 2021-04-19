---
description: Un endpoint di comunicazione che può connettersi a una LAN per inviare e ricevere frame di dati. Gli endpoint LAN includono Ethernet, token ring e interfacce FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: Classe CIM_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320044"
---
# <a name="cim_lanendpoint-class"></a><span data-ttu-id="0d022-104">CIM \_ LANEndpoint (classe)</span><span class="sxs-lookup"><span data-stu-id="0d022-104">CIM\_LANEndpoint class</span></span>

<span data-ttu-id="0d022-105">Un endpoint di comunicazione che può connettersi a una LAN per inviare e ricevere frame di dati.</span><span class="sxs-lookup"><span data-stu-id="0d022-105">A communication endpoint that can connect to a LAN to send and receive data frames.</span></span> <span data-ttu-id="0d022-106">Gli endpoint LAN includono Ethernet, token ring e interfacce FDDI.</span><span class="sxs-lookup"><span data-stu-id="0d022-106">LAN endpoints include ethernet, token Ring, and FDDI interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d022-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d022-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a><span data-ttu-id="0d022-108">Members</span><span class="sxs-lookup"><span data-stu-id="0d022-108">Members</span></span>

<span data-ttu-id="0d022-109">La classe **CIM \_ LANEndpoint** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0d022-109">The **CIM\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="0d022-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d022-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d022-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d022-111">Properties</span></span>

<span data-ttu-id="0d022-112">La classe **CIM \_ LANEndpoint** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0d022-112">The **CIM\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d022-113">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="0d022-113">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d022-114">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0d022-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d022-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d022-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d022-116">Matrice che contiene altri indirizzi unicast che possono essere utilizzati per comunicare con l'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="0d022-116">An array that contains other unicast addresses that may be used to communicate with the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="0d022-117">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="0d022-117">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d022-118">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0d022-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d022-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d022-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d022-120">Matrice che contiene gli indirizzi multicast su cui è in ascolto l'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="0d022-120">An array that contains the multicast addresses to which the LAN endpoint listens.</span></span>

</dd> <dt>

<span data-ttu-id="0d022-121">**LANId**</span><span class="sxs-lookup"><span data-stu-id="0d022-121">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d022-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d022-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d022-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d022-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d022-124">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment. LanID, CIM \_ LANSegment. LanID")</span><span class="sxs-lookup"><span data-stu-id="0d022-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.LANID, CIM\_LANSegment.LANID")</span></span>
</dt> </dl>

<span data-ttu-id="0d022-125">Etichetta o identificatore per il segmento LAN a cui è connesso l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="0d022-125">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="0d022-126">Se l'endpoint non è attualmente connesso o se queste informazioni sono sconosciute, **LanID** è null.</span><span class="sxs-lookup"><span data-stu-id="0d022-126">If the endpoint is not currently connected or if this information is unknown, then **LANID** is NULL.</span></span>

</dd> <dt>

<span data-ttu-id="0d022-127">**LANType**</span><span class="sxs-lookup"><span data-stu-id="0d022-127">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d022-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d022-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d022-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d022-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d022-130">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANCONNECTIVITYSEGMENT. ConnectivityType, CIM \_ LANSegment. LANType ")</span><span class="sxs-lookup"><span data-stu-id="0d022-130">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.ConnectivityType, CIM\_LANSegment.LANType")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="0d022-131">Descrizione deprecata: tipo di tecnologia utilizzata nella LAN.</span><span class="sxs-lookup"><span data-stu-id="0d022-131">Deprecated description: The kind of technology used on the LAN.</span></span>

 

<span data-ttu-id="0d022-132">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0d022-132">This property is deprecated.</span></span> <span data-ttu-id="0d022-133">È invece consigliabile usare la proprietà **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="0d022-133">Instead we recommend that you use the **ProtocolType** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d022-134">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0d022-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d022-135">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0d022-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="0d022-136">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="0d022-136">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="0d022-137">**Tokenring** (3)</span><span class="sxs-lookup"><span data-stu-id="0d022-137">**TokenRing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="0d022-138">**FDDI** (4)</span><span class="sxs-lookup"><span data-stu-id="0d022-138">**FDDI** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d022-139">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="0d022-139">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d022-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d022-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d022-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d022-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d022-142">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span><span class="sxs-lookup"><span data-stu-id="0d022-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span></span>
</dt> </dl>

<span data-ttu-id="0d022-143">Indirizzo unicast principale utilizzato dall'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="0d022-143">The principal unicast address used by the LAN endpoint.</span></span>

<span data-ttu-id="0d022-144">L'indirizzo MAC deve essere formattato con le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d022-144">The MAC address must be formatted with the following characteristics:</span></span>

-   <span data-ttu-id="0d022-145">L'indirizzo è costituito da dodici cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="0d022-145">The address consists of twelve hexadecimal digits.</span></span>
-   <span data-ttu-id="0d022-146">Ogni coppia di cifre rappresenta uno dei sei ottetti dell'indirizzo MAC.</span><span class="sxs-lookup"><span data-stu-id="0d022-146">Each pair of digits represents one of the six octets of the MAC address.</span></span>
-   <span data-ttu-id="0d022-147">Ogni coppia di cifre deve essere in ordine di bit canonico in base allo standard RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="0d022-147">Each pair of digits must be in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="0d022-148">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="0d022-148">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d022-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d022-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d022-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d022-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d022-151">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="0d022-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="0d022-152">Dimensione massima, in byte, dei campi dati inviati o ricevuti dall'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="0d022-152">The maximum size, in bytes, of data fields sent or received by the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="0d022-153">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="0d022-153">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d022-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d022-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d022-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d022-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d022-156">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANConnectivitySegment. OtherTypeDescription ","**CIM \_ LANEndpoint**.**LANType**")</span><span class="sxs-lookup"><span data-stu-id="0d022-156">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.OtherTypeDescription", "**CIM\_LANEndpoint**.**LANType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="0d022-157">Descrizione deprecata: tipo di tecnologia utilizzata sulla LAN quando la proprietà **LANType** è impostata su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="0d022-157">Deprecated description: The type of technology used on the LAN when the **LANType** property is set to "1" (Other).</span></span>

 

<span data-ttu-id="0d022-158">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0d022-158">This property is deprecated.</span></span> <span data-ttu-id="0d022-159">È invece consigliabile usare la proprietà **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="0d022-159">Instead we recommend that you use the **OtherTypeDescription** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d022-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d022-160">Requirements</span></span>



| <span data-ttu-id="0d022-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d022-161">Requirement</span></span> | <span data-ttu-id="0d022-162">Valore</span><span class="sxs-lookup"><span data-stu-id="0d022-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d022-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d022-163">Minimum supported client</span></span><br/> | <span data-ttu-id="0d022-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0d022-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0d022-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d022-165">Minimum supported server</span></span><br/> | <span data-ttu-id="0d022-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d022-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0d022-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d022-167">Namespace</span></span><br/>                | <span data-ttu-id="0d022-168">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0d022-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0d022-169">MOF</span><span class="sxs-lookup"><span data-stu-id="0d022-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d022-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d022-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d022-171">DLL</span><span class="sxs-lookup"><span data-stu-id="0d022-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d022-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d022-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d022-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d022-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d022-174">**\_PROTOCOLENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="0d022-174">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

