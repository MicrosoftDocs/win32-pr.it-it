---
description: Win32 \_ NetworkProtocol&\# 8194; La classe WMI rappresenta un protocollo e le relative caratteristiche di rete in un computer Win32.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Classe Win32_NetworkProtocol
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483789"
---
# <a name="win32_networkprotocol-class"></a><span data-ttu-id="686e5-103">Win32 \_ NetworkProtocol (classe)</span><span class="sxs-lookup"><span data-stu-id="686e5-103">Win32\_NetworkProtocol class</span></span>

<span data-ttu-id="686e5-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkProtocol Win32** rappresenta un protocollo e le relative caratteristiche di rete in un computer Win32.</span><span class="sxs-lookup"><span data-stu-id="686e5-104">The **Win32\_NetworkProtocol** [WMI class](../wmisdk/retrieving-a-class.md) represents a protocol and its network characteristics on a Win32 computer system.</span></span>

<span data-ttu-id="686e5-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="686e5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="686e5-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="686e5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="686e5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="686e5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a><span data-ttu-id="686e5-108">Members</span><span class="sxs-lookup"><span data-stu-id="686e5-108">Members</span></span>

<span data-ttu-id="686e5-109">La classe **Win32 \_ NetworkProtocol** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="686e5-109">The **Win32\_NetworkProtocol** class has these types of members:</span></span>

-   [<span data-ttu-id="686e5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="686e5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="686e5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="686e5-111">Properties</span></span>

<span data-ttu-id="686e5-112">La classe **Win32 \_ NetworkProtocol** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="686e5-112">The **Win32\_NetworkProtocol** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="686e5-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="686e5-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="686e5-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-116">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="686e5-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-117">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="686e5-117">A short textual description of the object.</span></span>

<span data-ttu-id="686e5-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="686e5-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="686e5-119">**ConnectionlessService**</span><span class="sxs-lookup"><span data-stu-id="686e5-119">**ConnectionlessService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-120">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-122">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags XP1 senza \| \_ connessione")</span><span class="sxs-lookup"><span data-stu-id="686e5-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP1\_CONNECTIONLESS")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-123">Il protocollo supporta il servizio senza connessione.</span><span class="sxs-lookup"><span data-stu-id="686e5-123">Protocol supports connectionless service.</span></span> <span data-ttu-id="686e5-124">Un servizio senza connessione (datagramma) descrive un protocollo di comunicazione o un trasporto in cui i pacchetti di dati vengono instradati in modo indipendente l'uno dall'altro e possono seguire diverse route e arrivare in un ordine diverso rispetto a quello in cui sono stati inviati.</span><span class="sxs-lookup"><span data-stu-id="686e5-124">A connectionless (datagram) service describes a communications protocol or transport in which data packets are routed independently of each other and may follow different routes and arrive in a different order from that in which they were sent.</span></span> <span data-ttu-id="686e5-125">Viceversa, un servizio orientato alla connessione fornisce un circuito virtuale attraverso il quale i pacchetti di dati vengono ricevuti nello stesso ordine in cui sono stati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="686e5-125">Conversely, a connection-oriented service provides a virtual circuit through which data packets are received in the same order they were transmitted.</span></span> <span data-ttu-id="686e5-126">Se la connessione tra computer ha esito negativo, l'applicazione riceve una notifica.</span><span class="sxs-lookup"><span data-stu-id="686e5-126">If the connection between computers fails, the application is notified.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-127">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="686e5-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="686e5-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-130">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="686e5-130">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-131">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="686e5-131">A textual description of the object.</span></span>

<span data-ttu-id="686e5-132">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="686e5-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="686e5-133">**GuaranteesDelivery**</span><span class="sxs-lookup"><span data-stu-id="686e5-133">**GuaranteesDelivery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-136">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ \_ recapito garantito")</span><span class="sxs-lookup"><span data-stu-id="686e5-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_DELIVERY")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-137">Il protocollo supporta la distribuzione di pacchetti di dati.</span><span class="sxs-lookup"><span data-stu-id="686e5-137">Protocol supports delivery of data packets.</span></span> <span data-ttu-id="686e5-138">Se questo flag è **false**, non è certo che tutti i dati inviati raggiungano la destinazione prevista.</span><span class="sxs-lookup"><span data-stu-id="686e5-138">If this flag is **FALSE**, it is uncertain that all of the data sent will reach the intended destination.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-139">**GuaranteesSequencing**</span><span class="sxs-lookup"><span data-stu-id="686e5-139">**GuaranteesSequencing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-140">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-142">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags XP- \| \_ \_ ordine garantito")</span><span class="sxs-lookup"><span data-stu-id="686e5-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_ORDER")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-143">Il protocollo garantisce che i dati arrivino nell'ordine in cui sono stati inviati.</span><span class="sxs-lookup"><span data-stu-id="686e5-143">Protocol ensures that data will arrive in the order in which it was sent.</span></span> <span data-ttu-id="686e5-144">Tenere presente che questa caratteristica non garantisce il recapito dei dati, ma solo il relativo ordine.</span><span class="sxs-lookup"><span data-stu-id="686e5-144">Be aware that this characteristic does not ensure delivery of the data, only its order.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="686e5-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-146">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="686e5-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-148">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="686e5-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-149">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="686e5-149">Indicates when the object was installed.</span></span> <span data-ttu-id="686e5-150">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="686e5-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="686e5-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="686e5-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="686e5-152">**MaximumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="686e5-152">**MaximumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-153">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="686e5-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-155">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| Protocol \_ info \| iMaxSockAddr"), [**unità**](../wmisdk/standard-qualifiers.md) ("caratteri")</span><span class="sxs-lookup"><span data-stu-id="686e5-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMaxSockAddr"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-156">Lunghezza massima di un indirizzo socket supportato dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="686e5-156">Maximum length of a socket address supported by the protocol.</span></span> <span data-ttu-id="686e5-157">Gli indirizzi socket possono essere elementi come un URL ( `www.microsoft.com` ) o un indirizzo IP ( `130.215.24.1` ).</span><span class="sxs-lookup"><span data-stu-id="686e5-157">Socket addresses may be items such as a URL (`www.microsoft.com`) or an IP address (`130.215.24.1`).</span></span>

