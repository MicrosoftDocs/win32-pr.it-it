---
description: 6to4 è un metodo per la connessione di host o siti IPv6 tramite l'infrastruttura Internet IPv4 esistente.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Configurazione 2: traffico IPv6 tra nodi in subnet diverse di un Internet (6to4) IPv4'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1abd5477005e6a1e71c13aaf19a734e9191097d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484949"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a><span data-ttu-id="51fa6-103">Configurazione 2: traffico IPv6 tra nodi in subnet diverse di un Internet (6to4) IPv4</span><span class="sxs-lookup"><span data-stu-id="51fa6-103">Configuration 2: IPv6 Traffic Between Nodes on Different Subnets of an IPv4 Internetwork (6to4)</span></span>

<span data-ttu-id="51fa6-104">6to4 è un metodo per la connessione di host o siti IPv6 tramite l'infrastruttura Internet IPv4 esistente.</span><span class="sxs-lookup"><span data-stu-id="51fa6-104">6to4 is a method for connecting IPv6 hosts or sites over the existing IPv4 Internet infrastructure.</span></span> <span data-ttu-id="51fa6-105">Usa un prefisso di indirizzo univoco per fornire ai siti IPv6 isolati il proprio spazio di indirizzi IPv6.</span><span class="sxs-lookup"><span data-stu-id="51fa6-105">It uses a unique address prefix to give isolated IPv6 sites their own IPv6 address space.</span></span> <span data-ttu-id="51fa6-106">6to4 è come uno "pseudo-ISP" che fornisce la connettività IPv6.</span><span class="sxs-lookup"><span data-stu-id="51fa6-106">6to4 is like a "pseudo-ISP" providing IPv6 connectivity.</span></span> <span data-ttu-id="51fa6-107">È possibile utilizzare 6to4 per comunicare direttamente con altri siti 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-107">You can use 6to4 to communicate directly with other 6to4 sites.</span></span> <span data-ttu-id="51fa6-108">6to4 non richiede l'utilizzo di router IPv6 e il traffico IPv6 è incapsulato con un'intestazione IPv4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-108">6to4 does not require the use of IPv6 routers and its IPv6 traffic is encapsulated with an IPv4 header.</span></span>

<span data-ttu-id="51fa6-109">Nella figura seguente viene illustrata la configurazione di due nodi in subnet separate mediante 6to4 per la comunicazione attraverso un router IPv4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-109">The following illustration shows the configuration of two nodes on separate subnets using 6to4 to communicate across an IPv4 router.</span></span>

![nodi che usano 6to4 per comunicare attraverso un router IPv4.](images/v6mig-2.png)

<span data-ttu-id="51fa6-111">Il requisito principale per l'utilizzo di 6to4 è un indirizzo IPv4 instradabile a livello globale per il sito.</span><span class="sxs-lookup"><span data-stu-id="51fa6-111">The main requirement for using 6to4 is one globally routable IPv4 address for your site.</span></span> <span data-ttu-id="51fa6-112">Si supponga che il sito sia costituito da una raccolta di computer IPv6 gestiti (alcuni eseguono il protocollo IPv6 Microsoft e altre implementazioni IPv6).</span><span class="sxs-lookup"><span data-stu-id="51fa6-112">Suppose that your site consists of a collection of IPv6 computers that you manage (some running the Microsoft IPv6 protocol and some running other IPv6 implementations).</span></span> <span data-ttu-id="51fa6-113">Si supponga inoltre che tutti i computer IPv6 siano connessi direttamente tramite Ethernet o 6-over-4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-113">Assume also that all IPv6 computers are directly connected using Ethernet or 6-over-4.</span></span> <span data-ttu-id="51fa6-114">L'indirizzo IPv4 instradabile a livello globale deve essere assegnato a uno dei computer in cui è in esecuzione il protocollo IPv6 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="51fa6-114">The globally routable IPv4 address must be assigned to one of your computers running the Microsoft IPv6 protocol.</span></span> <span data-ttu-id="51fa6-115">Il computer sarà il gateway 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-115">This computer will be your 6to4 gateway.</span></span>

