---
description: Per la prima configurazione non è necessaria alcuna configurazione aggiuntiva oltre all'installazione del protocollo Microsoft IPv6 Technology Preview.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Configurazione 1: singola subnet con indirizzi locali rispetto al collegamento'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049490"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a><span data-ttu-id="8e47c-103">Configurazione 1: singola subnet con indirizzi locali rispetto al collegamento</span><span class="sxs-lookup"><span data-stu-id="8e47c-103">Configuration 1: Single Subnet with Link-local Addresses</span></span>

<span data-ttu-id="8e47c-104">Per la prima configurazione non è necessaria alcuna configurazione aggiuntiva oltre all'installazione del protocollo Microsoft IPv6 Technology Preview.</span><span class="sxs-lookup"><span data-stu-id="8e47c-104">The first configuration requires no additional configuration beyond installing the Microsoft IPv6 Technology Preview protocol.</span></span> <span data-ttu-id="8e47c-105">Questa configurazione è costituita da almeno due nodi nella stessa subnet.</span><span class="sxs-lookup"><span data-stu-id="8e47c-105">This configuration consists of at least two nodes on the same subnet.</span></span> <span data-ttu-id="8e47c-106">Nella terminologia IPv6, i due nodi si trovano nello stesso collegamento senza router intermedi.</span><span class="sxs-lookup"><span data-stu-id="8e47c-106">In IPv6 terminology, the two nodes are on the same link with no intermediate routers.</span></span>

<span data-ttu-id="8e47c-107">Nella figura seguente viene illustrata la configurazione di due nodi in una singola subnet usando indirizzi locali al collegamento.</span><span class="sxs-lookup"><span data-stu-id="8e47c-107">The following illustration shows the configuration of two nodes on a single subnet using link-local addresses.</span></span>

![due nodi che usano indirizzi locali al collegamento.](images/v6mig-1.png)

<span data-ttu-id="8e47c-109">Per impostazione predefinita, IPv6 configura indirizzi IP locali al collegamento per ogni interfaccia corrispondente a schede di rete Ethernet installate.</span><span class="sxs-lookup"><span data-stu-id="8e47c-109">By default, IPv6 configures link-local IP addresses for each interface corresponding to installed Ethernet network adapters.</span></span> <span data-ttu-id="8e47c-110">Gli indirizzi locali al collegamento hanno il prefisso FE80::/64.</span><span class="sxs-lookup"><span data-stu-id="8e47c-110">Link-local addresses have the prefix fe80::/64.</span></span> <span data-ttu-id="8e47c-111">Gli ultimi 64 bit dell'indirizzo IPv6 sono noti come identificatori di interfaccia ed è derivato dall'indirizzo MAC a 48 bit della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="8e47c-111">The last 64 bits of the IPv6 address is known as the interface identifier and is derived from the 48-bit MAC address of the network adapter.</span></span>

<span data-ttu-id="8e47c-112">Per creare l'identificatore di interfaccia IPv6 dall'indirizzo MAC Ethernet a 48 bit (6 byte):</span><span class="sxs-lookup"><span data-stu-id="8e47c-112">To create the IPv6 interface identifier from the 48-bit (6-byte) Ethernet MAC address:</span></span>

-   <span data-ttu-id="8e47c-113">Le cifre esadecimali 0xFF-Fe vengono inserite tra il terzo e il quarto byte dell'indirizzo MAC.</span><span class="sxs-lookup"><span data-stu-id="8e47c-113">The hex digits 0xff-fe are inserted between the third and fourth byte of the MAC address.</span></span>
-   <span data-ttu-id="8e47c-114">Il bit universale/locale, il secondo bit di ordine inferiore del primo byte dell'indirizzo MAC, è complementare.</span><span class="sxs-lookup"><span data-stu-id="8e47c-114">The Universal/Local bit, the second low-order bit of the first byte of the MAC address, is complemented.</span></span> <span data-ttu-id="8e47c-115">Se è 1, viene convertito in 0 e, se è 0, viene trasformato in 1.</span><span class="sxs-lookup"><span data-stu-id="8e47c-115">If it is a 1, it is turned to 0, and if it is a 0, it is turned to 1.</span></span>

<span data-ttu-id="8e47c-116">Ad esempio, per l'indirizzo MAC 00-60-08-52-F9-D8:</span><span class="sxs-lookup"><span data-stu-id="8e47c-116">For example, for the MAC address 00-60-08-52-f9-d8:</span></span>

