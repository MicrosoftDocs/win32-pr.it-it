---
description: Win32 \_ TCPIPPrinterPort&\# 32; Classe WMI che rappresenta un punto di accesso del servizio TCP/IP.
ms.assetid: b1be18b6-47de-461c-a90b-c7e0537130ef
ms.tgt_platform: multiple
title: Classe Win32_TCPIPPrinterPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TCPIPPrinterPort
- Win32_TCPIPPrinterPort.Caption
- Win32_TCPIPPrinterPort.Description
- Win32_TCPIPPrinterPort.InstallDate
- Win32_TCPIPPrinterPort.Status
- Win32_TCPIPPrinterPort.CreationClassName
- Win32_TCPIPPrinterPort.Name
- Win32_TCPIPPrinterPort.SystemCreationClassName
- Win32_TCPIPPrinterPort.SystemName
- Win32_TCPIPPrinterPort.Type
- Win32_TCPIPPrinterPort.ByteCount
- Win32_TCPIPPrinterPort.HostAddress
- Win32_TCPIPPrinterPort.PortNumber
- Win32_TCPIPPrinterPort.Protocol
- Win32_TCPIPPrinterPort.Queue
- Win32_TCPIPPrinterPort.SNMPCommunity
- Win32_TCPIPPrinterPort.SNMPDevIndex
- Win32_TCPIPPrinterPort.SNMPEnabled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a0b0f0cb73cc60ff117399a636b0ab8542fac6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305240"
---
# <a name="win32_tcpipprinterport-class"></a><span data-ttu-id="73f8a-103">Win32 \_ TCPIPPrinterPort (classe)</span><span class="sxs-lookup"><span data-stu-id="73f8a-103">Win32\_TCPIPPrinterPort class</span></span>

<span data-ttu-id="73f8a-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ TCPIPPrinterPort Win32** rappresenta un punto di accesso del servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="73f8a-104">The **Win32\_TCPIPPrinterPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a TCP/IP service access point.</span></span>

<span data-ttu-id="73f8a-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="73f8a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="73f8a-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="73f8a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f8a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73f8a-107">Syntax</span></span>

``` syntax
class Win32_TCPIPPrinterPort : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
  boolean  ByteCount;
  string   HostAddress;
  uint32   PortNumber;
  uint32   Protocol;
  string   Queue;
  string   SNMPCommunity;
  uint32   SNMPDevIndex;
  boolean  SNMPEnabled;
};
```

## <a name="members"></a><span data-ttu-id="73f8a-108">Members</span><span class="sxs-lookup"><span data-stu-id="73f8a-108">Members</span></span>

<span data-ttu-id="73f8a-109">La classe **Win32 \_ TCPIPPrinterPort** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="73f8a-109">The **Win32\_TCPIPPrinterPort** class has these types of members:</span></span>