<span data-ttu-id="51fa6-116">Se si dispone di un indirizzo IPv4 che fa parte dello spazio di indirizzi privato (10.0.0.0/8, 172.16.0.0/12 o 192.168.0.0/16) o dello spazio di indirizzi APIPA (Automatic Private IP Addressing) di 169.254.0.0/16 usato da Windows 2000, non è instradabile a livello globale.</span><span class="sxs-lookup"><span data-stu-id="51fa6-116">If you have an IPv4 address that is part of the private address space (10.0.0.0/8, 172.16.0.0/12, or 192.168.0.0/16) or the Automatic Private IP Addressing (APIPA) address space of 169.254.0.0/16 used by Windows 2000, it is not globally routable.</span></span> <span data-ttu-id="51fa6-117">In caso contrario, si tratta probabilmente di un indirizzo IP pubblico ed è instradabile a livello globale.</span><span class="sxs-lookup"><span data-stu-id="51fa6-117">Otherwise, it is probably a public IP address and is globally routable.</span></span> <span data-ttu-id="51fa6-118">Per ulteriori informazioni su come determinare se la connessione ISP supporta 6to4, vedere l'argomento [debug di configurazione 6to4](#debugging-6to4-configuration) in questo documento.</span><span class="sxs-lookup"><span data-stu-id="51fa6-118">See the [Debugging 6to4 Configuration](#debugging-6to4-configuration) topic in this document for more help in determining whether your ISP connection supports 6to4.</span></span>

## <a name="the-6to4cfgexe-tool"></a><span data-ttu-id="51fa6-119">Strumento 6to4cfg.exe</span><span class="sxs-lookup"><span data-stu-id="51fa6-119">The 6to4cfg.exe Tool</span></span>

<span data-ttu-id="51fa6-120">Lo strumento 6to4cfg.exe automatizza la configurazione 6to4, individuando automaticamente l'indirizzo IPv4 instradabile a livello globale e creando un prefisso 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-120">The 6to4cfg.exe tool automates 6to4 configuration, automatically discovering your globally routable IPv4 address and creating a 6to4 prefix.</span></span> <span data-ttu-id="51fa6-121">Esegue direttamente la configurazione oppure può scrivere uno script di configurazione che può essere ispezionato ed eseguito in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="51fa6-121">It either performs the configuration directly, or it can write a configuration script that you can inspect and run later.</span></span>

<span data-ttu-id="51fa6-122">Di seguito è riportata la sintassi di base del comando 6to4cfg.exe.</span><span class="sxs-lookup"><span data-stu-id="51fa6-122">The basic 6to4cfg.exe command syntax is as follows.</span></span>

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span data-ttu-id="51fa6-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*filename*\]</span><span class="sxs-lookup"><span data-stu-id="51fa6-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*filename*\]</span></span>
</dt> <dd>

<span data-ttu-id="51fa6-124">Scrive lo script di configurazione in un file, se si specifica un nome file.</span><span class="sxs-lookup"><span data-stu-id="51fa6-124">Writes the configuration script to a file, if you specify a file name.</span></span> <span data-ttu-id="51fa6-125">Lo script di configurazione utilizza Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="51fa6-125">The configuration script uses Ipv6.exe.</span></span>

<span data-ttu-id="51fa6-126">È possibile specificare con per il nome file per scrivere lo script di configurazione nell'output della console, che risulta utile per vedere quali 6to4cfg.exe eseguiranno in uno scenario di test.</span><span class="sxs-lookup"><span data-stu-id="51fa6-126">You can specify con for the file name to write the configuration script to console output, which is useful for seeing what 6to4cfg.exe will do in a test scenario.</span></span>

<span data-ttu-id="51fa6-127">Se non si specifica un nome di file, 6to4cfg.exe aggiorna direttamente la configurazione IPv6 nel computer.</span><span class="sxs-lookup"><span data-stu-id="51fa6-127">If you do not specify a file name, 6to4cfg.exe directly updates the IPv6 configuration on your computer.</span></span>

</dd> <dt>

<span data-ttu-id="51fa6-128"><span id="-r"></span><span id="-R"></span>-r</span><span class="sxs-lookup"><span data-stu-id="51fa6-128"><span id="-r"></span><span id="-R"></span>-r</span></span>
</dt> <dd>

<span data-ttu-id="51fa6-129">Diventa un router del gateway 6to4 per la rete locale, abilitando il routing su tutte le interfacce e i prefissi di subnet assegnati.</span><span class="sxs-lookup"><span data-stu-id="51fa6-129">Becomes a 6to4 gateway router for your local network, enabling routing on all of your interfaces and assigned subnet prefixes.</span></span>

</dd> <dt>

<span data-ttu-id="51fa6-130"><span id="-s"></span><span id="-S"></span>-s</span><span class="sxs-lookup"><span data-stu-id="51fa6-130"><span id="-s"></span><span id="-S"></span>-s</span></span>
</dt> <dd>

<span data-ttu-id="51fa6-131">Abilita l'indirizzamento locale del sito nel sito 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-131">Enables site-local addressing in your 6to4 site.</span></span> <span data-ttu-id="51fa6-132">Questo comando è utile solo se utilizzato in combinazione con-r.</span><span class="sxs-lookup"><span data-stu-id="51fa6-132">This command is only useful when used in conjunction with -r.</span></span>

