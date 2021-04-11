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
# <a name="ipv6exe"></a>Ipv6.exe

Tutte le configurazioni IPv6 vengono eseguite con lo strumento Ipv6.exe. Questo strumento viene utilizzato principalmente per l'esecuzione di query e la configurazione di interfacce, indirizzi, cache e route IPv6. Di seguito sono riportati i sottocomandi IPv6:

<dl> <dt>

<span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6 se** \[ Se\#\]
</dt> <dd>

Visualizza informazioni sulle interfacce. Se viene specificato un numero di interfaccia, vengono visualizzate solo le informazioni su tale interfaccia. In caso contrario, verranno visualizzate le informazioni su tutte le interfacce. L'output include l'indirizzo del livello di collegamento dell'interfaccia e l'elenco di indirizzi IPv6 assegnati all'interfaccia, tra cui la MTU corrente dell'interfaccia e la MTU massima (true) che l'interfaccia è in grado di supportare.

\#L'interfaccia 1 è una pseudo-interfaccia usata per il loopback. \#L'interfaccia 2 è una pseudo-interfaccia usata per il tunneling configurato, il tunneling automatico e il tunneling 6to4. Le altre interfacce sono numerate in modo sequenziale nell'ordine in cui vengono create. Questo ordine varia da un computer a un altro.

Gli indirizzi del livello di collegamento nel formato *AA* - *BB* - *CC* - *DD* - *EE* - *FF* sono indirizzi Ethernet. Indirizzo del livello di collegamento in *un oggetto*. *b*. *c*. il formato *d* è costituito da una o più interfacce da 6 a 4. Per ulteriori informazioni su 6-over-4, vedere la specifica RFC 2529.

Le due pseudo-interfacce non utilizzano l'individuazione router adiacenti IPv6.

</dd> <dt>

<span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**IPv6 IFC** se \# \[ inoltri \] \[ annuncia \] \[ -inoltri \] \[ -annuncia i \] \[ byte MTU \# sito \] \[ -identificatore\]
</dt> <dd>

Controlla gli attributi di interfaccia. È possibile inoltrare le interfacce, nel qual caso inoltrare pacchetti con indirizzi di destinazione non assegnati all'interfaccia. Le interfacce possono essere annunciate, nel qual caso inviano annunci router. Questi attributi possono essere controllati in modo indipendente. Un'interfaccia invia richieste router e riceve annunci router o riceve richieste router e invia annunci router.

Poiché le due pseudo-interfacce non utilizzano l'individuazione Neighbor, non possono essere configurate per l'invio di annunci router.

Gli inoltri possono essere abbreviati come FORW e annunciati come ADV.

È anche possibile impostare il MTU per l'interfaccia. Il nuovo MTU deve essere minore o uguale al valore massimo (true) MTU del collegamento (come segnalato da IPv6 if) e maggiore o uguale alla MTU IPv6 minima (1280 byte).

È anche possibile modificare l'identificatore del sito per un'interfaccia. Gli identificatori del sito vengono usati nel \_ \_ campo ID ambito sin6 con indirizzi locali del sito.

</dd> <dt>

<span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IFD IPv6** se\#
</dt> <dd>

Elimina un'interfaccia. Le pseudo-interfacce loopback e tunnel non possono essere eliminate.

</dd> <dt>

<span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**NC IPv6** \[ Se \# \[ Address\]\]
</dt> <dd>

Visualizza il contenuto della cache del router adiacente. Se viene specificato un numero di interfaccia, vengono visualizzati solo i contenuti della cache adiacente di tale interfaccia. In caso contrario, viene visualizzato il contenuto di tutte le cache adiacenti dell'interfaccia. Se viene specificata un'interfaccia, è possibile specificare un indirizzo IPv6 per visualizzare solo tale voce della cache adiacente.

Per ogni voce della cache adiacente vengono visualizzati l'interfaccia, l'indirizzo IPv6, l'indirizzo del livello di collegamento e lo stato di raggiungimento.

</dd> <dt>

<span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**NCF IPv6** \[ Se \# \[ Address\]\]
</dt> <dd>

Scarica le voci della cache adiacenti specificate. Vengono eliminate solo le voci della cache adiacenti senza riferimenti. Poiché le voci della cache di route contengono riferimenti a voci di cache adiacenti, la cache di route deve essere scaricata per prima. Le voci della tabella di routing possono inoltre mantenere i riferimenti alle voci della cache adiacenti.

</dd> <dt>

<span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**RC IPv6** \[ Se \# Address\]
</dt> <dd>

Visualizza il contenuto della cache di route. La cache di route è il nome di implementazione IPv6 Microsoft per la cache di destinazione. Se vengono specificate un'interfaccia e un indirizzo, viene visualizzata la voce della cache di route per raggiungere l'indirizzo tramite l'interfaccia. In caso contrario, vengono visualizzate tutte le voci della cache di route.

Per ogni voce della cache di route vengono visualizzati l'indirizzo IPv6 e l'interfaccia hop successiva e l'indirizzo adiacente correnti. Indirizzo di origine preferito da usare con questa destinazione, l'MTU del percorso corrente per raggiungere questa destinazione attraverso l'interfaccia e la determinazione della presenza di una voce specifica dell'interfaccia, ovvero la voce della cache della route. Viene visualizzato anche un indirizzo di interesse (per la mobilità) per l'indirizzo di destinazione.

Un indirizzo di destinazione può avere più voci della cache di route, quante una per ogni interfaccia in uscita. Un indirizzo di destinazione può tuttavia includere al massimo una voce della cache di route non specifica dell'interfaccia. Una voce specifica dell'interfaccia-route della cache viene usata solo se l'applicazione specifica in modo esplicito l'interfaccia in uscita.

</dd> <dt>

<span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**RCF IPv6** \[ Se \# \[ Address\]\]
</dt> <dd>

Scarica le voci della cache di route specificate.

</dd> <dt>

<span id="ipv6_bc"></span><span id="IPV6_BC"></span>**IPv6 BC**
</dt> <dd>

Visualizza il contenuto della cache di binding, che contiene le associazioni tra gli indirizzi domestici e gli indirizzi di assistenza per IPv6 per dispositivi mobili.

Per ogni binding vengono visualizzati l'indirizzo Home, l'indirizzo di interesse, il numero di sequenza dell'associazione e la durata.

</dd> <dt>

<span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**adu adu** se \# /Address \[ Lifetime VL \[ /pl \] \] \[ anycast \] \[\]
</dt> <dd>

Aggiunge o rimuove un'assegnazione di indirizzi unicast o anycast su un'interfaccia. L'indirizzo unicast viene agito a meno che non sia specificata la funzione anycast.

La durata è infinita se non è specificata. Se viene specificata solo una durata valida, la durata preferita è uguale alla durata valida. È possibile specificare una durata infinita o un valore finito in secondi. La durata preferita deve essere minore o uguale alla durata valida. Se si specifica una durata pari a zero, l'indirizzo verrà rimosso.

È possibile abbreviare la durata del ciclo di vita.

Per gli indirizzi anycast, gli unici valori di durata validi sono zero e infinite.

</dd> <dt>

<span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**TSS IPv6**
</dt> <dd>

Consente di visualizzare il contenuto corrente della tabella dei prefissi di sito.

Per ogni prefisso del sito, il comando Visualizza il prefisso, l'interfaccia a cui si applica il prefisso del sito e la durata del prefisso in secondi.

I prefissi del sito vengono in genere configurati automaticamente dagli annunci router. Vengono usati nella funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) per filtrare indirizzi locali del sito non appropriati.

</dd> <dt>

<span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>prefisso **SPU IPv6** se \# \[ Lifetime L\]
</dt> <dd>

Aggiunge, rimuove o aggiorna un prefisso nella tabella del prefisso del sito.

Il prefisso e il numero di interfaccia sono obbligatori. Durata del prefisso del sito, specificata in secondi, il valore predefinito è infinite se non è specificato. Se si specifica una durata pari a zero, il prefisso del sito viene eliminato.

Questo comando non è necessario per la configurazione normale di host o router.

</dd> <dt>

<span id="ipv6_rt"></span><span id="IPV6_RT"></span>**RT IPv6**
</dt> <dd>

Consente di visualizzare il contenuto corrente della tabella di routing.

Per ogni voce della tabella di routing, il comando Visualizza il prefisso della route, un'interfaccia on-link o un neighbor hop successivo su un'interfaccia, un valore di preferenza (più piccolo) e una durata in secondi.

Le voci della tabella di routing possono avere anche attributi di **pubblicazione** e di **invecchiamento** . Per impostazione predefinita, l'età (la durata viene conteggiata, anziché costante rimanente) e non viene pubblicata (non utilizzata per la creazione di annunci router).

Negli host le voci della tabella di routing vengono in genere configurate automaticamente dagli annunci router.

</dd> <dt>

<span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>prefisso **RTU** per la \# \[ \] \[ durata/NextHop L \] \[ preferenza P \] \[ pubblicazione \] \[ età \] \[ SPL sito-lunghezza prefisso\]
</dt> <dd>

Aggiunge o rimuove una route nella tabella di routing. Il prefisso della route è obbligatorio. Il prefisso può essere collegato a un'interfaccia specificata o hop successivo, specificato con un indirizzo adiacente in un'interfaccia. La route può avere una durata in secondi, con l'impostazione predefinita infinita, e una preferenza, con il valore predefinito zero o la scelta più preferita. Se si specifica una durata pari a zero, la route viene eliminata.

Se la route viene specificata come pubblicata, a indicare che verrà utilizzata per la creazione di annunci router, non invecchia. La durata della route non viene conteggiata e pertanto è effettivamente infinita, ma il valore viene utilizzato negli annunci router. Facoltativamente, è possibile specificare una route come route pubblicata che invecchia anche. Per impostazione predefinita, una route non pubblicata è sempre di età.

La sottoopzione SPL facoltativa può essere usata per specificare una lunghezza del prefisso del sito associata alla route. La lunghezza del prefisso del sito viene utilizzata solo quando si inviano annunci router.

La durata può essere abbreviata come durata, preferenza come pref e pubblicazione come pubblicazione.

</dd> </dl>

 

 