-   <span data-ttu-id="8e47c-117">Le cifre esadecimali 0xFF-Fe vengono inserite tra 0x08 (il terzo byte) e 0x52 (il quarto byte) dell'indirizzo MAC, formando l'indirizzo 64 bit 00-60-08-FF-FE-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="8e47c-117">The hex digits 0xff-fe are inserted between 0x08 (the third byte) and 0x52 (the fourth byte) of the MAC address, forming the 64-bit address 00-60-08-ff-fe-52-f9-d8.</span></span>
-   <span data-ttu-id="8e47c-118">Il bit universale/locale, il secondo bit di ordine inferiore di 0x00 (il primo byte) dell'indirizzo MAC è complementare.</span><span class="sxs-lookup"><span data-stu-id="8e47c-118">The Universal/Local bit, the second low-order bit of 0x00 (the first byte) of the MAC address is complemented.</span></span> <span data-ttu-id="8e47c-119">Il secondo bit di ordine inferiore di 0x00 è 0 che, quando complementato, diventa 1.</span><span class="sxs-lookup"><span data-stu-id="8e47c-119">The second low-order bit of 0x00 is 0 which, when complemented, becomes 1.</span></span> <span data-ttu-id="8e47c-120">Il risultato è che, per il primo byte, 0x00 diventa 0x02.</span><span class="sxs-lookup"><span data-stu-id="8e47c-120">The result is that for the first byte, 0x00 becomes 0x02.</span></span>

<span data-ttu-id="8e47c-121">Pertanto, l'identificatore di interfaccia IPv6 corrispondente all'indirizzo MAC Ethernet 00-60-08-52-F9-D8 è 02-60-08-FF-FE-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="8e47c-121">Therefore, the IPv6 interface identifier corresponding to the Ethernet MAC address of 00-60-08-52-f9-d8 is 02-60-08-ff-fe-52-f9-d8.</span></span>

<span data-ttu-id="8e47c-122">L'indirizzo locale del collegamento di un nodo è la combinazione del prefisso FE80::/64 e dell'identificatore di interfaccia a 64 bit espresso nella notazione esadecimale con due punti IPv6.</span><span class="sxs-lookup"><span data-stu-id="8e47c-122">The link-local address of a node is the combination of the prefix fe80::/64 and the 64-bit interface identifier expressed in IPv6 colon-hexadecimal notation.</span></span> <span data-ttu-id="8e47c-123">Pertanto, l'indirizzo locale rispetto al collegamento del nodo di esempio con il prefisso FE80::/64 e l'identificatore di interfaccia 02-60-08-FF-FE-52-F9-D8 è FE80:: 260:8FF: FE52: F9D8.</span><span class="sxs-lookup"><span data-stu-id="8e47c-123">Therefore, the link-local address of this example node with the prefix fe80::/64 and the interface identifier 02-60-08-ff-fe-52-f9-d8 is fe80::260:8ff:fe52:f9d8.</span></span>

<span data-ttu-id="8e47c-124">È possibile visualizzare l'indirizzo locale del collegamento usando IPv6 se, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="8e47c-124">You can view your link local address by using ipv6 if, as demonstrated in the following example:</span></span>

<span data-ttu-id="8e47c-125">**IPv6 se**</span><span class="sxs-lookup"><span data-stu-id="8e47c-125">**ipv6 if**</span></span>

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

<span data-ttu-id="8e47c-126">Interfaccia 4 è un'interfaccia corrispondente a una scheda Ethernet installata con un indirizzo locale rispetto al collegamento FE80:: 210:5AFF: FEAA: 20A2.</span><span class="sxs-lookup"><span data-stu-id="8e47c-126">Interface 4 is an interface corresponding to an installed Ethernet adapter with a link-local address of fe80::210:5aff:feaa:20a2.</span></span>

<span data-ttu-id="8e47c-127">Per ulteriori informazioni sull'indirizzamento IPv6 e una panoramica dei concetti relativi a IPv6, vedere Introduzione a IPv6 white paper.</span><span class="sxs-lookup"><span data-stu-id="8e47c-127">For more information on IPv6 addressing and an overview of IPv6 concepts, see the Introduction to IPv6 white paper.</span></span>

## <a name="testing-connectivity-between-two-link-local-hosts"></a><span data-ttu-id="8e47c-128">Test della connettività tra due host locali di collegamento</span><span class="sxs-lookup"><span data-stu-id="8e47c-128">Testing Connectivity Between Two Link-local Hosts</span></span>

<span data-ttu-id="8e47c-129">È possibile eseguire un semplice ping (uno scambio di messaggi di richiesta echo ICMPv6 e di risposta echo) usando IPv6 tra due host locali al collegamento.</span><span class="sxs-lookup"><span data-stu-id="8e47c-129">You can do a simple ping (an exchange of ICMPv6 Echo Request and Echo Reply messages) using IPv6 between two link-local hosts.</span></span>

<span data-ttu-id="8e47c-130">**Per eseguire il ping usando IPv6 tra due host locali al collegamento**</span><span class="sxs-lookup"><span data-stu-id="8e47c-130">**To ping using IPv6 between two link-local hosts**</span></span>