</dd> <dt>

<span data-ttu-id="51fa6-133"><span id="-u"></span><span id="-U"></span>-u</span><span class="sxs-lookup"><span data-stu-id="51fa6-133"><span id="-u"></span><span id="-U"></span>-u</span></span>
</dt> <dd>

<span data-ttu-id="51fa6-134">Specifica che la configurazione 6to4 deve essere invertita.</span><span class="sxs-lookup"><span data-stu-id="51fa6-134">Specifies that the 6to4 configuration be reversed.</span></span> <span data-ttu-id="51fa6-135">Pertanto 6to4cfg-u inverte l'effetto di 6to4cfg e 6to4cfg-r-u inverte l'effetto di 6to4cfg-r e così via.</span><span class="sxs-lookup"><span data-stu-id="51fa6-135">Therefore 6to4cfg -u reverses the effect of 6to4cfg and 6to4cfg -r -u reverses the effect of 6to4cfg -r, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="51fa6-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>- *Inoltro* R</span><span class="sxs-lookup"><span data-stu-id="51fa6-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *relay*</span></span>
</dt> <dd>

<span data-ttu-id="51fa6-137">Specifica il nome o l'indirizzo IPv4 di un router di inoltro 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-137">Specifies the name or IPv4 address of a 6to4 relay router.</span></span> <span data-ttu-id="51fa6-138">Il nome predefinito è 6to4.ipv6.microsoft.com, il router di inoltro 6to4 su Internet.</span><span class="sxs-lookup"><span data-stu-id="51fa6-138">The default name is 6to4.ipv6.microsoft.com, the 6to4 relay router on the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="51fa6-139"><span id="-b"></span><span id="-B"></span>-b</span><span class="sxs-lookup"><span data-stu-id="51fa6-139"><span id="-b"></span><span id="-B"></span>-b</span></span>
</dt> <dd>

<span data-ttu-id="51fa6-140">Specifica che 6to4cfg.exe seleziona l'indirizzo di inoltro "migliore" anziché il primo.</span><span class="sxs-lookup"><span data-stu-id="51fa6-140">Specifies that 6to4cfg.exe picks the "best" relay address instead of the first.</span></span>

</dd> <dt>

<span data-ttu-id="51fa6-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *Indirizzo*</span><span class="sxs-lookup"><span data-stu-id="51fa6-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *address*</span></span>
</dt> <dd>

<span data-ttu-id="51fa6-142">Specifica l'indirizzo IPv4 locale per il prefisso 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-142">Specifies the local IPv4 address for the 6to4 prefix.</span></span>

</dd> </dl>

## <a name="manual-6to4-configuration"></a><span data-ttu-id="51fa6-143">Configurazione di 6to4 manuale</span><span class="sxs-lookup"><span data-stu-id="51fa6-143">Manual 6to4 Configuration</span></span>

<span data-ttu-id="51fa6-144">In questo esempio l'indirizzo del gateway 6to4 è 172.31.42.239.</span><span class="sxs-lookup"><span data-stu-id="51fa6-144">In this example the address of the 6to4 gateway is 172.31.42.239.</span></span> <span data-ttu-id="51fa6-145">Per usare 6to4, è necessario un indirizzo IPv4 instradabile a livello globale.</span><span class="sxs-lookup"><span data-stu-id="51fa6-145">You need your own globally routable IPv4 address to use 6to4.</span></span>

> [!Note]  
> <span data-ttu-id="51fa6-146">L'indirizzo IP 172.31.42.239 viene usato solo a scopo esemplificativo.</span><span class="sxs-lookup"><span data-stu-id="51fa6-146">The IP address 172.31.42.239 is used for example purposes only.</span></span> <span data-ttu-id="51fa6-147">Si tratta di un indirizzo privato e non è instradabile a livello globale su Internet.</span><span class="sxs-lookup"><span data-stu-id="51fa6-147">This is a private address and is not globally routable on the Internet.</span></span>

 