</dd> <dt>

<span data-ttu-id="686e5-158">**MaximumMessageSize**</span><span class="sxs-lookup"><span data-stu-id="686e5-158">**MaximumMessageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="686e5-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-161">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| Protocol \_ info \| dwMessageSize"), [**unità**](../wmisdk/standard-qualifiers.md) ("caratteri")</span><span class="sxs-lookup"><span data-stu-id="686e5-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwMessageSize"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-162">Dimensione massima del messaggio supportata dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="686e5-162">Maximum message size supported by the protocol.</span></span> <span data-ttu-id="686e5-163">Dimensione massima di un messaggio che può essere inviato o ricevuto dall'host.</span><span class="sxs-lookup"><span data-stu-id="686e5-163">This is the maximum size of a message that can be sent from or received by the host.</span></span> <span data-ttu-id="686e5-164">Per i protocolli che non supportano il framing dei messaggi, la dimensione massima effettiva di un messaggio che può essere inviato a un indirizzo specificato potrebbe essere minore di questo valore.</span><span class="sxs-lookup"><span data-stu-id="686e5-164">For protocols that do not support message framing, the actual maximum size of a message that can be sent to a given address may be less than this value.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-165">**MessageOriented**</span><span class="sxs-lookup"><span data-stu-id="686e5-165">**MessageOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-166">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-168">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures ( \| informazioni sul protocollo \_ \| \| ) dwServiceFlags XP \_ message \_ oriented")</span><span class="sxs-lookup"><span data-stu-id="686e5-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_MESSAGE\_ORIENTED")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-169">Il protocollo è orientato ai messaggi.</span><span class="sxs-lookup"><span data-stu-id="686e5-169">Protocol is message-oriented.</span></span> <span data-ttu-id="686e5-170">Un protocollo orientato ai messaggi utilizza pacchetti di dati per trasferire le informazioni.</span><span class="sxs-lookup"><span data-stu-id="686e5-170">A message-oriented protocol uses packets of data to transfer information.</span></span> <span data-ttu-id="686e5-171">Viceversa, i protocolli orientati al flusso trasferiscono i dati come flusso continuo di byte.</span><span class="sxs-lookup"><span data-stu-id="686e5-171">Conversely, stream-oriented protocols transfer data as a continuous stream of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-172">**MinimumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="686e5-172">**MinimumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-173">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="686e5-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-175">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| Protocol \_ info \| iMinSockAddr"), [**unità**](../wmisdk/standard-qualifiers.md) ("caratteri")</span><span class="sxs-lookup"><span data-stu-id="686e5-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMinSockAddr "), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-176">Lunghezza minima di un indirizzo socket supportato dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="686e5-176">Minimum length of a socket address supported by the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-177">**Nome**</span><span class="sxs-lookup"><span data-stu-id="686e5-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="686e5-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-180">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("nome"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| Protocol \_ info \| lpProtocol")</span><span class="sxs-lookup"><span data-stu-id="686e5-180">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|lpProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-181">Nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="686e5-181">Name for the protocol.</span></span>

