---
description: Windows Sockets Abilita l'individuazione del listener multicast (MLD) su IPv6 e il protocollo IGMP (Internet Group Management Protocol) su IPv4 per le applicazioni multicast tramite l'utilizzo di opzioni socket e IOCTL.
ms.assetid: a5de4273-e86e-4f13-b068-256cb38706d4
title: MLD e IGMP con Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6cb9f9c345463e283adea0136037d7ccd03cebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226087"
---
# <a name="mld-and-igmp-using-windows-sockets"></a>MLD e IGMP con Windows Sockets

Windows Sockets Abilita l'individuazione del listener multicast (MLD) su IPv6 e il protocollo IGMP (Internet Group Management Protocol) su IPv4 per le applicazioni multicast tramite l'utilizzo di opzioni socket e IOCTL. Questa pagina descrive le opzioni socket che consentono la programmazione multicast e ne descrive il modo in cui vengono usate. Per le definizioni di ogni opzione socket, consultare la pagina [opzioni socket](socket-options.md) .

Per informazioni sull'uso di IOCTL per la programmazione multicast, vedere la [programmazione multicast basata sullo stato finale](final-state-based-multicast-programming.md) più avanti in questa sezione.

In Windows Vista e versioni successive è disponibile un set di opzioni di socket per la programmazione multicast che supporta indirizzi IPv6 e IPv4. Queste opzioni di socket sono indipendenti dall'IP e possono essere usate sia in IPv6 che in IPv4. In IPv6 le opzioni socket utilizzano MLDv2. In IPv4 le opzioni del socket utilizzano IGMPv3. Queste opzioni IP indipendenti sono le opzioni socket preferite per la programmazione multicast in Windows Vista e versioni successive. Windows Sockets usa le seguenti opzioni di socket: 

| Opzione socket               | Tipo di argomento                                            |
|-----------------------------|----------------------------------------------------------|
| \_origine blocco \_ mcast        | [**Gruppo \_ di Struttura di \_ req di origine**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| \_gruppo join \_ mcast          | [**Gruppo \_ di**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req) Struttura di req                |
| \_gruppo di \_ origine mcast join \_  | [**Gruppo \_ di Struttura di \_ req di origine**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| \_gruppo mcast Leave \_         | [**Gruppo \_ di**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req) Struttura di req                |
| MCAST \_ uscire \_ dal \_ gruppo di origine | [**Gruppo \_ di Struttura di \_ req di origine**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| \_origine di sblocco \_ mcast      | [**Gruppo \_ di Struttura di \_ req di origine**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |



 

Un set di opzioni socket è disponibile per la programmazione multicast che supporta solo indirizzi IPv6. Queste opzioni socket usano MLDv1 o MLDv2. La versione di MLD utilizzata dipende dalla versione di Windows. MLDv2 è supportato in Windows Vista e versioni successive. Windows Sockets usa le seguenti opzioni di socket: 

| Opzione socket          | Tipo di argomento                             |
|------------------------|-------------------------------------------|
| \_Aggiunta di \_ appartenenza a IPv6  | [**struttura \_ MREQ IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |
| \_Appartenenza a eliminazione IPv6 \_ | [**struttura \_ MREQ IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |



 

Un set di opzioni socket è disponibile per la programmazione multicast che supporta solo indirizzi IPv4. Queste opzioni socket usano IGMPv3 o IGMPv2. La versione di IGMP utilizzata dipende dalla versione di Windows. IGMPv3 è supportato in Windows Vista e versioni successive. Windows Sockets usa le seguenti opzioni di socket:

| Opzione socket                | Tipo di argomento                                        |
|------------------------------|------------------------------------------------------|
| \_aggiunta \_ appartenenza IP          | [**struttura \_ MREQ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| \_aggiunta di \_ \_ appartenenza all'origine IP  | struttura di [**\_ \_ origine MREQ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_origine blocco \_ IP            | struttura di [**\_ \_ origine MREQ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_appartenenza a destinazione IP \_         | [**struttura \_ MREQ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| \_ \_ appartenenza all'origine di eliminazione IP \_ | struttura di [**\_ \_ origine MREQ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_origine sblocco IP \_          | struttura di [**\_ \_ origine MREQ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |



 

Quando IGMPv3 è disponibile, le opzioni per l'aggiunta dell'origine IP \_ \_ , l'origine del \_ \_ blocco IP, l'appartenenza all'origine di rilascio IP \_ \_ \_ \_ e \_ l'origine di sblocco IP \_ vengono gestite in modo più efficiente poiché il router è in grado di gestire il filtro. Quando è disponibile solo IGMPv2, l'host deve gestire il filtro.

Esistono due categorie in cui la maggior parte delle applicazioni è probabile che rientrino, ovvero qualsiasi origine e controllata.

-   Per impostazione predefinita, tutte le applicazioni di origine accettano tutte le origini, consentendo la disattivazione **delle** singole origini secondo necessità. Un esempio di applicazione di qualsiasi origine è una chiamata di conferenza video che consente a tutti i destinatari di partecipare.
-   Le applicazioni **controllate di origine** limitano le origini a un elenco specifico, ad esempio una stazione radio Internet o la trasmissione di un evento significativo. Il processo di utilizzo delle opzioni socket è leggermente diverso per ogni.

In Windows Vista e versioni successive, i passaggi seguenti si applicano alle applicazioni di qualsiasi origine:

- Usare **il \_ \_ gruppo mcast join** per partecipare a un gruppo.  
- Usare **l' \_ \_ origine del blocco mcast** per disattivare un'origine specificata, se necessario.  
- Usare **mcast \_ Unblock \_ source** per riabilitare un'origine bloccata, se necessario.  
- Usare **mcast \_ Leave \_ Group** per uscire dal gruppo.  

In Windows Vista e versioni successive, si applicano i passaggi seguenti per le applicazioni di origine controllata:

- Usare **il \_ \_ \_ gruppo di origine mcast join** per unire in join ogni coppia di gruppi/origini.  
- Usare **mcast \_ lasciare \_ il \_ gruppo di origine** per lasciare ogni gruppo/origine oppure usare **mcast \_ Leave \_ Group** per lasciare tutte le origini, se lo stesso indirizzo di gruppo viene usato da tutte le origini.  

I passaggi seguenti si applicano a tutte le applicazioni di origine:

- Usare **IP \_ Aggiungi \_ appartenenza** per partecipare a un gruppo (**IPv6 \_ Aggiungi \_ appartenenza** per IPv6).  
- Usare **l' \_ \_ origine del blocco IP** per disattivare un'origine specificata, se necessario.  
- Usare **l' \_ \_ origine di sblocco IP** per riabilitare un'origine bloccata, se necessario.  
- Utilizzare **l' \_ \_ appartenenza a destinazione IP** per lasciare il gruppo (**eliminazione dell' \_ \_ appartenenza IPv6** per IPv6).  

I passaggi seguenti si applicano alle applicazioni controllate-Source:

- Utilizzare **IP \_ Aggiungi \_ origine \_ appartenenza** per unire ogni coppia gruppo/origine.  
- Utilizzare **l' \_ \_ \_ appartenenza all'origine di rilascio IP** per lasciare ogni gruppo/origine oppure utilizzare l'appartenenza a una **\_ destinazione \_ IP** per lasciare tutte le origini, se lo stesso indirizzo di gruppo viene utilizzato da tutte le origini.  

Per l'ordine in cui sono impostate le opzioni del socket sono presenti regole associate. Per informazioni e risoluzione dei problemi relativi alle opzioni del socket multicast, vedere [comportamento dell'opzione socket multicast](multicast-socket-option-behavior.md).