<span data-ttu-id="51fa6-148">L'indirizzo IPv4 instradabile a 32 bit viene combinato con il prefisso 2002::/16 a 16 bit per formare un prefisso di indirizzo IPv6 a 48 bit per il sito.</span><span class="sxs-lookup"><span data-stu-id="51fa6-148">The 32-bit globally routable IPv4 address is combined with the 16-bit prefix 2002::/16 to form a 48-bit IPv6 address prefix for your site.</span></span> <span data-ttu-id="51fa6-149">In questo esempio, il prefisso del sito 6to4 è 2002: ac1f: 2AEF::/48.</span><span class="sxs-lookup"><span data-stu-id="51fa6-149">In this example, the 6to4 site prefix is 2002:ac1f:2aef::/48.</span></span> <span data-ttu-id="51fa6-150">Si noti che ac1f: 2AEF è la codifica esadecimale di 172.31.42.239 (ovviamente, si userà un prefisso diverso in base all'indirizzo IPv4 instradabile a livello globale).</span><span class="sxs-lookup"><span data-stu-id="51fa6-150">Note that ac1f:2aef is the hexadecimal encoding of 172.31.42.239 (of course, you will use a different prefix based on your own globally routable IPv4 address).</span></span> <span data-ttu-id="51fa6-151">Utilizzando il prefisso del sito 6to4, è possibile assegnare indirizzi e prefissi di subnet all'interno del sito.</span><span class="sxs-lookup"><span data-stu-id="51fa6-151">Using the 6to4 site prefix, you can assign addresses and subnet prefixes inside your site.</span></span>

<span data-ttu-id="51fa6-152">Questo esempio presuppone che si usi la subnet 0 per configurare manualmente un indirizzo 6to4 nel computer gateway 6to4 e che si usi la subnet 1 per la configurazione automatica degli indirizzi nel segmento di rete Ethernet.</span><span class="sxs-lookup"><span data-stu-id="51fa6-152">This example assumes that you use subnet 0 for manually configuring a 6to4 address on your 6to4 gateway computer and that you use subnet 1 for automatically configuring addresses on your Ethernet network segment.</span></span> <span data-ttu-id="51fa6-153">Sono tuttavia possibili altre scelte.</span><span class="sxs-lookup"><span data-stu-id="51fa6-153">However, other choices are possible.</span></span>

1.  <span data-ttu-id="51fa6-154">Utilizzare Ipv6.exe per abilitare 6to4 nel computer gateway 6to4:</span><span class="sxs-lookup"><span data-stu-id="51fa6-154">Use Ipv6.exe to enable 6to4 on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="51fa6-155">**RTU 2002::/16 2 IPv6**</span><span class="sxs-lookup"><span data-stu-id="51fa6-155">**ipv6 rtu 2002::/16 2**</span></span>

    <span data-ttu-id="51fa6-156">Il comando **RTU IPv6** esegue un aggiornamento della tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="51fa6-156">The **ipv6 rtu** command performs a routing table update.</span></span> <span data-ttu-id="51fa6-157">Può essere usato per aggiungere, rimuovere o aggiornare una route.</span><span class="sxs-lookup"><span data-stu-id="51fa6-157">It can be used to add, remove, or update a route.</span></span> <span data-ttu-id="51fa6-158">In questo caso viene abilitato 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-158">In this case it is enabling 6to4.</span></span>

    <span data-ttu-id="51fa6-159">L'argomento 2002::/16 è il prefisso della route, che specifica il prefisso 6to4 univoco.</span><span class="sxs-lookup"><span data-stu-id="51fa6-159">The 2002::/16 argument is the prefix of the route, specifying the unique 6to4 prefix.</span></span>

    <span data-ttu-id="51fa6-160">L'argomento 2 specifica l'interfaccia in collegamento per questo prefisso.</span><span class="sxs-lookup"><span data-stu-id="51fa6-160">The 2 argument specifies the on-link interface for this prefix.</span></span> <span data-ttu-id="51fa6-161">\#L'interfaccia 2 è la "pseudo-interfaccia" usata per i tunnel configurati, il tunneling automatico e 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-161">Interface \#2 is the "pseudo-interface" used for configured tunnels, automatic tunneling, and 6to4.</span></span> <span data-ttu-id="51fa6-162">Quando un indirizzo di destinazione IPv6 corrisponde al prefisso 2002::/16, vengono estratti i 32 bit che seguono il prefisso nell'indirizzo di destinazione per formare un indirizzo di destinazione IPv4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-162">When an IPv6 destination address matches the 2002::/16 prefix, the 32 bits that follow the prefix in the destination address are extracted to form an IPv4 destination address.</span></span> <span data-ttu-id="51fa6-163">Il pacchetto viene incapsulato con un'intestazione IPv4 e inviato all'indirizzo di destinazione IPv4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-163">The packet is encapsulated with an IPv4 header and sent to the IPv4 destination address.</span></span>

