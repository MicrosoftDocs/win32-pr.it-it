---
description: La classe SnmpNotification esegue il mapping dalla macro del tipo di notifica a una classe CIM incapsulata.
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: Classe SnmpNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: 89b50d04b435f862a329953f14b47646937a1d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530210"
---
# <a name="snmpnotification-class"></a><span data-ttu-id="4032d-103">Classe SnmpNotification</span><span class="sxs-lookup"><span data-stu-id="4032d-103">SnmpNotification class</span></span>

<span data-ttu-id="4032d-104">La classe **SnmpNotification** esegue il mapping dalla macro del [tipo di notifica](notification-type-macro.md) a una classe CIM incapsulata.</span><span class="sxs-lookup"><span data-stu-id="4032d-104">The **SnmpNotification** class maps from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class.</span></span> <span data-ttu-id="4032d-105">Si tratta di una classe di base utilizzata dal provider [SNMP](snmp-provider.md) per qualsiasi classe mappata dalla macro del [tipo di notifica](notification-type-macro.md) a una classe CIM incapsulata dal provider SNMP.</span><span class="sxs-lookup"><span data-stu-id="4032d-105">It is a base class used by the [SNMP Provider](snmp-provider.md) for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class by the SNMP Provider.</span></span>

> [!Note]  
> <span data-ttu-id="4032d-106">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4032d-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4032d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4032d-107">Syntax</span></span>

