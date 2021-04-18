---
description: Gli indirizzi IPv6 locali e locali del sito sono denominati indirizzi con ambito.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Collegamento IPv6-indirizzi locali e locali del sito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306936"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a><span data-ttu-id="2b8ae-103">Collegamento IPv6-indirizzi locali e locali del sito</span><span class="sxs-lookup"><span data-stu-id="2b8ae-103">IPv6 Link-local and Site-local Addresses</span></span>

<span data-ttu-id="2b8ae-104">Gli indirizzi IPv6 locali e locali del sito sono denominati indirizzi con ambito.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-104">IPv6 link-local and site-local addresses are called scoped addresses.</span></span> <span data-ttu-id="2b8ae-105">L'API Windows Sockets (Winsock) supporta il membro **\_ \_ ID ambito sin6** nella [**struttura \_ IN6 di SOCKADDR**](sockaddr-2.md) per l'utilizzo con gli indirizzi con ambito.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-105">The Windows Sockets (Winsock) API supports the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure for use with scoped addresses.</span></span> <span data-ttu-id="2b8ae-106">Per gli indirizzi di collegamento IPv6 (prefisso FE80::/10), il membro dell' **\_ \_ ID ambito sin6** nella **struttura \_ IN6 sockaddr** è il numero di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-106">For IPv6 link-local addresses (fe80::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is the interface number.</span></span> <span data-ttu-id="2b8ae-107">Per gli indirizzi IP locali del sito IPv6 (prefisso FEC0::/10), il membro dell' **\_ \_ ID ambito sin6** nella struttura **sockaddr \_ IN6** è un identificatore di sito.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-107">For IPv6 site-local addresses (fec0::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is a site identifier.</span></span>

<span data-ttu-id="2b8ae-108">Di seguito è riportato un esempio di indirizzo IPv6 locale al collegamento nell'interfaccia \# 5:</span><span class="sxs-lookup"><span data-stu-id="2b8ae-108">An example of a link-local IPv6 address on interface \#5 is the following:</span></span>

``` syntax
fe80::208:74ff:feda:625c%5
```

<span data-ttu-id="2b8ae-109">Il seguente comando è disponibile in Windows XP con Service Pack 1 (SP1) e versioni successive per eseguire query e configurare IPv6 in un computer locale:</span><span class="sxs-lookup"><span data-stu-id="2b8ae-109">The following command is available on Windows XP with Service Pack 1 (SP1) and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="2b8ae-110">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="2b8ae-110">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="2b8ae-111">Le modifiche di configurazione apportate utilizzando i comandi Netsh.exe sono permanenti e non vengono perse quando il computer o il protocollo IPv6 viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-111">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="2b8ae-112">Prima di Windows XP con Service Pack 1 (SP1), la gestione e la configurazione di IPv6 utilizzavano diversi strumenti da riga di comando precedenti (Net.exe, Ipv6.exe e Ipsec6.exe) per la configurazione e la gestione di IPv6.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools (Net.exe, Ipv6.exe, and Ipsec6.exe) to configure and manage IPv6.</span></span> <span data-ttu-id="2b8ae-113">Utilizzando questi strumenti obsoleti, le modifiche IPv6 non sono permanenti e vengono perse quando il computer o il protocollo IPv6 è stato riavviato.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span> <span data-ttu-id="2b8ae-114">Questi strumenti da riga di comando precedenti sono supportati solo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-114">These older command-line tools are only supported on Windows XP.</span></span>

<span data-ttu-id="2b8ae-115">In Windows XP con SP1, il comando seguente visualizzerà l'elenco delle interfacce IPv6 in un computer locale, tra cui l'indice dell'interfaccia, il nome dell'interfaccia e diverse altre proprietà dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-115">On Windows XP with SP1, the following command will display the list of IPv6 interfaces on a local computer including the interface index, the interface name, and various other interface properties.</span></span>

<span data-ttu-id="2b8ae-116">**netsh interface ipv6 show interface**</span><span class="sxs-lookup"><span data-stu-id="2b8ae-116">**netsh interface ipv6 show interface**</span></span>

<span data-ttu-id="2b8ae-117">In Windows XP con SP1, il comando seguente modifica l'identificatore del sito associato a un indice di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-117">On Windows XP with SP1, the following command will change the site identifier associated with an interface index.</span></span>