2.  <span data-ttu-id="51fa6-164">Configurare un indirizzo 6to4 nel computer gateway 6to4:</span><span class="sxs-lookup"><span data-stu-id="51fa6-164">Configure a 6to4 address on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="51fa6-165">**IPv6 Adu 2/2002: ac1f: 2AEF:: ac1f: 2AEF**</span><span class="sxs-lookup"><span data-stu-id="51fa6-165">**ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef**</span></span>

    <span data-ttu-id="51fa6-166">Il comando **Adu di IPv6** esegue un aggiornamento degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="51fa6-166">The **ipv6 adu** command performs an address update.</span></span> <span data-ttu-id="51fa6-167">Può essere usato per aggiungere, rimuovere o aggiornare un indirizzo in un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="51fa6-167">It can be used to add, remove, or update an address on an interface.</span></span> <span data-ttu-id="51fa6-168">In questa istanza viene configurato l'indirizzo 6to4 del computer.</span><span class="sxs-lookup"><span data-stu-id="51fa6-168">In this instance, it is configuring the computer's 6to4 address.</span></span>

    <span data-ttu-id="51fa6-169">L'argomento 2/2002: ac1f: 2AEF:: ac1f: 2AEF specifica sia l'interfaccia che l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="51fa6-169">The 2/2002:ac1f:2aef::ac1f:2aef argument specifies both the interface and the address.</span></span> <span data-ttu-id="51fa6-170">È necessario configurare Address 2002: ac1f: 2AEF:: ac1f: 2AEF sull'interfaccia \# 2.</span><span class="sxs-lookup"><span data-stu-id="51fa6-170">It requires configuring address 2002:ac1f:2aef::ac1f:2aef on interface \#2.</span></span> <span data-ttu-id="51fa6-171">L'indirizzo viene creato usando il prefisso del sito 2002: ac1f: 2AEF::/48, subnet 0 per assegnare un prefisso di subnet 2002: ac1f: 2AEF::/64 e un identificatore di interfaccia a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="51fa6-171">The address is created using the site prefix 2002:ac1f:2aef::/48, subnet 0 to give a subnet prefix 2002:ac1f:2aef::/64, and a 64-bit interface identifier.</span></span> <span data-ttu-id="51fa6-172">La convenzione illustrata usa l'indirizzo IPv4 del computer per l'identificatore di interfaccia per gli indirizzi assegnati all'interfaccia \# 2.</span><span class="sxs-lookup"><span data-stu-id="51fa6-172">The convention demonstrated uses the computer's IPv4 address for the interface identifier for addresses assigned to interface \#2.</span></span> <span data-ttu-id="51fa6-173">Per l'uso, ac1f: 2AEF deve essere sostituito dalla codifica esadecimale dell'indirizzo IPv4 instradabile a livello globale.</span><span class="sxs-lookup"><span data-stu-id="51fa6-173">For your use, ac1f:2aef should be replaced by the hexadecimal encoding of your own globally routable IPv4 address.</span></span>

<span data-ttu-id="51fa6-174">I due comandi precedenti sono sufficienti per consentire la comunicazione con altri siti 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-174">The two preceding commands are sufficient to allow communication with other 6to4 sites.</span></span> <span data-ttu-id="51fa6-175">Ad esempio, è possibile provare a effettuare il ping del sito Microsoft 6to4:</span><span class="sxs-lookup"><span data-stu-id="51fa6-175">For example, you can try pinging the Microsoft 6to4 site:</span></span>

<span data-ttu-id="51fa6-176">**ping6 2002:836b: 9820:: 836b: 9820**</span><span class="sxs-lookup"><span data-stu-id="51fa6-176">**ping6 2002:836b:9820::836b:9820**</span></span>

<span data-ttu-id="51fa6-177">Per abilitare la comunicazione con backbone 6bone, è necessario creare un tunnel configurato predefinito per un inoltro 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-177">To enable communication with the 6bone, you must create a default configured tunnel to a 6to4 relay.</span></span> <span data-ttu-id="51fa6-178">È possibile utilizzare il router di inoltro Microsoft 6to4, 131.107.152.32:</span><span class="sxs-lookup"><span data-stu-id="51fa6-178">You can use the Microsoft 6to4 relay router, 131.107.152.32:</span></span>

<span data-ttu-id="51fa6-179">**RTU IPv6::/0 2/:: 131.107.152.32 pub vita 1800**</span><span class="sxs-lookup"><span data-stu-id="51fa6-179">**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**</span></span>

<span data-ttu-id="51fa6-180">Il comando **RTU IPv6** esegue un aggiornamento della tabella di routing, stabilendo, in questa istanza, una route predefinita al relay 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-180">The **ipv6 rtu** command performs a routing table update, establishing, in this instance, a default route to the 6to4 relay.</span></span>