1.  <span data-ttu-id="8e47c-131">Installare Microsoft IPv6 Technology Preview per Windows in due host Windows (host A e host B) che si trovano nello stesso collegamento (subnet).</span><span class="sxs-lookup"><span data-stu-id="8e47c-131">Install the Microsoft IPv6 Technology Preview for Windows on two Windows hosts (Host A and Host B) that are on the same link (subnet).</span></span>
2.  <span data-ttu-id="8e47c-132">Usare IPv6 se sull'host a per ottenere l'indirizzo locale del collegamento per l'interfaccia Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8e47c-132">Use ipv6 if on Host A to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="8e47c-133">Esempio: l'indirizzo locale del collegamento dell'host A è FE80:: 210:5AFF: FEAA: 20A2.</span><span class="sxs-lookup"><span data-stu-id="8e47c-133">Example: The link-local address of Host A is fe80::210:5aff:feaa:20a2.</span></span>

3.  <span data-ttu-id="8e47c-134">Usare IPv6 se sull'host B per ottenere l'indirizzo locale del collegamento per l'interfaccia Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8e47c-134">Use ipv6 if on Host B to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="8e47c-135">Esempio: l'indirizzo locale del collegamento dell'host B è FE80:: 260:97FF: FE02:6EA5.</span><span class="sxs-lookup"><span data-stu-id="8e47c-135">Example: The link-local address of Host B is fe80::260:97ff:fe02:6ea5.</span></span>

4.  <span data-ttu-id="8e47c-136">Dall'host A eseguire il ping dell'host B utilizzando Ping6.exe.</span><span class="sxs-lookup"><span data-stu-id="8e47c-136">From Host A, ping Host B using Ping6.exe.</span></span>

    <span data-ttu-id="8e47c-137">Esempio: ping6 FE80:: 260:97FF: FE02:6EA5</span><span class="sxs-lookup"><span data-stu-id="8e47c-137">Example: ping6 fe80::260:97ff:fe02:6ea5</span></span>

<span data-ttu-id="8e47c-138">Per specificare l'indirizzo di origine da cui vengono inviati i messaggi di richiesta echo, è anche possibile usare l'opzione Ping6.exe-s.</span><span class="sxs-lookup"><span data-stu-id="8e47c-138">To specify the source address from which the Echo Request messages are sent, you can also use the Ping6.exe -s option.</span></span> <span data-ttu-id="8e47c-139">Ad esempio, per inviare richieste echo all'host B dall'indirizzo IPv6 di FE80:: 210:5AFF: FEAA: 20A2, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="8e47c-139">For example, to send Echo Requests to Host B from the IPv6 address of fe80::210:5aff:feaa:20a2, use the following command:</span></span>

<span data-ttu-id="8e47c-140">**ping6-s FE80:: 210:5AFF: FEAA: 20A2% 4 FE80:: 260:97FF: FE02:6EA5**</span><span class="sxs-lookup"><span data-stu-id="8e47c-140">**ping6 -s fe80::210:5aff:feaa:20a2%4 fe80::260:97ff:fe02:6ea5**</span></span>

<span data-ttu-id="8e47c-141">Quando si esegue il ping di un indirizzo locale rispetto al collegamento o al sito, è consigliabile specificare l'ID ambito in modo che l'indirizzo di destinazione non sia ambiguo.</span><span class="sxs-lookup"><span data-stu-id="8e47c-141">When pinging a link-local or site-local address, it is recommended to specify the scope-ID to make the destination address unambiguous.</span></span> <span data-ttu-id="8e47c-142">La notazione per specificare l'ID ambito è Address% scope-ID.</span><span class="sxs-lookup"><span data-stu-id="8e47c-142">The notation to specify the scope-ID is address%scope-ID.</span></span> <span data-ttu-id="8e47c-143">Per gli indirizzi locali al collegamento, l'ID ambito è uguale al numero di interfaccia visualizzato nel comando IPv6 if.</span><span class="sxs-lookup"><span data-stu-id="8e47c-143">For link-local addresses, the scope-ID is equal to the interface number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="8e47c-144">Per gli indirizzi locali del sito, l'ID ambito è uguale al numero del sito come visualizzato nel comando IPv6 if.</span><span class="sxs-lookup"><span data-stu-id="8e47c-144">For site-local addresses, the scope-ID is equal to the site number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="8e47c-145">Ad esempio, per inviare messaggi di richiesta echo all'host B utilizzando l'ID ambito 4, utilizzare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="8e47c-145">For example, to send Echo Request messages to Host B using scope-ID 4, use the following command:</span></span>

<span data-ttu-id="8e47c-146">**ping6 FE80:: 260:97FF: FE02:6EA5% 4**</span><span class="sxs-lookup"><span data-stu-id="8e47c-146">**ping6 fe80::260:97ff:fe02:6ea5%4**</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e47c-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e47c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e47c-148">Configurazioni consigliate per IPv6</span><span class="sxs-lookup"><span data-stu-id="8e47c-148">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> </dl>

 

 