<span data-ttu-id="686e5-182">Esempio: "TCP/IP"</span><span class="sxs-lookup"><span data-stu-id="686e5-182">Example: "TCP/IP"</span></span>

</dd> <dt>

<span data-ttu-id="686e5-183">**PseudoStreamOriented**</span><span class="sxs-lookup"><span data-stu-id="686e5-183">**PseudoStreamOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-184">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-186">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ pseudo \_ Stream")</span><span class="sxs-lookup"><span data-stu-id="686e5-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_PSEUDO\_STREAM")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-187">Il protocollo è un protocollo orientato ai messaggi che può ricevere pacchetti di dati a lunghezza variabile o dati trasmessi per tutte le operazioni di ricezione.</span><span class="sxs-lookup"><span data-stu-id="686e5-187">Protocol is a message-oriented protocol that can receive variable-length data packets or streamed data for all receive operations.</span></span> <span data-ttu-id="686e5-188">Questa funzionalità facoltativa è utile quando un'applicazione non vuole che il protocollo consenta di incorniciare i messaggi e richiede caratteristiche orientate al flusso.</span><span class="sxs-lookup"><span data-stu-id="686e5-188">This optional ability is useful when an application does not want the protocol to frame messages, and requires stream-oriented characteristics.</span></span> <span data-ttu-id="686e5-189">Se **true**, il protocollo è pseudo-orientato al flusso.</span><span class="sxs-lookup"><span data-stu-id="686e5-189">If **TRUE**, the protocol is pseudo stream-oriented.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-190">**Status**</span><span class="sxs-lookup"><span data-stu-id="686e5-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="686e5-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-193">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="686e5-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-194">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="686e5-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="686e5-195">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="686e5-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="686e5-196">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="686e5-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="686e5-197">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="686e5-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="686e5-198">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="686e5-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="686e5-199">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="686e5-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="686e5-200">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="686e5-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="686e5-201">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="686e5-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="686e5-202">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="686e5-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="686e5-203">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="686e5-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="686e5-204">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="686e5-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="686e5-205">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="686e5-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="686e5-206">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="686e5-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="686e5-207">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="686e5-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="686e5-208">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="686e5-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="686e5-209">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="686e5-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="686e5-210">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="686e5-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="686e5-211">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="686e5-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="686e5-212">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="686e5-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="686e5-213">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="686e5-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="686e5-214">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="686e5-214">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="686e5-215">**SupportsBroadcasting**</span><span class="sxs-lookup"><span data-stu-id="686e5-215">**SupportsBroadcasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-216">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-218">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures, \| informazioni sul protocollo \_ \| dwServiceFlags \| XP supporta la \_ \_ trasmissione")</span><span class="sxs-lookup"><span data-stu-id="686e5-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_BROADCAST")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-219">Il protocollo supporta un meccanismo per la trasmissione di messaggi attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="686e5-219">Protocol supports a mechanism for broadcasting messages across the network.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-220">**SupportsConnectData**</span><span class="sxs-lookup"><span data-stu-id="686e5-220">**SupportsConnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-221">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-223">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures ( \| informazioni sul protocollo \_ \| \| ) dwServiceFlags XP \_ Connect \_ Data")</span><span class="sxs-lookup"><span data-stu-id="686e5-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_CONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-224">Il protocollo consente la connessione dei dati attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="686e5-224">Protocol allows data to be connected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-225">**SupportsDisconnectData**</span><span class="sxs-lookup"><span data-stu-id="686e5-225">**SupportsDisconnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-226">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-228">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ Disconnetti \_ dati")</span><span class="sxs-lookup"><span data-stu-id="686e5-228">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_DISCONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-229">Il protocollo consente la disconnessione dei dati attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="686e5-229">Protocol allows data to be disconnected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-230">**SupportsEncryption**</span><span class="sxs-lookup"><span data-stu-id="686e5-230">**SupportsEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-231">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-233">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ Encrypts")</span><span class="sxs-lookup"><span data-stu-id="686e5-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_ENCRYPTS")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-234">Il protocollo supporta la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="686e5-234">Protocol supports data encryption.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-235">**SupportsExpeditedData**</span><span class="sxs-lookup"><span data-stu-id="686e5-235">**SupportsExpeditedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-236">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-238">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ Accelerated \_ Data")</span><span class="sxs-lookup"><span data-stu-id="686e5-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_EXPEDITED\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-239">Il protocollo supporta dati accelerati (noti anche come dati urgenti) attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="686e5-239">Protocol supports expedited data (also known as urgent data) across the network.</span></span> <span data-ttu-id="686e5-240">I dati accelerati possono ignorare il controllo di flusso e ricevere la priorità rispetto ai pacchetti di dati normali.</span><span class="sxs-lookup"><span data-stu-id="686e5-240">Expedited data can bypass flow control and receive priority over normal data packets.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-241">**SupportsFragmentation**</span><span class="sxs-lookup"><span data-stu-id="686e5-241">**SupportsFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-242">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-244">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures Structures \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ frammentazione")</span><span class="sxs-lookup"><span data-stu-id="686e5-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_FRAGMENTATION")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-245">Il protocollo supporta la trasmissione dei dati in frammenti.</span><span class="sxs-lookup"><span data-stu-id="686e5-245">Protocol supports transmitting the data in fragments.</span></span> <span data-ttu-id="686e5-246">L'unità di trasferimento massima (MTU) della rete fisica è nascosta per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="686e5-246">Physical network maximum transfer unit (MTU) is hidden from applications.</span></span> <span data-ttu-id="686e5-247">Ogni tipo di supporto ha una dimensione massima del frame che non può essere superata.</span><span class="sxs-lookup"><span data-stu-id="686e5-247">Each media type has a maximum frame size that cannot be exceeded.</span></span> <span data-ttu-id="686e5-248">Il livello di collegamento individua il MTU e lo segnala ai protocolli utilizzati.</span><span class="sxs-lookup"><span data-stu-id="686e5-248">The link layer discovers the MTU and reports it to the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-249">**SupportsGracefulClosing**</span><span class="sxs-lookup"><span data-stu-id="686e5-249">**SupportsGracefulClosing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-250">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-252">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ normale \_ Close")</span><span class="sxs-lookup"><span data-stu-id="686e5-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GRACEFUL\_CLOSE")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-253">Il protocollo supporta operazioni di chiusura in due fasi, note anche come "operazioni di chiusura normali".</span><span class="sxs-lookup"><span data-stu-id="686e5-253">Protocol supports two-phase close operations, also known as "graceful close operations".</span></span> <span data-ttu-id="686e5-254">In caso contrario, il protocollo supporta solo operazioni di chiusura interrotte.</span><span class="sxs-lookup"><span data-stu-id="686e5-254">If not, the protocol supports only abortive close operations.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-255">**SupportsGuaranteedBandwidth**</span><span class="sxs-lookup"><span data-stu-id="686e5-255">**SupportsGuaranteedBandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-256">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-258">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ allocazione della larghezza di banda \_ ")</span><span class="sxs-lookup"><span data-stu-id="686e5-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_BANDWIDTH\_ALLOCATION")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-259">Il protocollo dispone di un meccanismo per stabilire e mantenere una larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="686e5-259">Protocol has a mechanism to establish and maintain a bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-260">**SupportsMulticasting**</span><span class="sxs-lookup"><span data-stu-id="686e5-260">**SupportsMulticasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-261">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-263">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures, \| informazioni sul protocollo \_ \| dwServiceFlags \| XP supporta il \_ \_ multicast")</span><span class="sxs-lookup"><span data-stu-id="686e5-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_MULTICAST")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-264">Il protocollo supporta il multicast.</span><span class="sxs-lookup"><span data-stu-id="686e5-264">Protocol supports multicasting.</span></span>