<span data-ttu-id="51fa6-181">L'argomento::/0 è il prefisso della route.</span><span class="sxs-lookup"><span data-stu-id="51fa6-181">The ::/0 argument is the route prefix.</span></span> <span data-ttu-id="51fa6-182">Il prefisso di lunghezza zero indica che si tratta di una route predefinita.</span><span class="sxs-lookup"><span data-stu-id="51fa6-182">The zero-length prefix indicates that it is a default route.</span></span>

<span data-ttu-id="51fa6-183">L'argomento 2/:: 131.107.152.32 specifica il prossimo hop successivo per questo prefisso.</span><span class="sxs-lookup"><span data-stu-id="51fa6-183">The 2/::131.107.152.32 argument specifies the next-hop neighbor for this prefix.</span></span> <span data-ttu-id="51fa6-184">Richiede che i pacchetti corrispondenti al prefisso vengano inoltrati a address:: 131.107.152.32 usando Interface \# 2.</span><span class="sxs-lookup"><span data-stu-id="51fa6-184">It requires that packets matching the prefix are forwarded to address ::131.107.152.32 using interface \#2.</span></span> <span data-ttu-id="51fa6-185">L'invio di un pacchetto a:: 131.107.152.32 sull'interfaccia \# 2 ne determina l'incapsulamento con un'intestazione V4 e l'invio a 131.107.152.32.</span><span class="sxs-lookup"><span data-stu-id="51fa6-185">Forwarding a packet to ::131.107.152.32 on interface \#2 causes it to be encapsulated with a v4 header and sent to 131.107.152.32.</span></span>

<span data-ttu-id="51fa6-186">L'argomento pub rende questa una route pubblicata.</span><span class="sxs-lookup"><span data-stu-id="51fa6-186">The pub argument makes this a published route.</span></span> <span data-ttu-id="51fa6-187">Poiché questo è pertinente solo per i router, non ha alcun effetto fino a quando non viene abilitato il routing.</span><span class="sxs-lookup"><span data-stu-id="51fa6-187">Because this is only relevant for routers, it has no effect until routing is enabled.</span></span> <span data-ttu-id="51fa6-188">Analogamente, la durata di 30 minuti riguarda solo se il routing è abilitato.</span><span class="sxs-lookup"><span data-stu-id="51fa6-188">Similarly, the 30-minute lifetime pertains only if routing is enabled.</span></span>

<span data-ttu-id="51fa6-189">Dovrebbe essere possibile accedere ai siti di backbone 6bone e ai siti 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-189">You should be able to access 6bone sites as well as 6to4 sites.</span></span> <span data-ttu-id="51fa6-190">Per eseguire il test, è possibile usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="51fa6-190">You can use the following command to test this:</span></span>

<span data-ttu-id="51fa6-191">**ping6 3FFE: 1CFF: 0: F5:: 1**</span><span class="sxs-lookup"><span data-stu-id="51fa6-191">**ping6 3ffe:1cff:0:f5::1**</span></span>

<span data-ttu-id="51fa6-192">Il passaggio finale consiste nell'abilitare il routing sul gateway 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-192">The final step is to enable routing on your 6to4 gateway.</span></span> <span data-ttu-id="51fa6-193">Questo esempio si basa sul presupposto che l'interfaccia \# 3 sul computer gateway sia un'interfaccia Ethernet e che l'interfaccia \# 4 sia 6-over-4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-193">This example assumes that interface \#3 on your gateway computer is an Ethernet interface and interface \#4 is 6-over-4.</span></span> <span data-ttu-id="51fa6-194">Il computer potrebbe numerare le interfacce in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="51fa6-194">Your computer might number its interfaces differently.</span></span> <span data-ttu-id="51fa6-195">I due comandi seguenti assegnano i prefissi di subnet ai due collegamenti.</span><span class="sxs-lookup"><span data-stu-id="51fa6-195">The following two commands assign subnet prefixes to the two links.</span></span> <span data-ttu-id="51fa6-196">I prefissi di subnet sono derivati dal prefisso 6to4 del sito 2002: ac1f: 2AEF::/48:</span><span class="sxs-lookup"><span data-stu-id="51fa6-196">The subnet prefixes are derived from the site's 6to4 prefix 2002:ac1f:2aef::/48:</span></span>

<span data-ttu-id="51fa6-197">**IPv6 RTU 2002: ac1f: 2AEF: 1::/64 3 pub vita 1800**</span><span class="sxs-lookup"><span data-stu-id="51fa6-197">**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**</span></span>

<span data-ttu-id="51fa6-198">**IPv6 RTU 2002: ac1f: 2AEF: 2::/64 4 pub vita 1800**</span><span class="sxs-lookup"><span data-stu-id="51fa6-198">**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**</span></span>

