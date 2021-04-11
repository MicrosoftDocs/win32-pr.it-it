---
description: Tutte le configurazioni IPv6 vengono eseguite con lo strumento Ipv6.exe.
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226084"
---
# <a name="ipv6exe"></a><span data-ttu-id="78e1b-103">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="78e1b-103">Ipv6.exe</span></span>

<span data-ttu-id="78e1b-104">Tutte le configurazioni IPv6 vengono eseguite con lo strumento Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="78e1b-104">All IPv6 configuration is done with the Ipv6.exe tool.</span></span> <span data-ttu-id="78e1b-105">Questo strumento viene utilizzato principalmente per l'esecuzione di query e la configurazione di interfacce, indirizzi, cache e route IPv6.</span><span class="sxs-lookup"><span data-stu-id="78e1b-105">This tool is primarily used for the querying and configuring of IPv6 interfaces, addresses, caches, and routes.</span></span> <span data-ttu-id="78e1b-106">Di seguito sono riportati i sottocomandi IPv6:</span><span class="sxs-lookup"><span data-stu-id="78e1b-106">The following are IPv6 subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="78e1b-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6 se** \[ Se\#\]</span><span class="sxs-lookup"><span data-stu-id="78e1b-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**ipv6 if** \[if\#\]</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-108">Visualizza informazioni sulle interfacce.</span><span class="sxs-lookup"><span data-stu-id="78e1b-108">Displays information about interfaces.</span></span> <span data-ttu-id="78e1b-109">Se viene specificato un numero di interfaccia, vengono visualizzate solo le informazioni su tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-109">If an interface number is specified, only information about that interface is displayed.</span></span> <span data-ttu-id="78e1b-110">In caso contrario, verranno visualizzate le informazioni su tutte le interfacce.</span><span class="sxs-lookup"><span data-stu-id="78e1b-110">Otherwise, information about all interfaces is displayed.</span></span> <span data-ttu-id="78e1b-111">L'output include l'indirizzo del livello di collegamento dell'interfaccia e l'elenco di indirizzi IPv6 assegnati all'interfaccia, tra cui la MTU corrente dell'interfaccia e la MTU massima (true) che l'interfaccia è in grado di supportare.</span><span class="sxs-lookup"><span data-stu-id="78e1b-111">The output includes the interface's link-layer address and the list of IPv6 addresses assigned to the interface, including the interface's current MTU and the maximum (true) MTU that the interface can support.</span></span>

<span data-ttu-id="78e1b-112">\#L'interfaccia 1 è una pseudo-interfaccia usata per il loopback.</span><span class="sxs-lookup"><span data-stu-id="78e1b-112">Interface \#1 is a pseudo-interface used for loopback.</span></span> <span data-ttu-id="78e1b-113">\#L'interfaccia 2 è una pseudo-interfaccia usata per il tunneling configurato, il tunneling automatico e il tunneling 6to4.</span><span class="sxs-lookup"><span data-stu-id="78e1b-113">Interface \#2 is a pseudo-interface used for configured tunneling, automatic tunneling, and 6to4 tunneling.</span></span> <span data-ttu-id="78e1b-114">Le altre interfacce sono numerate in modo sequenziale nell'ordine in cui vengono create.</span><span class="sxs-lookup"><span data-stu-id="78e1b-114">Other interfaces are numbered sequentially in the order in which they are created.</span></span> <span data-ttu-id="78e1b-115">Questo ordine varia da un computer a un altro.</span><span class="sxs-lookup"><span data-stu-id="78e1b-115">This order varies from one computer to another.</span></span>

<span data-ttu-id="78e1b-116">Gli indirizzi del livello di collegamento nel formato *AA* - *BB* - *CC* - *DD* - *EE* - *FF* sono indirizzi Ethernet.</span><span class="sxs-lookup"><span data-stu-id="78e1b-116">Link-layer addresses in *aa*-*bb*-*cc*-*dd*-*ee*-*ff* format are Ethernet addresses.</span></span> <span data-ttu-id="78e1b-117">Indirizzo del livello di collegamento in *un oggetto*. *b*. *c*. il formato *d* è costituito da una o più interfacce da 6 a 4.</span><span class="sxs-lookup"><span data-stu-id="78e1b-117">Link-layer address in *a*.*b*.*c*.*d* form are 6-over-4 interfaces.</span></span> <span data-ttu-id="78e1b-118">Per ulteriori informazioni su 6-over-4, vedere la specifica RFC 2529.</span><span class="sxs-lookup"><span data-stu-id="78e1b-118">For more information on 6-over-4, see RFC 2529.</span></span>

