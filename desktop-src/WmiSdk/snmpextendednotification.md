---
description: La classe SnmpExtendedNotification è la classe di base per qualsiasi classe mappata dalla macro del tipo di notifica a una classe CIM dal provider SNMP.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: Classe SnmpExtendedNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: e21fcc32976c42f41cd33a519e5fa6c684acdfc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309878"
---
# <a name="snmpextendednotification-class"></a><span data-ttu-id="b906a-103">Classe SnmpExtendedNotification</span><span class="sxs-lookup"><span data-stu-id="b906a-103">SnmpExtendedNotification class</span></span>

<span data-ttu-id="b906a-104">La classe **SnmpExtendedNotification** è la classe di base per qualsiasi classe mappata dalla macro del [tipo di notifica](notification-type-macro.md) a una classe CIM dal [provider SNMP](snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b906a-104">The **SnmpExtendedNotification** class is the base class for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to a CIM class by the [SNMP Provider](snmp-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="b906a-105">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b906a-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="b906a-106">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b906a-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b906a-107">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b906a-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b906a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b906a-108">Syntax</span></span>

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
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

## <a name="members"></a><span data-ttu-id="b906a-109">Members</span><span class="sxs-lookup"><span data-stu-id="b906a-109">Members</span></span>

<span data-ttu-id="b906a-110">La classe **SnmpExtendedNotification** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b906a-110">The **SnmpExtendedNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="b906a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b906a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b906a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b906a-112">Properties</span></span>

<span data-ttu-id="b906a-113">La classe **SnmpExtendedNotification** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b906a-113">The **SnmpExtendedNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b906a-114">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="b906a-114">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b906a-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b906a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b906a-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b906a-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b906a-117">Indirizzo di rete dell'entità che ha creato la notifica.</span><span class="sxs-lookup"><span data-stu-id="b906a-117">Network address of the entity that created the notification.</span></span> <span data-ttu-id="b906a-118">Si tratta dell'indirizzo effettivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b906a-118">This is the actual address of the device.</span></span> <span data-ttu-id="b906a-119">Quando l'entità di gestione USA SNMP su UDP, l'indirizzo di trasporto fa riferimento a un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="b906a-119">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="b906a-120">Quando l'entità di gestione utilizza SNMP su IPX, l'indirizzo di trasporto viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="b906a-120">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="b906a-121">Questa proprietà è valida solo per SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="b906a-121">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="b906a-122">**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="b906a-122">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b906a-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b906a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b906a-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b906a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b906a-125">Protocollo di trasporto utilizzato dall'entità mittente.</span><span class="sxs-lookup"><span data-stu-id="b906a-125">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="b906a-126">Questa proprietà è valida per SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b906a-126">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="b906a-127">**AgentTransportAddress**</span><span class="sxs-lookup"><span data-stu-id="b906a-127">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b906a-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b906a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b906a-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b906a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b906a-130">Indirizzo di rete dell'entità che ha inviato la notifica.</span><span class="sxs-lookup"><span data-stu-id="b906a-130">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="b906a-131">Si tratta dell'indirizzo dell'ultima entità che ha inviato la notifica.</span><span class="sxs-lookup"><span data-stu-id="b906a-131">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="b906a-132">Quando l'entità di gestione USA SNMP su UDP, l'indirizzo di trasporto fa riferimento a un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="b906a-132">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="b906a-133">Quando l'entità di gestione utilizza SNMP su IPX, l'indirizzo di trasporto fa riferimento a un indirizzo IPX.</span><span class="sxs-lookup"><span data-stu-id="b906a-133">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="b906a-134">Questa proprietà è valida per SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b906a-134">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="b906a-135">**AgentTransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="b906a-135">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b906a-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b906a-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b906a-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b906a-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b906a-138">Protocollo di trasporto utilizzato dall'entità mittente.</span><span class="sxs-lookup"><span data-stu-id="b906a-138">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="b906a-139">**Community**</span><span class="sxs-lookup"><span data-stu-id="b906a-139">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b906a-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b906a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b906a-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b906a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b906a-142">Nome della community associato a un'istanza della PDU.</span><span class="sxs-lookup"><span data-stu-id="b906a-142">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="b906a-143">Il nome della community autentica il creatore della PDU.</span><span class="sxs-lookup"><span data-stu-id="b906a-143">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="b906a-144">Questa proprietà è valida sia per SNMPv1 che per SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b906a-144">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="b906a-145">**Identificazione**</span><span class="sxs-lookup"><span data-stu-id="b906a-145">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b906a-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b906a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b906a-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b906a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b906a-148">Qualificatori: **\_ convenzione testuale** ("OBJECTIDENTIFIER"), **codifica** ("OBJECTIDENTIFIER"), **\_ sintassi degli oggetti** ("OBJECTIDENTIFIER"), **\_ identificatore di oggetto** ("1.3.6.1.6.3.1.1.4.1")</span><span class="sxs-lookup"><span data-stu-id="b906a-148">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="b906a-149">Identificazione autorevole della notifica.</span><span class="sxs-lookup"><span data-stu-id="b906a-149">Authoritative identification of this notification.</span></span> <span data-ttu-id="b906a-150">Esegue il mapping direttamente alla voce MIB SnmpTrapOID binding della variabile.</span><span class="sxs-lookup"><span data-stu-id="b906a-150">Maps directly to the MIB entry SnmpTrapOID variable binding.</span></span> <span data-ttu-id="b906a-151">Questa proprietà è valida solo per SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b906a-151">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="b906a-152">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="b906a-152">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b906a-153">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b906a-153">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b906a-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b906a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b906a-155">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="b906a-155">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="b906a-156">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b906a-156">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="b906a-157">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b906a-157">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b906a-158">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="b906a-158">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b906a-159">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b906a-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b906a-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b906a-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b906a-161">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="b906a-161">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="b906a-162">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="b906a-162">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="b906a-163">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="b906a-163">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="b906a-164">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b906a-164">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="b906a-165">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b906a-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b906a-166">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="b906a-166">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b906a-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b906a-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b906a-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b906a-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b906a-169">Qualificatori: **\_ convenzione testuale** ("TimeTicks"), **codifica** ("TimeTicks"), **\_ sintassi degli oggetti** ("TimeTicks"), **\_ identificatore di oggetto** ("1.3.6.1.2.1.1.3")</span><span class="sxs-lookup"><span data-stu-id="b906a-169">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="b906a-170">Tempo in centesimi di secondo dall'ultima reinizializzazione della parte relativa alla gestione della rete dell'agente.</span><span class="sxs-lookup"><span data-stu-id="b906a-170">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="b906a-171">Viene eseguito il mapping alla variabile MIB sysUptime. 0, che è di tipo **INTEGER32**.</span><span class="sxs-lookup"><span data-stu-id="b906a-171">This maps to the MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="b906a-172">Questa proprietà esegue il mapping al **timestamp** della proprietà della classe CIM, che è di tipo **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="b906a-172">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="b906a-173">Questa proprietà è valida solo per SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b906a-173">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b906a-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="b906a-174">Remarks</span></span>

<span data-ttu-id="b906a-175">Una macro del [tipo di notifica](notification-type-macro.md) che contiene riferimenti a una macro di [tipo oggetto](object-type-macro.md) denominata **timestamp** o **Identificazione** causa un conflitto di mapping.</span><span class="sxs-lookup"><span data-stu-id="b906a-175">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="b906a-176">Se si verifica questo conflitto, le proprietà obbligatorie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.</span><span class="sxs-lookup"><span data-stu-id="b906a-176">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="b906a-177">Una macro del [tipo di notifica](notification-type-macro.md) che contiene riferimenti a una macro di [tipo oggetto](object-type-macro.md) denominata **community** causa un conflitto di mapping.</span><span class="sxs-lookup"><span data-stu-id="b906a-177">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="b906a-178">Se si verifica questo conflitto, le proprietà obbligatorie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.</span><span class="sxs-lookup"><span data-stu-id="b906a-178">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b906a-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b906a-179">Requirements</span></span>



| <span data-ttu-id="b906a-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="b906a-180">Requirement</span></span> | <span data-ttu-id="b906a-181">Valore</span><span class="sxs-lookup"><span data-stu-id="b906a-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b906a-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b906a-182">Minimum supported client</span></span><br/> | <span data-ttu-id="b906a-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b906a-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b906a-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b906a-184">Minimum supported server</span></span><br/> | <span data-ttu-id="b906a-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b906a-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b906a-186">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b906a-186">Namespace</span></span><br/>                | <span data-ttu-id="b906a-187">\\Archivio SMIR SNMP \\ radice</span><span class="sxs-lookup"><span data-stu-id="b906a-187">Root\\snmp\\SMIR</span></span><br/>                                                             |
| <span data-ttu-id="b906a-188">MOF</span><span class="sxs-lookup"><span data-stu-id="b906a-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b906a-189"><dt>SnmpSmiR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b906a-189"><dt>SnmpSmiR.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b906a-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b906a-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b906a-191">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="b906a-191">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="b906a-192">Macro del tipo di notifica</span><span class="sxs-lookup"><span data-stu-id="b906a-192">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