<span data-ttu-id="51fa6-199">Il comando **RTU IPv6** specifica che il prefisso 2002: ac1f: 2AEF: 1::/64 è in collegamento all'interfaccia \# 3.</span><span class="sxs-lookup"><span data-stu-id="51fa6-199">The **ipv6 rtu** command specifies that the prefix 2002:ac1f:2aef:1::/64 is on-link to interface \#3.</span></span> <span data-ttu-id="51fa6-200">Viene configurato il prefisso della prima subnet sull'interfaccia Ethernet.</span><span class="sxs-lookup"><span data-stu-id="51fa6-200">It is configuring the first subnet prefix on the Ethernet interface.</span></span> <span data-ttu-id="51fa6-201">La route viene pubblicata con una durata di 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="51fa6-201">The route is published with a lifetime of 30 minutes.</span></span>

<span data-ttu-id="51fa6-202">Analogamente, il prefisso 2002: ac1f: 2AEF: 2::/64 è configurato sull'interfaccia 6-over-4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-202">Similarly, the 2002:ac1f:2aef:2::/64 prefix is configured on the 6-over-4 interface.</span></span>

<span data-ttu-id="51fa6-203">I tre comandi successivi abilitano il funzionamento del computer gateway 6to4 come router:</span><span class="sxs-lookup"><span data-stu-id="51fa6-203">The next three commands enable the 6to4 gateway computer to function as a router:</span></span>

<span data-ttu-id="51fa6-204">**FORW IFC 2 IPv6**</span><span class="sxs-lookup"><span data-stu-id="51fa6-204">**ipv6 ifc 2 forw**</span></span>

<span data-ttu-id="51fa6-205">**FORW ADV di IPv6 IFC 3**</span><span class="sxs-lookup"><span data-stu-id="51fa6-205">**ipv6 ifc 3 forw adv**</span></span>

<span data-ttu-id="51fa6-206">**FORW ADV IPv6 IFC 4**</span><span class="sxs-lookup"><span data-stu-id="51fa6-206">**ipv6 ifc 4 forw adv**</span></span>

<span data-ttu-id="51fa6-207">Il comando **IFC IPv6** controlla gli attributi di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="51fa6-207">The **ipv6 ifc** command controls attributes of an interface.</span></span> <span data-ttu-id="51fa6-208">Un router inoltra i pacchetti e invia annunci router.</span><span class="sxs-lookup"><span data-stu-id="51fa6-208">A router forwards packets and sends router advertisements.</span></span> <span data-ttu-id="51fa6-209">Nell'implementazione di Microsoft IPv6, questi attributi per interfaccia sono controllati separatamente.</span><span class="sxs-lookup"><span data-stu-id="51fa6-209">In the Microsoft IPv6 implementation, these per-interface attributes are controlled separately.</span></span>

<span data-ttu-id="51fa6-210">\#L'interfaccia 2 non è necessaria per la pubblicità perché si tratta di una pseudo-interfaccia.</span><span class="sxs-lookup"><span data-stu-id="51fa6-210">Interface \#2 is not needed for advertising because it is a pseudo-interface.</span></span>

<span data-ttu-id="51fa6-211">Se il computer dispone di interfacce aggiuntive, è necessario configurarle anche per l'invio e la pubblicità.</span><span class="sxs-lookup"><span data-stu-id="51fa6-211">If your computer has additional interfaces, they should also be configured to be forwarding and advertising.</span></span>

<span data-ttu-id="51fa6-212">Dopo l'esecuzione di questi comandi, il protocollo IPv6 Microsoft configurerà automaticamente gli indirizzi sulle interfacce \# 3 e \# 4 usando i rispettivi prefissi di subnet e le due interfacce inizieranno a inviare annunci router a intervalli approssimativamente da 3 a 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="51fa6-212">After running these commands, the Microsoft IPv6 protocol will automatically configure addresses on interfaces \#3 and \#4 using the respective subnet prefixes and the two interfaces will start sending router advertisements at approximately 3 to 10 minute intervals.</span></span>

<span data-ttu-id="51fa6-213">Gli host che ricevono questi annunci router si configureranno automaticamente con una route predefinita e un indirizzo 6to4 derivato dal prefisso della subnet del collegamento.</span><span class="sxs-lookup"><span data-stu-id="51fa6-213">Hosts receiving these router advertisements will automatically configure themselves with a default route and a 6to4 address derived from the subnet prefix of their link.</span></span> <span data-ttu-id="51fa6-214">Avranno la comunicazione con altri siti 6to4 e backbone 6bone tramite il computer gateway.</span><span class="sxs-lookup"><span data-stu-id="51fa6-214">They will have communication to other 6to4 sites and the 6bone through the gateway computer.</span></span>