<span data-ttu-id="78e1b-119">Le due pseudo-interfacce non utilizzano l'individuazione router adiacenti IPv6.</span><span class="sxs-lookup"><span data-stu-id="78e1b-119">The two pseudo-interfaces do not use IPv6 Neighbor Discovery.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**IPv6 IFC** se \# \[ inoltri \] \[ annuncia \] \[ -inoltri \] \[ -annuncia i \] \[ byte MTU \# sito \] \[ -identificatore\]</span><span class="sxs-lookup"><span data-stu-id="78e1b-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ipv6 ifc** if\# \[forwards\] \[advertises\] \[-forwards\] \[-advertises\] \[mtu \#bytes\] \[site site-identifier\]</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-121">Controlla gli attributi di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-121">Controls interface attributes.</span></span> <span data-ttu-id="78e1b-122">È possibile inoltrare le interfacce, nel qual caso inoltrare pacchetti con indirizzi di destinazione non assegnati all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-122">Interfaces can be forwarding, in which case they forward packets with destination addresses not assigned to the interface.</span></span> <span data-ttu-id="78e1b-123">Le interfacce possono essere annunciate, nel qual caso inviano annunci router.</span><span class="sxs-lookup"><span data-stu-id="78e1b-123">Interfaces can be advertising, in which case they send router advertisements.</span></span> <span data-ttu-id="78e1b-124">Questi attributi possono essere controllati in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="78e1b-124">These attributes can be independently controlled.</span></span> <span data-ttu-id="78e1b-125">Un'interfaccia invia richieste router e riceve annunci router o riceve richieste router e invia annunci router.</span><span class="sxs-lookup"><span data-stu-id="78e1b-125">An interface either sends router solicitations and receives router advertisements, or receives router solicitations and sends router advertisements.</span></span>

<span data-ttu-id="78e1b-126">Poiché le due pseudo-interfacce non utilizzano l'individuazione Neighbor, non possono essere configurate per l'invio di annunci router.</span><span class="sxs-lookup"><span data-stu-id="78e1b-126">Because the two pseudo-interfaces do not use Neighbor Discovery, they cannot be configured to send router advertisements.</span></span>

<span data-ttu-id="78e1b-127">Gli inoltri possono essere abbreviati come FORW e annunciati come ADV.</span><span class="sxs-lookup"><span data-stu-id="78e1b-127">Forwards can be abbreviated as forw, and advertised as adv.</span></span>

<span data-ttu-id="78e1b-128">È anche possibile impostare il MTU per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-128">The MTU for the interface can also be set.</span></span> <span data-ttu-id="78e1b-129">Il nuovo MTU deve essere minore o uguale al valore massimo (true) MTU del collegamento (come segnalato da IPv6 if) e maggiore o uguale alla MTU IPv6 minima (1280 byte).</span><span class="sxs-lookup"><span data-stu-id="78e1b-129">The new MTU must be less than or equal to the link's maximum (true) MTU (as reported by ipv6 if) and greater than or equal to the minimum IPv6 MTU (1280 bytes).</span></span>