``` syntax
class SnmpNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="4032d-108">Members</span><span class="sxs-lookup"><span data-stu-id="4032d-108">Members</span></span>

<span data-ttu-id="4032d-109">La classe **SnmpNotification** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4032d-109">The **SnmpNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="4032d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4032d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4032d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4032d-111">Properties</span></span>

<span data-ttu-id="4032d-112">La classe **SnmpNotification** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4032d-112">The **SnmpNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4032d-113">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="4032d-113">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4032d-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4032d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4032d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4032d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4032d-116">Indirizzo di rete dell'entità che ha creato la notifica.</span><span class="sxs-lookup"><span data-stu-id="4032d-116">Network address of the entity that created the notification.</span></span> <span data-ttu-id="4032d-117">Si tratta dell'indirizzo effettivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4032d-117">This is the actual address of the device.</span></span> <span data-ttu-id="4032d-118">Quando l'entità di gestione USA SNMP su UDP, l'indirizzo di trasporto fa riferimento a un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="4032d-118">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="4032d-119">Quando l'entità di gestione utilizza SNMP su IPX, l'indirizzo di trasporto viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="4032d-119">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="4032d-120">Questa proprietà è valida solo per SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="4032d-120">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="4032d-121">**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="4032d-121">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4032d-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4032d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4032d-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4032d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4032d-124">Protocollo di trasporto utilizzato dall'entità mittente.</span><span class="sxs-lookup"><span data-stu-id="4032d-124">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="4032d-125">Questa proprietà è valida per SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4032d-125">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="4032d-126">**AgentTransportAddress**</span><span class="sxs-lookup"><span data-stu-id="4032d-126">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4032d-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4032d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4032d-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4032d-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4032d-129">Indirizzo di rete dell'entità che ha inviato la notifica.</span><span class="sxs-lookup"><span data-stu-id="4032d-129">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="4032d-130">Si tratta dell'indirizzo dell'ultima entità che ha inviato la notifica.</span><span class="sxs-lookup"><span data-stu-id="4032d-130">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="4032d-131">Quando l'entità di gestione USA SNMP su UDP, l'indirizzo di trasporto fa riferimento a un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="4032d-131">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="4032d-132">Quando l'entità di gestione utilizza SNMP su IPX, l'indirizzo di trasporto fa riferimento a un indirizzo IPX.</span><span class="sxs-lookup"><span data-stu-id="4032d-132">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="4032d-133">Questa proprietà è valida per SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4032d-133">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="4032d-134">**AgentTransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="4032d-134">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4032d-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4032d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4032d-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4032d-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4032d-137">Protocollo di trasporto utilizzato dall'entità mittente.</span><span class="sxs-lookup"><span data-stu-id="4032d-137">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="4032d-138">**Community**</span><span class="sxs-lookup"><span data-stu-id="4032d-138">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4032d-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4032d-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4032d-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4032d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4032d-141">Nome della community associato a un'istanza della PDU.</span><span class="sxs-lookup"><span data-stu-id="4032d-141">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="4032d-142">Il nome della community autentica il creatore della PDU.</span><span class="sxs-lookup"><span data-stu-id="4032d-142">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="4032d-143">Questa proprietà è valida sia per SNMPv1 che per SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4032d-143">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="4032d-144">**Identificazione**</span><span class="sxs-lookup"><span data-stu-id="4032d-144">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4032d-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4032d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4032d-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4032d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4032d-147">Qualificatori: **\_ convenzione testuale** ("OBJECTIDENTIFIER"), **codifica** ("OBJECTIDENTIFIER"), **\_ sintassi degli oggetti** ("OBJECTIDENTIFIER"), **\_ identificatore di oggetto** ("1.3.6.1.6.3.1.1.4.1")</span><span class="sxs-lookup"><span data-stu-id="4032d-147">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="4032d-148">Identificazione autorevole della notifica.</span><span class="sxs-lookup"><span data-stu-id="4032d-148">Authoritative identification of this notification.</span></span> <span data-ttu-id="4032d-149">Esegue il mapping direttamente al binding della variabile SnmpTrapOID.</span><span class="sxs-lookup"><span data-stu-id="4032d-149">Maps directly to the SnmpTrapOID variable binding.</span></span> <span data-ttu-id="4032d-150">Questa proprietà è valida solo per SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4032d-150">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="4032d-151">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="4032d-151">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4032d-152">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="4032d-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4032d-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4032d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4032d-154">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="4032d-154">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="4032d-155">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="4032d-155">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="4032d-156">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4032d-156">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4032d-157">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="4032d-157">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4032d-158">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4032d-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4032d-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4032d-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4032d-160">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="4032d-160">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="4032d-161">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="4032d-161">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="4032d-162">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="4032d-162">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="4032d-163">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="4032d-163">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="4032d-164">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4032d-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4032d-165">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="4032d-165">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4032d-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4032d-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4032d-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4032d-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4032d-168">Qualificatori: **\_ convenzione testuale** ("TimeTicks"), **codifica** ("TimeTicks"), **\_ sintassi degli oggetti** ("TimeTicks"), **\_ identificatore di oggetto** ("1.3.6.1.2.1.1.3")</span><span class="sxs-lookup"><span data-stu-id="4032d-168">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="4032d-169">Tempo in centesimi di secondo dall'ultima reinizializzazione della parte relativa alla gestione della rete dell'agente.</span><span class="sxs-lookup"><span data-stu-id="4032d-169">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="4032d-170">Variabile MIB sysUptime. 0, che è di tipo **INTEGER32**.</span><span class="sxs-lookup"><span data-stu-id="4032d-170">MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="4032d-171">Questa proprietà esegue il mapping al **timestamp** della proprietà della classe CIM, che è di tipo **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="4032d-171">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="4032d-172">Questa proprietà è valida solo per SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4032d-172">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4032d-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="4032d-173">Remarks</span></span>

<span data-ttu-id="4032d-174">Una macro del [tipo di notifica](notification-type-macro.md) che contiene riferimenti a una macro di [tipo oggetto](object-type-macro.md) denominata **timestamp** o **Identificazione** causa un conflitto di mapping.</span><span class="sxs-lookup"><span data-stu-id="4032d-174">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="4032d-175">Se si verifica questo conflitto, le proprietà obbligatorie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.</span><span class="sxs-lookup"><span data-stu-id="4032d-175">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="4032d-176">Una macro del [tipo di notifica](notification-type-macro.md) che contiene riferimenti a una macro di [tipo oggetto](object-type-macro.md) denominata **community** causa un conflitto di mapping.</span><span class="sxs-lookup"><span data-stu-id="4032d-176">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="4032d-177">Se si verifica questo conflitto, le proprietà obbligatorie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.</span><span class="sxs-lookup"><span data-stu-id="4032d-177">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4032d-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4032d-178">Requirements</span></span>



| <span data-ttu-id="4032d-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="4032d-179">Requirement</span></span> | <span data-ttu-id="4032d-180">Valore</span><span class="sxs-lookup"><span data-stu-id="4032d-180">Value</span></span> |
|-------------------------------------|----------------------------------|
| <span data-ttu-id="4032d-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4032d-181">Minimum supported client</span></span><br/> | <span data-ttu-id="4032d-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4032d-182">Windows Vista</span></span><br/>         |
| <span data-ttu-id="4032d-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4032d-183">Minimum supported server</span></span><br/> | <span data-ttu-id="4032d-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4032d-184">Windows Server 2008</span></span><br/>   |
| <span data-ttu-id="4032d-185">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4032d-185">Namespace</span></span><br/>                | <span data-ttu-id="4032d-186">\\Localhost SNMP \\ radice</span><span class="sxs-lookup"><span data-stu-id="4032d-186">Root\\snmp\\localhost</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4032d-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4032d-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4032d-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="4032d-188">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="4032d-189">Macro del tipo di notifica</span><span class="sxs-lookup"><span data-stu-id="4032d-189">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