<span data-ttu-id="2b8ae-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteID = value**</span><span class="sxs-lookup"><span data-stu-id="2b8ae-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid=value**</span></span>

<span data-ttu-id="2b8ae-119">In Windows XP il seguente comando precedente comporterà anche la modifica dell'identificatore del sito associato a un indirizzo locale del sito a 3.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-119">On Windows XP, the following older command will also change the site identifier associated with a site-local address to 3.</span></span>

<span data-ttu-id="2b8ae-120">**FEC0 RTU per IPv6::/10 3**</span><span class="sxs-lookup"><span data-stu-id="2b8ae-120">**ipv6 rtu fec0::/10 3**</span></span>

<span data-ttu-id="2b8ae-121">Se si invia o si connette a un indirizzo con ambito, il membro **dell' \_ \_ ID ambito sin6** nella struttura [**\_ IN6 di SOCKADDR**](sockaddr-2.md) può essere lasciato non specificato (zero) che rappresenta un indirizzo con ambito ambiguo.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-121">If you are sending or connecting to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure can be left unspecified (zero) which represents an ambiguous scoped address.</span></span> <span data-ttu-id="2b8ae-122">Ad esempio, il seguente indirizzo locale rispetto al collegamento è ambiguo:</span><span class="sxs-lookup"><span data-stu-id="2b8ae-122">For example, the following link-local address is ambiguous:</span></span>

``` syntax
fe80::10
```

<span data-ttu-id="2b8ae-123">Se si sta associando a un indirizzo con ambito, il membro dell' **\_ \_ ID ambito sin6** nella struttura [**sockaddr \_ IN6**](sockaddr-2.md) deve contenere un valore diverso da zero che specifica un numero di interfaccia valido per un indirizzo locale del collegamento o un identificatore di sito per un indirizzo locale del sito.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-123">If you are binding to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure must contain a nonzero value that specifies a valid interface number for a link-local address or a site identifier for a site-local address.</span></span>

## <a name="ambiguous-scoped-addresses"></a><span data-ttu-id="2b8ae-124">Indirizzi con ambito ambiguo</span><span class="sxs-lookup"><span data-stu-id="2b8ae-124">Ambiguous Scoped Addresses</span></span>

<span data-ttu-id="2b8ae-125">Se si sta inviando o eseguendo la connessione a un indirizzo con ambito e non è stato specificato il membro dell' **\_ \_ ID ambito sin6** nella struttura [**\_ IN6 di SOCKADDR**](sockaddr-2.md) , l'indirizzo con ambito è ambiguo.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-125">If you are sending or connecting to a scoped address and have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, then the scoped address is ambiguous.</span></span> <span data-ttu-id="2b8ae-126">Per risolvere questo problema, il protocollo IPv6 determina innanzitutto se il socket è stato associato a un indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-126">To resolve this, the IPv6 protocol first determines whether you have bound the socket to a source address.</span></span> <span data-ttu-id="2b8ae-127">In tal caso, l'indirizzo di origine associato risolve l'ambiguità fornendo un numero di interfaccia o un identificatore di sito.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-127">If so, the bound source address resolves the ambiguity by supplying an interface number or site identifier.</span></span>

<span data-ttu-id="2b8ae-128">Se si sta inviando o connettendosi a un indirizzo con ambito e non è stato specificato il membro dell' **\_ \_ ID ambito sin6** né associato un indirizzo di origine, il protocollo IPv6 controlla la tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-128">If you are sending or connecting to a scoped address and have neither specified the **sin6\_scope\_id** member nor bound a source address, then the IPv6 protocol checks the routing table.</span></span> <span data-ttu-id="2b8ae-129">Il comando seguente, ad esempio, visualizzerà la tabella di routing IPv6 in un computer locale:</span><span class="sxs-lookup"><span data-stu-id="2b8ae-129">For example, the following command will display the IPv6 routing table on a local computer:</span></span>

<span data-ttu-id="2b8ae-130">**netsh interface ipv6 show route**</span><span class="sxs-lookup"><span data-stu-id="2b8ae-130">**netsh interface ipv6 show route**</span></span>

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