<span data-ttu-id="78e1b-130">È anche possibile modificare l'identificatore del sito per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-130">The site-identifier for an interface can also be changed.</span></span> <span data-ttu-id="78e1b-131">Gli identificatori del sito vengono usati nel \_ \_ campo ID ambito sin6 con indirizzi locali del sito.</span><span class="sxs-lookup"><span data-stu-id="78e1b-131">Site identifiers are used in the sin6\_scope\_id field with site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IFD IPv6** se\#</span><span class="sxs-lookup"><span data-stu-id="78e1b-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**ipv6 ifd** if\#</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-133">Elimina un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-133">Deletes an interface.</span></span> <span data-ttu-id="78e1b-134">Le pseudo-interfacce loopback e tunnel non possono essere eliminate.</span><span class="sxs-lookup"><span data-stu-id="78e1b-134">The loopback and tunnel pseudo-interfaces cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**NC IPv6** \[ Se \# \[ Address\]\]</span><span class="sxs-lookup"><span data-stu-id="78e1b-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**ipv6 nc** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-136">Visualizza il contenuto della cache del router adiacente.</span><span class="sxs-lookup"><span data-stu-id="78e1b-136">Displays the contents of the neighbor cache.</span></span> <span data-ttu-id="78e1b-137">Se viene specificato un numero di interfaccia, vengono visualizzati solo i contenuti della cache adiacente di tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-137">If an interface number is specified, only the contents of that interface's neighbor cache are displayed.</span></span> <span data-ttu-id="78e1b-138">In caso contrario, viene visualizzato il contenuto di tutte le cache adiacenti dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-138">Otherwise, the contents of all the interface's neighbor caches are displayed.</span></span> <span data-ttu-id="78e1b-139">Se viene specificata un'interfaccia, è possibile specificare un indirizzo IPv6 per visualizzare solo tale voce della cache adiacente.</span><span class="sxs-lookup"><span data-stu-id="78e1b-139">If an interface is specified, an IPv6 address can be specified to display only that neighbor cache entry.</span></span>

<span data-ttu-id="78e1b-140">Per ogni voce della cache adiacente vengono visualizzati l'interfaccia, l'indirizzo IPv6, l'indirizzo del livello di collegamento e lo stato di raggiungimento.</span><span class="sxs-lookup"><span data-stu-id="78e1b-140">For each neighbor cache entry, the interface, IPv6 address, link-layer address, and reach state are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**NCF IPv6** \[ Se \# \[ Address\]\]</span><span class="sxs-lookup"><span data-stu-id="78e1b-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**ipv6 ncf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-142">Scarica le voci della cache adiacenti specificate.</span><span class="sxs-lookup"><span data-stu-id="78e1b-142">Flushes the specified neighbor cache entries.</span></span> <span data-ttu-id="78e1b-143">Vengono eliminate solo le voci della cache adiacenti senza riferimenti.</span><span class="sxs-lookup"><span data-stu-id="78e1b-143">Only neighbor cache entries without references are purged.</span></span> <span data-ttu-id="78e1b-144">Poiché le voci della cache di route contengono riferimenti a voci di cache adiacenti, la cache di route deve essere scaricata per prima.</span><span class="sxs-lookup"><span data-stu-id="78e1b-144">Because route cache entries hold references to neighbor cache entries, the route cache should be flushed first.</span></span> <span data-ttu-id="78e1b-145">Le voci della tabella di routing possono inoltre mantenere i riferimenti alle voci della cache adiacenti.</span><span class="sxs-lookup"><span data-stu-id="78e1b-145">Routing table entries can also hold references to neighbor cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**RC IPv6** \[ Se \# Address\]</span><span class="sxs-lookup"><span data-stu-id="78e1b-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**ipv6 rc** \[if\# address\]</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-147">Visualizza il contenuto della cache di route.</span><span class="sxs-lookup"><span data-stu-id="78e1b-147">Displays the contents of the route cache.</span></span> <span data-ttu-id="78e1b-148">La cache di route è il nome di implementazione IPv6 Microsoft per la cache di destinazione.</span><span class="sxs-lookup"><span data-stu-id="78e1b-148">The route cache is the Microsoft IPv6 implementation name for the destination cache.</span></span> <span data-ttu-id="78e1b-149">Se vengono specificate un'interfaccia e un indirizzo, viene visualizzata la voce della cache di route per raggiungere l'indirizzo tramite l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-149">If an interface and address are specified, the route cache entry for reaching the address through the interface is displayed.</span></span> <span data-ttu-id="78e1b-150">In caso contrario, vengono visualizzate tutte le voci della cache di route.</span><span class="sxs-lookup"><span data-stu-id="78e1b-150">Otherwise, all route cache entries are displayed.</span></span>