</dd> <dt>

<span data-ttu-id="686e5-265">**SupportsQualityofService**</span><span class="sxs-lookup"><span data-stu-id="686e5-265">**SupportsQualityofService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="686e5-266">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="686e5-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="686e5-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="686e5-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="686e5-268">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| WSAPROTOCOL \_ info \| dwServiceFlags1 \| XP1 \_ QoS \_ supported")</span><span class="sxs-lookup"><span data-stu-id="686e5-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|WSAPROTOCOL\_INFO\|dwServiceFlags1\|XP1\_QOS\_SUPPORTED")</span></span>
</dt> </dl>

<span data-ttu-id="686e5-269">Il protocollo è in grado di supportare qualità del servizio (QoS) dal provider di servizi o dal gestore di trasporto sovrapposto sottostante.</span><span class="sxs-lookup"><span data-stu-id="686e5-269">Protocol is capable of Quality of Service (QoS) support by the underlying layered service provider or transport carrier.</span></span> <span data-ttu-id="686e5-270">QoS è una raccolta di componenti che consentono la differenziazione e il trattamento preferenziale per subset di dati trasmessi in rete.</span><span class="sxs-lookup"><span data-stu-id="686e5-270">QoS is a collection of components that enable differentiation and preferential treatment for subsets of data transmitted over the network.</span></span> <span data-ttu-id="686e5-271">QoS significa che i subset di dati ottengono una priorità maggiore o un servizio garantito quando attraversano una rete.</span><span class="sxs-lookup"><span data-stu-id="686e5-271">QoS means subsets of data get higher priority or guaranteed service when traversing a network.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="686e5-272">Commenti</span><span class="sxs-lookup"><span data-stu-id="686e5-272">Remarks</span></span>