<span data-ttu-id="2b8ae-131">Ciò indica che gli indirizzi locali al collegamento vengono considerati come on-link per l'interfaccia \# 13 e \# 14 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-131">This indicates that link-local addresses are treated as on-link to interface \#13 and \#14 by default.</span></span>

<span data-ttu-id="2b8ae-132">L'ambiguità si verifica quando un computer locale dispone di più schede di rete.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-132">Ambiguity arises when a local computer has multiple network adapters.</span></span> <span data-ttu-id="2b8ae-133">Ad esempio, il comando **netsh** precedente indica che sono presenti due interfacce di rete (connessione alla rete locale e connessione di rete wireless).</span><span class="sxs-lookup"><span data-stu-id="2b8ae-133">For example, the **netsh** command above indicates there are two network interfaces (Local Area Connection and Wireless Network Connection).</span></span> <span data-ttu-id="2b8ae-134">Quando un'applicazione specifica un indirizzo locale del collegamento di destinazione (ad esempio, FE80:: 10) senza un ID ambito, non è chiaro quale adapter usare per inviare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-134">When an application specifies a destination link-local address (fe80::10, for example) without a scope ID, it is not clear which adapter to use to send the packet.</span></span> <span data-ttu-id="2b8ae-135">Quando si invia un pacchetto, solo un indirizzo unicast locale del collegamento (FE80::/64) o un indirizzo di destinazione multicast con ambito di collegamento (FF00::/8) non può soffrire di un ID ambito.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-135">Only a link-local unicast (fe80::/64) or a link-scope multicast (ff00::/8) IPv6 destination address can suffer from not having a scope ID when sending a packet.</span></span>

## <a name="neighbor-discovery"></a><span data-ttu-id="2b8ae-136">Individuazione router adiacenti</span><span class="sxs-lookup"><span data-stu-id="2b8ae-136">Neighbor Discovery</span></span>

<span data-ttu-id="2b8ae-137">Se non è stato specificato il membro dell' **\_ \_ ID ambito sin6** nella [**struttura \_ IN6 di SOCKADDR**](sockaddr-2.md) , non è stato associato un indirizzo di origine e non è stata specificata una route per gli indirizzi locali al collegamento, il protocollo IPv6 tenterà l'individuazione Neighbor per risolvere l'indirizzo locale del collegamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-137">If you have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, have not bound a source address, and have not specified a route for link-local addresses, then the IPv6 protocol will try Neighbor Discovery to resolve the destination link-local address.</span></span> <span data-ttu-id="2b8ae-138">Per un pacchetto specifico inviato, viene tentata un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-138">For a given packet being sent, one interface is tried.</span></span> <span data-ttu-id="2b8ae-139">Questa prima interfaccia tentata è considerata l'interfaccia più preferita.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-139">This first interface that is tried is considered the most preferred interface.</span></span> <span data-ttu-id="2b8ae-140">Se l'individuazione vicina non riesce a risolvere l'indirizzo locale rispetto al collegamento in un'interfaccia, il pacchetto da inviare viene eliminato e il sistema ricorda che l'indirizzo locale del collegamento di destinazione non è raggiungibile tramite tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-140">If Neighbor Discovery fails to resolve the link-local address on an interface, the packet to be sent is dropped and the system remembers that the destination link-local address is not reachable over that interface.</span></span> <span data-ttu-id="2b8ae-141">Nel pacchetto successivo da inviare in tutte le stesse condizioni, viene tentata un'interfaccia diversa per l'individuazione dei router adiacenti.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-141">On the next packet to be sent under all of the same conditions, a different interface is tried for Neighbor Discovery.</span></span> <span data-ttu-id="2b8ae-142">Questo processo continua con ognuna delle interfacce in un computer locale per ogni nuovo pacchetto fino a quando non viene rilevata l'individuazione vicina per l'indirizzo locale del collegamento di destinazione o se tutte le interfacce possibili sono state tentate e non sono riuscite.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-142">This process continues through each of the interfaces on a local computer for each new packet until Neighbor Discovery responds for the destination link-local address or all of the possible interfaces have been tried and failed.</span></span> <span data-ttu-id="2b8ae-143">Ogni volta che un tentativo di risolvere il router adiacente ha esito negativo, viene eliminata un'interfaccia per quel router adiacente.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-143">Each time an attempt to resolve the neighbor fails, one interface is eliminated for that neighbor.</span></span>