<span data-ttu-id="78e1b-151">Per ogni voce della cache di route vengono visualizzati l'indirizzo IPv6 e l'interfaccia hop successiva e l'indirizzo adiacente correnti.</span><span class="sxs-lookup"><span data-stu-id="78e1b-151">For each route cache entry, the IPv6 address and the current next-hop interface and neighbor address are displayed.</span></span> <span data-ttu-id="78e1b-152">Indirizzo di origine preferito da usare con questa destinazione, l'MTU del percorso corrente per raggiungere questa destinazione attraverso l'interfaccia e la determinazione della presenza di una voce specifica dell'interfaccia, ovvero la voce della cache della route.</span><span class="sxs-lookup"><span data-stu-id="78e1b-152">The preferred source address for use with this destination, the current path MTU for reaching this destination through the interface, and the determination of whether this is an interface specific–route cache entry are also displayed.</span></span> <span data-ttu-id="78e1b-153">Viene visualizzato anche un indirizzo di interesse (per la mobilità) per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="78e1b-153">Any care-of address (for mobility) for the destination address is displayed as well.</span></span>

<span data-ttu-id="78e1b-154">Un indirizzo di destinazione può avere più voci della cache di route, quante una per ogni interfaccia in uscita.</span><span class="sxs-lookup"><span data-stu-id="78e1b-154">A destination address can have multiple route cache entries—as many as one for each outgoing interface.</span></span> <span data-ttu-id="78e1b-155">Un indirizzo di destinazione può tuttavia includere al massimo una voce della cache di route non specifica dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-155">However, a destination address can have a maximum of one route cache entry that is not interface-specific.</span></span> <span data-ttu-id="78e1b-156">Una voce specifica dell'interfaccia-route della cache viene usata solo se l'applicazione specifica in modo esplicito l'interfaccia in uscita.</span><span class="sxs-lookup"><span data-stu-id="78e1b-156">An interface specific–route cache entry is only used if the application explicitly specifies that outgoing interface.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**RCF IPv6** \[ Se \# \[ Address\]\]</span><span class="sxs-lookup"><span data-stu-id="78e1b-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**ipv6 rcf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-158">Scarica le voci della cache di route specificate.</span><span class="sxs-lookup"><span data-stu-id="78e1b-158">Flushes the specified route cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**IPv6 BC**</span><span class="sxs-lookup"><span data-stu-id="78e1b-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**ipv6 bc**</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-160">Visualizza il contenuto della cache di binding, che contiene le associazioni tra gli indirizzi domestici e gli indirizzi di assistenza per IPv6 per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="78e1b-160">Displays the contents of the binding cache, which holds bindings between home addresses and care-of addresses for mobile IPv6.</span></span>

<span data-ttu-id="78e1b-161">Per ogni binding vengono visualizzati l'indirizzo Home, l'indirizzo di interesse, il numero di sequenza dell'associazione e la durata.</span><span class="sxs-lookup"><span data-stu-id="78e1b-161">For each binding, the home address, care-of address, binding sequence number, and lifetime are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**adu adu** se \# /Address \[ Lifetime VL \[ /pl \] \] \[ anycast \] \[\]</span><span class="sxs-lookup"><span data-stu-id="78e1b-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**ipv6 adu** if\#/address \[lifetime VL\[/PL\]\] \[anycast\] \[unicast\]</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-163">Aggiunge o rimuove un'assegnazione di indirizzi unicast o anycast su un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-163">Adds or removes a unicast or anycast address assignment on an interface.</span></span> <span data-ttu-id="78e1b-164">L'indirizzo unicast viene agito a meno che non sia specificata la funzione anycast.</span><span class="sxs-lookup"><span data-stu-id="78e1b-164">The unicast address is acted upon unless anycast is specified.</span></span>

<span data-ttu-id="78e1b-165">La durata è infinita se non è specificata.</span><span class="sxs-lookup"><span data-stu-id="78e1b-165">Lifetime is infinite if unspecified.</span></span> <span data-ttu-id="78e1b-166">Se viene specificata solo una durata valida, la durata preferita è uguale alla durata valida.</span><span class="sxs-lookup"><span data-stu-id="78e1b-166">If only a valid lifetime is specified, the preferred lifetime is equal to the valid lifetime.</span></span> <span data-ttu-id="78e1b-167">È possibile specificare una durata infinita o un valore finito in secondi.</span><span class="sxs-lookup"><span data-stu-id="78e1b-167">An infinite lifetime may be specified, or a finite value in seconds.</span></span> <span data-ttu-id="78e1b-168">La durata preferita deve essere minore o uguale alla durata valida.</span><span class="sxs-lookup"><span data-stu-id="78e1b-168">The preferred lifetime must be less than or equal to the valid lifetime.</span></span> <span data-ttu-id="78e1b-169">Se si specifica una durata pari a zero, l'indirizzo verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="78e1b-169">Specifying a lifetime of zero causes the address to be removed.</span></span>

