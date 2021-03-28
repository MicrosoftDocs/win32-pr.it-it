---
description: Questa classe è la classe del tipo di evento per gli eventi di rete. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: Classe SystemConfig_Network
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23b469c31645c6a5b04319f91b758ee19beb935c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977583"
---
# <a name="systemconfig_network-class"></a><span data-ttu-id="e0448-104">\_Classe di rete SystemConfig</span><span class="sxs-lookup"><span data-stu-id="e0448-104">SystemConfig\_Network class</span></span>

<span data-ttu-id="e0448-105">Questa classe è la classe del tipo di evento per gli eventi di rete.</span><span class="sxs-lookup"><span data-stu-id="e0448-105">This class is the event type class for network events.</span></span>

<span data-ttu-id="e0448-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="e0448-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0448-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0448-107">Syntax</span></span>

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a><span data-ttu-id="e0448-108">Members</span><span class="sxs-lookup"><span data-stu-id="e0448-108">Members</span></span>

<span data-ttu-id="e0448-109">La classe di **\_ rete SystemConfig** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e0448-109">The **SystemConfig\_Network** class has these types of members:</span></span>

-   [<span data-ttu-id="e0448-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0448-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0448-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0448-111">Properties</span></span>

<span data-ttu-id="e0448-112">La classe di **\_ rete SystemConfig** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e0448-112">The **SystemConfig\_Network** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0448-113">**MaxHashTableSize**</span><span class="sxs-lookup"><span data-stu-id="e0448-113">**MaxHashTableSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0448-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0448-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0448-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0448-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0448-116">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="e0448-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="e0448-117">Dimensioni della tabella hash in cui vengono archiviati i blocchi di controllo TCP (TCBs).</span><span class="sxs-lookup"><span data-stu-id="e0448-117">The size of the hash table in which TCP control blocks (TCBs) are stored.</span></span> <span data-ttu-id="e0448-118">TCP archivia i blocchi di controllo in una tabella hash in modo da poterli trovare molto rapidamente.</span><span class="sxs-lookup"><span data-stu-id="e0448-118">TCP stores control blocks in a hash table so it can find them very quickly.</span></span>

</dd> <dt>

<span data-ttu-id="e0448-119">**MaxUserPort**</span><span class="sxs-lookup"><span data-stu-id="e0448-119">**MaxUserPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0448-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0448-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0448-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0448-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0448-122">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="e0448-122">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e0448-123">Il numero di porta massimo TCP può essere assegnato quando un'applicazione richiede una porta utente disponibile dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e0448-123">The highest port number TCP can assign when an application requests an available user port from the system.</span></span> <span data-ttu-id="e0448-124">In genere, le porte temporanee (quelle utilizzate brevemente) vengono allocate ai numeri di porta da 1024 a 5000.</span><span class="sxs-lookup"><span data-stu-id="e0448-124">Typically, ephemeral ports (those used briefly) are allocated to port numbers 1024 through 5000.</span></span>

<span data-ttu-id="e0448-125">Il valore per il numero di porta utente massimo TCP può assegnare è controllato da un'impostazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e0448-125">The value for the highest user port number TCP can assign is controlled by a registry setting.</span></span> <span data-ttu-id="e0448-126">Per ulteriori informazioni, vedere [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="e0448-126">For more information, see [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span></span>

</dd> <dt>

<span data-ttu-id="e0448-127">**TcbTablePartitions**</span><span class="sxs-lookup"><span data-stu-id="e0448-127">**TcbTablePartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0448-128">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0448-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0448-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0448-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0448-130">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="e0448-130">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="e0448-131">Numero di partizioni nella tabella dei blocchi di controllo del trasporto.</span><span class="sxs-lookup"><span data-stu-id="e0448-131">The number of partitions in the Transport Control Block table.</span></span> <span data-ttu-id="e0448-132">Il partizionamento della tabella dei blocchi di controllo del trasporto riduce la contesa per l'accesso alle tabelle.</span><span class="sxs-lookup"><span data-stu-id="e0448-132">Partitioning the Transport Control Block table minimizes contention for table access.</span></span> <span data-ttu-id="e0448-133">Questa operazione è particolarmente utile nei sistemi multiprocessore.</span><span class="sxs-lookup"><span data-stu-id="e0448-133">This is especially useful on multiprocessor systems.</span></span>

</dd> <dt>

<span data-ttu-id="e0448-134">**TcpTimedWaitDelay**</span><span class="sxs-lookup"><span data-stu-id="e0448-134">**TcpTimedWaitDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0448-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0448-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0448-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0448-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0448-137">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="e0448-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="e0448-138">Tempo che deve trascorrere prima che TCP possa rilasciare una connessione chiusa e riutilizzare le relative risorse.</span><span class="sxs-lookup"><span data-stu-id="e0448-138">The time that must elapse before TCP can release a closed connection and reuse its resources.</span></span> <span data-ttu-id="e0448-139">Questo intervallo tra la chiusura e la versione è noto come \_ stato Time Wait o 2MSL.</span><span class="sxs-lookup"><span data-stu-id="e0448-139">This interval between closure and release is known as the TIME\_WAIT state or 2MSL state.</span></span> <span data-ttu-id="e0448-140">Durante questo periodo di tempo, è possibile riaprire la connessione a un costo molto inferiore per il client e il server rispetto alla creazione di una nuova connessione.</span><span class="sxs-lookup"><span data-stu-id="e0448-140">During this time, the connection can be reopened at much less cost to the client and server than establishing a new connection.</span></span>

<span data-ttu-id="e0448-141">La specifica RFC 793 pubblicata da IETF richiede che TCP mantenga una connessione chiusa per un intervallo almeno pari al doppio della durata massima del segmento (2MSL) della rete.</span><span class="sxs-lookup"><span data-stu-id="e0448-141">RFC 793 published by the IETF requires that TCP maintains a closed connection for an interval at least equal to twice the maximum segment lifetime (2MSL) of the network.</span></span> <span data-ttu-id="e0448-142">Quando viene rilasciata una connessione, è possibile utilizzare la coppia di socket e il blocco di controllo TCP (TCB) per supportare un'altra connessione.</span><span class="sxs-lookup"><span data-stu-id="e0448-142">When a connection is released, its socket pair and TCP control block (TCB) can be used to support another connection.</span></span> <span data-ttu-id="e0448-143">Per impostazione predefinita, MSL è definito come 120 secondi e il valore di questa voce è pari a due MSLs o 4 minuti.</span><span class="sxs-lookup"><span data-stu-id="e0448-143">By default, the MSL is defined to be 120 seconds, and the value of this entry is equal to two MSLs, or 4 minutes.</span></span> <span data-ttu-id="e0448-144">Per ulteriori informazioni, vedere [RFC 793](https://tools.ietf.org/html/rfc973).</span><span class="sxs-lookup"><span data-stu-id="e0448-144">For more information, see [RFC 793](https://tools.ietf.org/html/rfc973).</span></span>

<span data-ttu-id="e0448-145">La riduzione del valore di questa voce tramite un'impostazione del registro di sistema consente a TCP di rilasciare connessioni chiuse più velocemente, fornendo più risorse per le nuove connessioni.</span><span class="sxs-lookup"><span data-stu-id="e0448-145">Reducing the value of this entry using a registry setting allows TCP to release closed connections faster, providing more resources for new connections.</span></span> <span data-ttu-id="e0448-146">Tuttavia, se il valore è troppo basso, TCP potrebbe rilasciare le risorse di connessione prima del completamento della connessione, richiedendo al server di usare risorse aggiuntive per ristabilire la connessione.</span><span class="sxs-lookup"><span data-stu-id="e0448-146">However, if the value is too low, TCP might release connection resources before the connection is complete, requiring the server to use additional resources to reestablish the connection.</span></span>

<span data-ttu-id="e0448-147">In genere, TCP non rilascia connessioni chiuse fino alla scadenza del valore di questa voce.</span><span class="sxs-lookup"><span data-stu-id="e0448-147">Normally, TCP does not release closed connections until the value of this entry expires.</span></span> <span data-ttu-id="e0448-148">Il protocollo TCP, tuttavia, può rilasciare le connessioni prima della scadenza di questo valore se si esauriscono i blocchi di controllo TCP (TCBs).</span><span class="sxs-lookup"><span data-stu-id="e0448-148">However, TCP can release connections before this value expires if it is running out of TCP control blocks (TCBs).</span></span> <span data-ttu-id="e0448-149">Il numero di TCBs creato dal sistema è controllato da un'impostazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e0448-149">The number of TCBs the system creates is controlled by a registry setting.</span></span> <span data-ttu-id="e0448-150">Per ulteriori informazioni, vedere [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="e0448-150">For more information, see [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0448-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0448-151">Requirements</span></span>



| <span data-ttu-id="e0448-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0448-152">Requirement</span></span> | <span data-ttu-id="e0448-153">Valore</span><span class="sxs-lookup"><span data-stu-id="e0448-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e0448-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0448-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e0448-155">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0448-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e0448-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0448-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e0448-157">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e0448-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0448-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0448-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0448-159">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="e0448-159">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 