<span data-ttu-id="2b8ae-144">Se l'indirizzo locale del collegamento di destinazione viene risolto, l'interfaccia viene usata per inviare il pacchetto corrente.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-144">If the destination link-local address resolves, then that interface is used to send the current packet.</span></span> <span data-ttu-id="2b8ae-145">Questa interfaccia viene usata anche per tutti i successivi pacchetti con ambito ambiguo che vengono inviati allo stesso indirizzo di destinazione locale rispetto al collegamento.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-145">This interface is also used for any subsequent ambiguously-scoped packets that are sent to the same link-local destination address.</span></span>

<span data-ttu-id="2b8ae-146">Se l'individuazione router adiacenti non riesce a risolvere l'indirizzo locale del collegamento di destinazione su tutte le interfacce, il sistema tenta di inviare il pacchetto sull'interfaccia preferita (la prima interfaccia è stata tentata).</span><span class="sxs-lookup"><span data-stu-id="2b8ae-146">If Neighbor Discovery fails to resolve the destination link-local address on all interfaces, the system then tries to send the packet on the most preferred interface (the first interface tried).</span></span> <span data-ttu-id="2b8ae-147">Lo stack di rete continua a provare a risolvere l'indirizzo locale del collegamento di destinazione sull'interfaccia più preferita.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-147">The network stack keeps trying to resolve the destination link-local address on the most preferred interface.</span></span> <span data-ttu-id="2b8ae-148">Dopo un periodo di tempo in cui l'individuazione dei router adiacenti ha avuto esito negativo su tutte le interfacce, lo stack di rete riavvierà nuovamente il processo e tenterà di risolvere l'indirizzo locale del collegamento di destinazione su tutte le interfacce.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-148">After a period of time after Neighbor Discovery has failed on all interfaces, the network stack will restart the process again and try to resolve the destination link-local address on all of the interfaces.</span></span> <span data-ttu-id="2b8ae-149">Attualmente, questo intervallo di tempo quando l'individuazione del router adiacente viene nuovamente tentata su tutte le interfacce è di 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-149">Currently, this time interval when Neighbor Discovery is again tried on all interfaces is 60 seconds.</span></span> <span data-ttu-id="2b8ae-150">Tuttavia, questo intervallo di tempo può cambiare nelle versioni di Windows e non deve essere presupposto da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-150">However, this time interval may change on versions of Windows and should not be assumed by an application.</span></span>

> [!Note]  
> <span data-ttu-id="2b8ae-151">Se un'applicazione associa lo stesso indirizzo locale al collegamento a un'interfaccia diversa dopo che l'individuazione del router adiacente ha risolto l'indirizzo locale rispetto al collegamento, che non eseguirà l'override dell'interfaccia con l'indirizzo di destinazione locale del collegamento restituito dall'individuazione vicina.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-151">If an application binds the same link-local address to a different interface after Neighbor Discovery has resolved the link-local address, that will not override the interface with the link-local destination address returned by Neighbor Discovery.</span></span>

 

<span data-ttu-id="2b8ae-152">Per ulteriori informazioni sull'individuazione dei router adiacenti per IP versione 6, vedere [RFC4861](https://tools.ietf.org/html/rfc4861) pubblicato da IETF.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-152">For more information on Neighbor Discovery for IP version 6, see [RFC4861](https://tools.ietf.org/html/rfc4861) published by the IETF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b8ae-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b8ae-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b8ae-154">Prefissi di sito IPv6</span><span class="sxs-lookup"><span data-stu-id="2b8ae-154">IPv6 Site Prefixes</span></span>](site-prefixes-2.md)
</dt> <dt>

[<span data-ttu-id="2b8ae-155">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="2b8ae-155">Ipv6.exe</span></span>](ipv6-exe-2.md)
</dt> <dt>

[<span data-ttu-id="2b8ae-156">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="2b8ae-156">Netsh.exe</span></span>](netsh-exe.md)
</dt> <dt>

[<span data-ttu-id="2b8ae-157">Utilizzo di IPv6</span><span class="sxs-lookup"><span data-stu-id="2b8ae-157">Using IPv6</span></span>](using-ipv6-2.md)
</dt> </dl>

 

 