<span data-ttu-id="78e1b-170">È possibile abbreviare la durata del ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="78e1b-170">You can abbreviate lifetime as life.</span></span>

<span data-ttu-id="78e1b-171">Per gli indirizzi anycast, gli unici valori di durata validi sono zero e infinite.</span><span class="sxs-lookup"><span data-stu-id="78e1b-171">For anycast addresses, the only valid lifetime values are zero and infinite.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**TSS IPv6**</span><span class="sxs-lookup"><span data-stu-id="78e1b-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**ipv6 spt**</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-173">Consente di visualizzare il contenuto corrente della tabella dei prefissi di sito.</span><span class="sxs-lookup"><span data-stu-id="78e1b-173">Displays the current contents of the site prefix table.</span></span>

<span data-ttu-id="78e1b-174">Per ogni prefisso del sito, il comando Visualizza il prefisso, l'interfaccia a cui si applica il prefisso del sito e la durata del prefisso in secondi.</span><span class="sxs-lookup"><span data-stu-id="78e1b-174">For each site prefix, the command displays the prefix, the interface to which the site prefix applies, and the prefix lifetime in seconds.</span></span>

<span data-ttu-id="78e1b-175">I prefissi del sito vengono in genere configurati automaticamente dagli annunci router.</span><span class="sxs-lookup"><span data-stu-id="78e1b-175">Site prefixes are normally auto-configured from router advertisements.</span></span> <span data-ttu-id="78e1b-176">Vengono usati nella funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) per filtrare indirizzi locali del sito non appropriati.</span><span class="sxs-lookup"><span data-stu-id="78e1b-176">They are used in the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function to filter inappropriate site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>prefisso **SPU IPv6** se \# \[ Lifetime L\]</span><span class="sxs-lookup"><span data-stu-id="78e1b-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**ipv6 spu** prefix if\# \[lifetime L\]</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-178">Aggiunge, rimuove o aggiorna un prefisso nella tabella del prefisso del sito.</span><span class="sxs-lookup"><span data-stu-id="78e1b-178">Adds, removes, or updates a prefix in the site prefix table.</span></span>

<span data-ttu-id="78e1b-179">Il prefisso e il numero di interfaccia sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="78e1b-179">The prefix and interface number are required.</span></span> <span data-ttu-id="78e1b-180">Durata del prefisso del sito, specificata in secondi, il valore predefinito è infinite se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="78e1b-180">The site prefix lifetime, specified in seconds, defaults to infinite if not specified.</span></span> <span data-ttu-id="78e1b-181">Se si specifica una durata pari a zero, il prefisso del sito viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="78e1b-181">Specifying a lifetime of zero deletes the site prefix.</span></span>

<span data-ttu-id="78e1b-182">Questo comando non è necessario per la configurazione normale di host o router.</span><span class="sxs-lookup"><span data-stu-id="78e1b-182">This command is unnecessary for the normal configuration of hosts or routers.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**RT IPv6**</span><span class="sxs-lookup"><span data-stu-id="78e1b-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**ipv6 rt**</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-184">Consente di visualizzare il contenuto corrente della tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="78e1b-184">Displays the current contents of the routing table.</span></span>

<span data-ttu-id="78e1b-185">Per ogni voce della tabella di routing, il comando Visualizza il prefisso della route, un'interfaccia on-link o un neighbor hop successivo su un'interfaccia, un valore di preferenza (più piccolo) e una durata in secondi.</span><span class="sxs-lookup"><span data-stu-id="78e1b-185">For each routing table entry, the command displays the route prefix, an on-link interface or a next-hop neighbor on an interface, a preference value (smaller is preferred), and a lifetime in seconds.</span></span>

