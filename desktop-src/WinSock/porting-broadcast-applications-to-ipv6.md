---
description: In questa sezione vengono descritte le procedure consigliate per la portabilità di un'applicazione di trasmissione IPv6 nelle funzionalità multicast disponibili con Windows Socket.
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: Porting di applicazioni broadcast in IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb54fec87be2aa6174de603d2c3e4d0e640156902002b1e87fab149a70e3d1ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641701"
---
# <a name="porting-broadcast-applications-to-ipv6"></a>Porting di applicazioni broadcast in IPv6

In questa sezione vengono descritte le procedure consigliate per la portabilità di un'applicazione di trasmissione IPv6 nelle funzionalità multicast disponibili con Windows Socket.

## <a name="comparing-ipv4-to-ipv6"></a>Confronto tra IPv4 e IPv6

La considerazione più importante quando si prepara la portabilità di un'applicazione di trasmissione IPv4 a IPv6 è la seguente: IPv6 non ha implementato il concetto di trasmissione. IPv6 usa invece il multicast.

Il multicast per IPv6 può emulare le funzionalità di trasmissione tradizionali disponibili in IPv4. L'impostazione [dell'opzione \_ IPV6 ADD \_ MEMBERSHIP](ipproto-ipv6-socket-options.md) socket con l'indirizzo IPv6 impostato sull'ambito locale del collegamento l'indirizzo di tutti i nodi (FF02::1) equivale alla trasmissione su indirizzi broadcast IPv4 usando l'opzione [socket SO \_ BROADCAST.](socket-options.md) Questo indirizzo viene talvolta chiamato gruppo *multicast all-nodes*. Per le applicazioni che vogliono semplicemente l'emulazione broadcast per IPv6, questo approccio è equivalente dal punto di vista operativo. Una differenza significativa con IPv6, tuttavia, è che i multicast nell'indirizzo del gruppo multicast tutti i nodi non vengono ricevuti per impostazione predefinita (i broadcast IPv4 vengono ricevuti per impostazione predefinita). I programmatori di applicazioni devono usare l'opzione del socket IPV6 ADD MEMBERSHIP per abilitare la ricezione multicast da qualsiasi origine, incluso l'indirizzo del \_ \_ gruppo multicast tutti i nodi.

> [!Note]  
> In IPv6 la selezione dell'interfaccia viene specificata nella struttura dell'argomento passata all'opzione socket multicast o a IOCTL.

 

Tuttavia, per trasmissioni più efficaci, più solide, più selettive e gestibili a più host, gli sviluppatori di applicazioni devono prendere in considerazione il passaggio a un modello multicast.

## <a name="moving-to-multicast"></a>Passaggio al multicast

Con il multicast, i programmatori di applicazioni possono scegliere in modo selettivo una determinata coppia di origine/gruppo, abilitando un modello di ricezione selettiva. L'individuazione del listener multicast (MLD) in IPv6 e la versione 3 del Internet Group Management Protocol (IGMPv3) in IPv4 supportano la programmazione multicast. Inoltre, il multicast consente alle applicazioni di bloccare (o sbloccare) in modo specifico i mittenti all'interno di un gruppo, proteggendo ulteriormente le applicazioni da emittenti non autorizzate. Questa funzionalità è disponibile per IPv4 (richiede IGMPv3) e IPv6 (richiede MLDv2).

Esistono due scenari principali per i programmatori di applicazioni che usano il multicast: quelli per la portabilità da applicazioni broadcast IPv4 (o multicast) a IPv6 e quelli per la creazione di nuove applicazioni multicast IPv6.

Per la portabilità di applicazioni esistenti, sono disponibili due opzioni per il passaggio al multicast IPv6: l'uso delle opzioni socket e l'uso degli IOCL.

-   L'uso delle opzioni socket è un approccio basato su modifiche che consente agli sviluppatori di modificare le proprietà del socket in base alle esigenze, ad esempio bloccando o sbloccando un mittente, aggiungendo una nuova origine e così via. Questo approccio è più intuitivo e consigliato. Per altre informazioni sull'approccio basato su modifiche alla programmazione multicast, vedere [MLD e IGMP using Windows Sockets](igmp-and-windows-sockets.md).
-   L'uso di IOCTL è un approccio basato sullo stato finale, perché consente agli sviluppatori di fornire uno stato del socket completamente configurato, inclusi gli elenchi di inclusione ed esclusione, con una sola chiamata. Per altre informazioni sull'approccio basato sullo stato finale, vedere [Programmazione multicast](final-state-based-multicast-programming.md)basata sullo stato finale.

Per coloro che creano nuove applicazioni multicast IPv6, è consigliabile usare le opzioni socket anziché gli IOCTL.

Esiste un altro approccio alla creazione di applicazioni multicast con IPv6 e ciò comporta l'uso della [**funzione WSAJoinLeaf.**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) Anche se **l'uso della funzione WSAJoinLeaf** non è la procedura consigliata, esistono situazioni che possono determinarne l'uso. Ad esempio, uno svantaggio dell'uso delle opzioni socket in Windows Server 2003 e versioni precedenti è che sono specifiche della versione IP. In queste versioni precedenti di Windows, le diverse opzioni socket devono essere per IPv6 e IPv4. In Windows Vista e versioni successive sono supportate nuove opzioni socket che possono essere usate con IPv4 e IPv6. La **funzione WSAJoinLeaf,** al contrario, è indipendente dalla versione IP e dal protocollo e pertanto può essere un approccio utile per la compilazione di un'applicazione che deve funzionare con più versioni IP in Windows Server 2003 e versioni precedenti. **L'uso della funzione WSAJoinLeaf** può risultare più appropriato in determinate situazioni in cui è necessario l'agnosticismo del protocollo e della versione IP.

 

 



