---
description: In questa sezione vengono descritte le procedure consigliate per il porting di un'applicazione broadcast IPv6 alle funzionalità multicast disponibili con Windows Sockets.
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: Porting di applicazioni broadcast a IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7dce09db6822a6f9b0a61873ca6bbff5a256b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484917"
---
# <a name="porting-broadcast-applications-to-ipv6"></a>Porting di applicazioni broadcast a IPv6

In questa sezione vengono descritte le procedure consigliate per il porting di un'applicazione broadcast IPv6 alle funzionalità multicast disponibili con Windows Sockets.

## <a name="comparing-ipv4-to-ipv6"></a>Confronto tra IPv4 e IPv6

La considerazione più importante quando si prepara la porta di un'applicazione broadcast IPv4 a IPv6 è la seguente: IPv6 non ha implementato il concetto di broadcast. Il protocollo IPv6 usa invece il multicast.

Multicast per IPv6 è in grado di emulare le funzionalità di broadcast tradizionali disponibili in IPv4. L'impostazione dell'opzione per il socket di [ \_ \_ appartenenza IPv6](ipproto-ipv6-socket-options.md) con l'indirizzo IPv6 impostato sull'indirizzo di tutti i nodi del collegamento locale (FF02:: 1) equivale a trasmettere gli indirizzi di trasmissione IPv4 utilizzando l'opzione socket [ \_ broadcast](socket-options.md) . Questo indirizzo viene talvolta denominato *gruppo multicast tutti i nodi*. Per le applicazioni che vogliono semplicemente emulazione broadcast per IPv6, questo approccio è funzionalmente equivalente. Una differenza rilevante rispetto a IPv6, tuttavia, è che i multicast nell'indirizzo del gruppo multicast tutti i nodi non vengono ricevuti per impostazione predefinita (le trasmissioni IPv4 vengono ricevute per impostazione predefinita). \_ \_ Per abilitare la ricezione multicast da qualsiasi origine, incluso l'indirizzo del gruppo multicast all-nodes, i programmatori di applicazioni devono usare l'opzione IPv6 Add Membership socket.

> [!Note]  
> In IPv6, nella struttura degli argomenti passata all'opzione socket multicast o IOCTL viene specificata la selezione dell'interfaccia.

 

Tuttavia, per trasmissioni più complesse, più affidabili e più selettivi e più gestibili a più host, gli sviluppatori di applicazioni devono considerare il passaggio a un modello multicast.

## <a name="moving-to-multicast"></a>Passaggio al multicast

Con il multicast, i programmatori di applicazioni possono scegliere selettivamente una particolare coppia di origine/gruppo, abilitando un modello di ricezione selettiva. Multicast listener Discovery (MLD) su IPv6 e la versione 3 di Internet Group Management Protocol (IGMPv3) in IPv4 supportano la programmazione multicast. Il multicast consente inoltre alle applicazioni di bloccare o sbloccare in modo specifico i mittenti all'interno di un gruppo, proteggendo ulteriormente le applicazioni da broadcaster non autorizzati. Questa funzionalità è disponibile per IPv4 (richiede IGMPv3) e IPv6 (richiede MLDv2).

Esistono due scenari principali per i programmatori di applicazioni che utilizzano il multicast, ovvero quelli che eseguono il porting da applicazioni broadcast IPv4 (o multicast) a IPv6 e quelli che creano nuove applicazioni multicast IPv6.

Per il porting delle applicazioni esistenti, sono disponibili due opzioni per passare a multicast IPv6: uso delle opzioni del socket e uso di IOCTL.

-   L'uso delle opzioni socket è un approccio basato sulle modifiche che consente agli sviluppatori di modificare le proprietà del socket come richiesto, ad esempio bloccando o sbloccando un mittente, aggiungendo una nuova origine e così via. Questo approccio è più intuitivo e l'approccio consigliato. Per ulteriori informazioni sull'approccio basato sulle modifiche alla programmazione multicast, vedere [mld e IGMP mediante Windows Sockets](igmp-and-windows-sockets.md).
-   L'uso di IOCTL è un approccio basato sullo stato finale, in quanto consente agli sviluppatori di fornire uno stato del socket completamente configurato, inclusi gli elenchi di inclusione ed esclusione, con una sola chiamata. Per ulteriori informazioni sull'approccio basato sullo stato finale, vedere [programmazione multicast basata sullo stato finale](final-state-based-multicast-programming.md).

Per coloro che creano nuove applicazioni multicast IPv6, la procedura consigliata consiste nell'usare le opzioni socket, anziché usare IOCTL.

Esiste un altro approccio per la creazione di applicazioni multicast con IPv6 e che comporta l'uso della funzione [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) . Sebbene l'utilizzo della funzione **WSAJoinLeaf** non sia la procedura consigliata, è possibile che si verifichino situazioni in cui è possibile impiegarne l'utilizzo. Ad esempio, uno svantaggio dell'uso delle opzioni socket in Windows Server 2003 e versioni precedenti è che si tratta di una versione specifica di IP. In queste versioni precedenti di Windows, le opzioni dei socket diversi devono essere per IPv6 e IPv4. In Windows Vista e versioni successive sono supportate nuove opzioni di socket che possono essere utilizzate con IPv4 e IPv6. La funzione **WSAJoinLeaf** , invece, è indipendente dalla versione IP e dal protocollo e pertanto può essere utile per la compilazione di un'applicazione che deve funzionare con più versioni IP in Windows Server 2003 e versioni precedenti. L'utilizzo della funzione **WSAJoinLeaf** può essere più appropriato in determinate situazioni in cui è richiesto il protocollo e l'agnosticismo della versione IP.

 

 