<span data-ttu-id="78e1b-186">Le voci della tabella di routing possono avere anche attributi di **pubblicazione** e di **invecchiamento** .</span><span class="sxs-lookup"><span data-stu-id="78e1b-186">Routing table entries may also have **publish** and **aging** attributes.</span></span> <span data-ttu-id="78e1b-187">Per impostazione predefinita, l'età (la durata viene conteggiata, anziché costante rimanente) e non viene pubblicata (non utilizzata per la creazione di annunci router).</span><span class="sxs-lookup"><span data-stu-id="78e1b-187">By default, they age (the lifetime counts down, rather than remaining constant) and are not published (not used in constructing router advertisements).</span></span>

<span data-ttu-id="78e1b-188">Negli host le voci della tabella di routing vengono in genere configurate automaticamente dagli annunci router.</span><span class="sxs-lookup"><span data-stu-id="78e1b-188">On hosts, routing table entries are normally auto-configured from router advertisements.</span></span>

</dd> <dt>

<span data-ttu-id="78e1b-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>prefisso **RTU** per la \# \[ \] \[ durata/NextHop L \] \[ preferenza P \] \[ pubblicazione \] \[ età \] \[ SPL sito-lunghezza prefisso\]</span><span class="sxs-lookup"><span data-stu-id="78e1b-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**ipv6 rtu** prefix if\#\[/nexthop\] \[lifetime L\] \[preference P\] \[publish\] \[age\] \[spl site-prefix-length\]</span></span>
</dt> <dd>

<span data-ttu-id="78e1b-190">Aggiunge o rimuove una route nella tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="78e1b-190">Adds or removes a route in the routing table.</span></span> <span data-ttu-id="78e1b-191">Il prefisso della route è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="78e1b-191">The route prefix is required.</span></span> <span data-ttu-id="78e1b-192">Il prefisso può essere collegato a un'interfaccia specificata o hop successivo, specificato con un indirizzo adiacente in un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-192">The prefix can be on-link to a specified interface, or next-hop, specified with a neighbor address on an interface.</span></span> <span data-ttu-id="78e1b-193">La route può avere una durata in secondi, con l'impostazione predefinita infinita, e una preferenza, con il valore predefinito zero o la scelta più preferita.</span><span class="sxs-lookup"><span data-stu-id="78e1b-193">The route can have a lifetime in seconds, with the default infinite, and a preference, with the default of zero, or most preferred.</span></span> <span data-ttu-id="78e1b-194">Se si specifica una durata pari a zero, la route viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="78e1b-194">Specifying a lifetime of zero deletes the route.</span></span>

<span data-ttu-id="78e1b-195">Se la route viene specificata come pubblicata, a indicare che verrà utilizzata per la creazione di annunci router, non invecchia.</span><span class="sxs-lookup"><span data-stu-id="78e1b-195">If the route is specified as published, indicating it will be used in constructing router advertisements, it does not age.</span></span> <span data-ttu-id="78e1b-196">La durata della route non viene conteggiata e pertanto è effettivamente infinita, ma il valore viene utilizzato negli annunci router.</span><span class="sxs-lookup"><span data-stu-id="78e1b-196">The route's lifetime does not count down and therefore is effectively infinite, but the value is used in router advertisements.</span></span> <span data-ttu-id="78e1b-197">Facoltativamente, è possibile specificare una route come route pubblicata che invecchia anche.</span><span class="sxs-lookup"><span data-stu-id="78e1b-197">Optionally, a route can be specified as a published route that also ages.</span></span> <span data-ttu-id="78e1b-198">Per impostazione predefinita, una route non pubblicata è sempre di età.</span><span class="sxs-lookup"><span data-stu-id="78e1b-198">A nonpublished route by default always ages.</span></span>

<span data-ttu-id="78e1b-199">La sottoopzione SPL facoltativa può essere usata per specificare una lunghezza del prefisso del sito associata alla route.</span><span class="sxs-lookup"><span data-stu-id="78e1b-199">The optional spl suboption can be used to specify a site prefix length associated with the route.</span></span> <span data-ttu-id="78e1b-200">La lunghezza del prefisso del sito viene utilizzata solo quando si inviano annunci router.</span><span class="sxs-lookup"><span data-stu-id="78e1b-200">The site prefix length is used only when sending router advertisements.</span></span>

<span data-ttu-id="78e1b-201">La durata può essere abbreviata come durata, preferenza come pref e pubblicazione come pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="78e1b-201">Lifetime can be abbreviated as life, preference as pref, and publish as pub.</span></span>

</dd> </dl>

 

 