-   [<span data-ttu-id="73f8a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73f8a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73f8a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73f8a-111">Properties</span></span>

<span data-ttu-id="73f8a-112">La classe **Win32 \_ TCPIPPrinterPort** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="73f8a-112">The **Win32\_TCPIPPrinterPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73f8a-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="73f8a-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-114">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="73f8a-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-116">Se **true**, il computer conta i byte in un documento prima di inviarli alla stampante e la stampante riporta il numero di byte effettivamente letti.</span><span class="sxs-lookup"><span data-stu-id="73f8a-116">If **TRUE**, the computer counts the bytes in a document before sending them to the printer and the printer reports back the number of bytes actually read.</span></span> <span data-ttu-id="73f8a-117">Questa funzionalità viene usata per la diagnostica quando vengono rilevati byte mancanti nell'output di stampa.</span><span class="sxs-lookup"><span data-stu-id="73f8a-117">This capability is used for diagnostics when missing bytes are detected in the print output.</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="73f8a-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73f8a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-121">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="73f8a-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-122">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="73f8a-122">A short textual description of the object.</span></span>

<span data-ttu-id="73f8a-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73f8a-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="73f8a-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73f8a-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-127">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="73f8a-127">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-128">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="73f8a-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="73f8a-129">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="73f8a-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="73f8a-130">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="73f8a-130">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="73f8a-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73f8a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-134">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="73f8a-134">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-135">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="73f8a-135">A textual description of the object.</span></span>

<span data-ttu-id="73f8a-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73f8a-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-137">**HostAddress**</span><span class="sxs-lookup"><span data-stu-id="73f8a-137">**HostAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73f8a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-140">Indirizzo del dispositivo o del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="73f8a-140">Address of the device or print server.</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="73f8a-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-142">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73f8a-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-144">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="73f8a-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-145">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="73f8a-145">Indicates when the object was installed.</span></span> <span data-ttu-id="73f8a-146">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="73f8a-146">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="73f8a-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73f8a-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-148">**Nome**</span><span class="sxs-lookup"><span data-stu-id="73f8a-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73f8a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-151">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="73f8a-151">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-152">Identifica in modo univoco il punto di accesso al servizio e fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="73f8a-152">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="73f8a-153">Questa funzionalità è descritta più dettagliatamente nella proprietà Description dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="73f8a-153">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="73f8a-154">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="73f8a-154">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-155">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="73f8a-155">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-156">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73f8a-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-158">Numero di porte TCP utilizzate dal monitor porta per comunicare con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73f8a-158">Number of the TCP ports used by the port monitor to communicate with the device.</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-159">**Protocollo**</span><span class="sxs-lookup"><span data-stu-id="73f8a-159">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-160">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73f8a-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-162">Protocollo di stampa utilizzato.</span><span class="sxs-lookup"><span data-stu-id="73f8a-162">Printing protocol used.</span></span> <span data-ttu-id="73f8a-163">Alcune stampanti supportano solo LPR.</span><span class="sxs-lookup"><span data-stu-id="73f8a-163">Some printers support only LPR.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="73f8a-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="73f8a-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="73f8a-165">RAW</span><span class="sxs-lookup"><span data-stu-id="73f8a-165">RAW</span></span>

<span data-ttu-id="73f8a-166">Stampa diretta in un dispositivo o in un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="73f8a-166">Printing directly to a device or print server.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="73f8a-167"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="73f8a-167"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="73f8a-168">LPR</span><span class="sxs-lookup"><span data-stu-id="73f8a-168">LPR</span></span>

<span data-ttu-id="73f8a-169">Protocollo legacy, che alla fine viene sostituito da RAW.</span><span class="sxs-lookup"><span data-stu-id="73f8a-169">Legacy protocol, which is eventually replaced by RAW.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="73f8a-170">**Coda**</span><span class="sxs-lookup"><span data-stu-id="73f8a-170">**Queue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73f8a-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-173">Nome della coda di stampa nel server se utilizzato con il protocollo LPR.</span><span class="sxs-lookup"><span data-stu-id="73f8a-173">Name of the print queue on the server when used with the LPR protocol.</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-174">**SNMPCommunity**</span><span class="sxs-lookup"><span data-stu-id="73f8a-174">**SNMPCommunity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73f8a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-177">Valore del livello di sicurezza per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73f8a-177">Security level value for the device.</span></span>

<span data-ttu-id="73f8a-178">Esempio: "public" "</span><span class="sxs-lookup"><span data-stu-id="73f8a-178">Example: "public'"</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-179">**SNMPDevIndex**</span><span class="sxs-lookup"><span data-stu-id="73f8a-179">**SNMPDevIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-180">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73f8a-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-182">Numero di indice SNMP del dispositivo per l'agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="73f8a-182">SNMP index number of this device for the SNMP agent.</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-183">**SNMPEnabled**</span><span class="sxs-lookup"><span data-stu-id="73f8a-183">**SNMPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-184">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="73f8a-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-186">Se **true**, questa stampante supporta [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Simple Network Management Protocol) e può fornire informazioni dettagliate sullo stato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73f8a-186">If **TRUE**, this printer supports [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Simple Network Management Protocol) and can provide rich status information from the device.</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-187">**Status**</span><span class="sxs-lookup"><span data-stu-id="73f8a-187">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73f8a-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-190">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="73f8a-190">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-191">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="73f8a-191">String that indicates the current status of the object.</span></span> <span data-ttu-id="73f8a-192">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="73f8a-192">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="73f8a-193">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="73f8a-193">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="73f8a-194">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="73f8a-194">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="73f8a-195">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="73f8a-195">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="73f8a-196">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="73f8a-196">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="73f8a-197">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="73f8a-197">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="73f8a-198">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73f8a-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="73f8a-199">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="73f8a-199">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="73f8a-200">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="73f8a-200">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="73f8a-201">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="73f8a-201">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="73f8a-202">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="73f8a-202">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="73f8a-203">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="73f8a-203">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="73f8a-204">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="73f8a-204">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="73f8a-205">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="73f8a-205">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="73f8a-206">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="73f8a-206">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="73f8a-207">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="73f8a-207">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="73f8a-208">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="73f8a-208">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="73f8a-209">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="73f8a-209">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="73f8a-210">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="73f8a-210">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="73f8a-211">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="73f8a-211">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73f8a-212">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="73f8a-212">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73f8a-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-215">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="73f8a-215">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-216">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="73f8a-216">The scoping system's creation class name.</span></span>

<span data-ttu-id="73f8a-217">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="73f8a-217">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-218">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="73f8a-218">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73f8a-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-221">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="73f8a-221">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-222">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="73f8a-222">The scoping system's name.</span></span>

<span data-ttu-id="73f8a-223">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="73f8a-223">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="73f8a-224">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="73f8a-224">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f8a-225">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73f8a-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73f8a-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f8a-227">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="73f8a-227">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="73f8a-228">Tipo di SAP, ad esempio collegato o reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="73f8a-228">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="73f8a-229">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="73f8a-229">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="73f8a-230">**Scrittura** (1)</span><span class="sxs-lookup"><span data-stu-id="73f8a-230">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="73f8a-231">**Lettura** (2)</span><span class="sxs-lookup"><span data-stu-id="73f8a-231">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="73f8a-232">**Reindirizzato** (4)</span><span class="sxs-lookup"><span data-stu-id="73f8a-232">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="73f8a-233">**Rete \_ Collegato** (8)</span><span class="sxs-lookup"><span data-stu-id="73f8a-233">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="73f8a-234">**sconosciuto** (16)</span><span class="sxs-lookup"><span data-stu-id="73f8a-234">**unknown** (16)</span></span>


<span data-ttu-id="73f8a-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="73f8a-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="73f8a-236">Commenti</span><span class="sxs-lookup"><span data-stu-id="73f8a-236">Remarks</span></span>

<span data-ttu-id="73f8a-237">La **classe \_ TCPIPPrinterPort di Win32** è derivata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md) che deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73f8a-237">The **Win32\_TCPIPPrinterPort** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="73f8a-238">Il privilegio **SeLoadDriverPrivilege** è necessario per eliminare un'istanza di questa classe WMI.</span><span class="sxs-lookup"><span data-stu-id="73f8a-238">The **SeLoadDriverPrivilege** privilege is required to delete an instance of this WMI class.</span></span> <span data-ttu-id="73f8a-239">Nel frammento di script seguente viene illustrato come effettuare una connessione a WMI che utilizza questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="73f8a-239">The following script snippet demonstrates how to make a connection to WMI that uses this privilege.</span></span>

`Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate, (LoadDriver)}")`

## <a name="examples"></a><span data-ttu-id="73f8a-240">Esempio</span><span class="sxs-lookup"><span data-stu-id="73f8a-240">Examples</span></span>

<span data-ttu-id="73f8a-241">L'esempio di PowerShell seguente rimuove una stampante e la porta della stampante TCPIP associata.</span><span class="sxs-lookup"><span data-stu-id="73f8a-241">The following PowerShell sample removes a printer and the associated TCPIP printer port.</span></span>


```PowerShell
function Remove-PrinterAndPort{
    Param( $printername )
   $printer=gwmi win32_Printer -filter "name='HPDJ600'"
   $printer.Delete()
   $port=gwmi win32_tcpipprinterport -filter "name='$($printer.portname)'" -enableall
   $port.Delete()
}
```



## <a name="requirements"></a><span data-ttu-id="73f8a-242">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73f8a-242">Requirements</span></span>



| <span data-ttu-id="73f8a-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="73f8a-243">Requirement</span></span> | <span data-ttu-id="73f8a-244">Valore</span><span class="sxs-lookup"><span data-stu-id="73f8a-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f8a-245">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73f8a-245">Minimum supported client</span></span><br/> | <span data-ttu-id="73f8a-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73f8a-246">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="73f8a-247">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73f8a-247">Minimum supported server</span></span><br/> | <span data-ttu-id="73f8a-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73f8a-248">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="73f8a-249">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="73f8a-249">Namespace</span></span><br/>                | <span data-ttu-id="73f8a-250">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="73f8a-250">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="73f8a-251">MOF</span><span class="sxs-lookup"><span data-stu-id="73f8a-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73f8a-252"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73f8a-252"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="73f8a-253">DLL</span><span class="sxs-lookup"><span data-stu-id="73f8a-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73f8a-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73f8a-254"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="73f8a-255">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73f8a-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73f8a-256">**\_SERVICEACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="73f8a-256">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dt>

[<span data-ttu-id="73f8a-257">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="73f8a-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