<span data-ttu-id="686e5-273">La classe **Win32 \_ NetworkProtocol** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="686e5-273">The **Win32\_NetworkProtocol** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="686e5-274">Esempio</span><span class="sxs-lookup"><span data-stu-id="686e5-274">Examples</span></span>

<span data-ttu-id="686e5-275">Nell'esempio di codice VBScript seguente viene illustrato come recuperare un elenco di servizi in esecuzione da istanze di **Win32 \_ NetworkProtocol**.</span><span class="sxs-lookup"><span data-stu-id="686e5-275">The following VBScript code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



<span data-ttu-id="686e5-276">Nell'esempio di codice Perl seguente viene illustrato come recuperare un elenco di servizi in esecuzione da istanze di **Win32 \_ NetworkProtocol**.</span><span class="sxs-lookup"><span data-stu-id="686e5-276">The following Perl code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="686e5-277">Requisiti</span><span class="sxs-lookup"><span data-stu-id="686e5-277">Requirements</span></span>



| <span data-ttu-id="686e5-278">Requisito</span><span class="sxs-lookup"><span data-stu-id="686e5-278">Requirement</span></span> | <span data-ttu-id="686e5-279">Valore</span><span class="sxs-lookup"><span data-stu-id="686e5-279">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="686e5-280">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="686e5-280">Minimum supported client</span></span><br/> | <span data-ttu-id="686e5-281">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="686e5-281">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="686e5-282">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="686e5-282">Minimum supported server</span></span><br/> | <span data-ttu-id="686e5-283">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="686e5-283">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="686e5-284">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="686e5-284">Namespace</span></span><br/>                | <span data-ttu-id="686e5-285">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="686e5-285">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="686e5-286">MOF</span><span class="sxs-lookup"><span data-stu-id="686e5-286">MOF</span></span><br/>                      | <dl> <span data-ttu-id="686e5-287"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="686e5-287"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="686e5-288">DLL</span><span class="sxs-lookup"><span data-stu-id="686e5-288">DLL</span></span><br/>                      | <dl> <span data-ttu-id="686e5-289"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="686e5-289"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="686e5-290">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="686e5-290">See also</span></span>

<dl> <dt>

[<span data-ttu-id="686e5-291">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="686e5-291">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="686e5-292">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="686e5-292">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