## <a name="debugging-6to4-configuration"></a><span data-ttu-id="51fa6-215">Debug della configurazione 6to4</span><span class="sxs-lookup"><span data-stu-id="51fa6-215">Debugging 6to4 Configuration</span></span>

<span data-ttu-id="51fa6-216">**Per eseguire il debug della configurazione 6to4**</span><span class="sxs-lookup"><span data-stu-id="51fa6-216">**To debug your 6to4 configuration**</span></span>

1.  <span data-ttu-id="51fa6-217">Verificare la connettività IPv4 al router di inoltro 6to4:</span><span class="sxs-lookup"><span data-stu-id="51fa6-217">Check your IPv4 connectivity to the 6to4 relay router:</span></span>

    <span data-ttu-id="51fa6-218">**ping 6to4.ipv6.microsoft.com**</span><span class="sxs-lookup"><span data-stu-id="51fa6-218">**ping 6to4.ipv6.microsoft.com**</span></span>

    <span data-ttu-id="51fa6-219">Se l'operazione ha esito negativo, non si dispone della connettività Internet globale.</span><span class="sxs-lookup"><span data-stu-id="51fa6-219">If this fails, then you do not have global Internet connectivity.</span></span>

2.  <span data-ttu-id="51fa6-220">Controllare l'incapsulamento IPv6 usando il tunneling automatico:</span><span class="sxs-lookup"><span data-stu-id="51fa6-220">Check IPv6 encapsulation by using automatic tunneling:</span></span>

    <span data-ttu-id="51fa6-221">**ping6:: 131.107.152.32**</span><span class="sxs-lookup"><span data-stu-id="51fa6-221">**ping6 ::131.107.152.32**</span></span>

    <span data-ttu-id="51fa6-222">Se il problema persiste, è possibile che sia presente un firewall o un Network Address Translator (NAT) tra il computer e Internet.</span><span class="sxs-lookup"><span data-stu-id="51fa6-222">If this fails, then you might have a firewall or network address translator (NAT) between your computer and the Internet.</span></span> <span data-ttu-id="51fa6-223">Se l'operazione ha esito positivo, la connessione Internet può supportare 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-223">If this is successful, then your Internet connection can support 6to4.</span></span>

3.  <span data-ttu-id="51fa6-224">Controllare la visualizzazione del comando IPv6 RT.</span><span class="sxs-lookup"><span data-stu-id="51fa6-224">Check the display of the ipv6 rt command.</span></span> <span data-ttu-id="51fa6-225">Verrà visualizzata una route 2002::/16-> 2.</span><span class="sxs-lookup"><span data-stu-id="51fa6-225">You should see a 2002::/16 -> 2 route.</span></span> <span data-ttu-id="51fa6-226">Controllare la visualizzazione del comando IPv6 If 2.</span><span class="sxs-lookup"><span data-stu-id="51fa6-226">Check the display of the ipv6 if 2 command.</span></span> <span data-ttu-id="51fa6-227">Verrà visualizzato un indirizzo preferito con un prefisso 2002::/16.</span><span class="sxs-lookup"><span data-stu-id="51fa6-227">You should see a preferred address with a 2002::/16 prefix.</span></span>

> [!Note]  
> <span data-ttu-id="51fa6-228">L'indirizzo IPv4 del router di inoltro Microsoft 6to4 di 131.107.152.32 è soggetto a modifiche.</span><span class="sxs-lookup"><span data-stu-id="51fa6-228">The IPv4 address of the Microsoft 6to4 relay router of 131.107.152.32 is subject to change.</span></span> <span data-ttu-id="51fa6-229">Se il passaggio 2 precedente non funziona, controllare l'output del comando ping nel passaggio 1 per verificare l'indirizzo IPv4 del router di inoltro Microsoft 6to4.</span><span class="sxs-lookup"><span data-stu-id="51fa6-229">If Step 2 above does not work, check the output of the ping command in step 1 to verify the IPv4 address of the Microsoft 6to4 relay router.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="51fa6-230">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51fa6-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51fa6-231">Configurazioni consigliate per IPv6</span><span class="sxs-lookup"><span data-stu-id="51fa6-231">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> <dt>

[<span data-ttu-id="51fa6-232">Singola subnet con indirizzi locali rispetto al collegamento</span><span class="sxs-lookup"><span data-stu-id="51fa6-232">Single subnet with link-local addresses</span></span>](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="51fa6-233">Utilizzo di IPsec tra due host di collegamento locale</span><span class="sxs-lookup"><span data-stu-id="51fa6-233">Using IPsec between two local link hosts</span></span>](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



