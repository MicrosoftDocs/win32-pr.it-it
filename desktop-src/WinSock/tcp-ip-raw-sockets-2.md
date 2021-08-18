---
description: Un socket non elaborato è un tipo di socket che consente l'accesso al provider di trasporto sottostante.
ms.assetid: 4cbe5505-75e7-454f-9e6b-f38bdc60bf6d
title: Socket non elaborati TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef8600c7b1a6c1bc5b2f7b5b210ca2d56f90069b0afce88c83ca45e9cfad8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733391"
---
# <a name="tcpip-raw-sockets"></a>Socket non elaborati TCP/IP

Un socket non elaborato è un tipo di socket che consente l'accesso al provider di trasporto sottostante. Questo argomento si concentra solo sui socket non elaborati e sui protocolli IPv4 e IPv6. Ciò è dovuto al fatto che la maggior parte degli altri protocolli, ad eccezione di ATM, non supporta socket non elaborati. Per usare socket non elaborati, un'applicazione deve avere informazioni dettagliate sul protocollo sottostante in uso.

I provider di servizi Winsock per il protocollo IP possono supportare un *tipo* di socket **SOCK \_ RAW.** Il provider Windows Sockets 2 per TCP/IP incluso in Windows supporta questo tipo di socket **\_ RAW SOCK.**

Esistono due tipi di base di questi socket non elaborati:

-   Il primo tipo usa un tipo di protocollo noto scritto nell'intestazione IP riconosciuta da un provider di servizi Winsock. Un esempio del primo tipo di socket è un socket per il protocollo ICMP (tipo di protocollo IP = 1) o il protocollo ICMPv6 (tipo di procotolo IP = 58).
-   Il secondo tipo consente l'impostazione di qualsiasi tipo di protocollo. Un esempio del secondo tipo è un protocollo sperimentale non supportato direttamente dal provider di servizi Winsock, ad esempio il protocollo SCTP (Stream Control Transmission Protocol).

## <a name="determining-if-raw-sockets-are-supported"></a>Determinare se i socket non elaborati sono supportati

Se un provider di servizi Winsock supporta socket **RAW \_ SOCK** per le famiglie di indirizzi AF INET o AF INET6, il tipo di socket di SOCK RAW deve essere incluso nella struttura WSAPROTOCOL INFO restituita dalla funzione \_ \_ [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) **\_** [**\_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per uno o più provider di trasporto disponibili.

Il membro **iAddressFamily** nella struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) deve specificare AF INET o AF INET6 e il membro \_ \_ **iSocketType** della struttura **WSAPROTOCOL \_ INFO** deve specificare **SOCK \_ RAW** per uno dei provider di trasporto.

Il **membro iProtocol** della struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) può essere impostato su **IP IPROTO. \_** Il membro **iProtocol** della struttura **WSAPROTOCOL \_ INFO** può anche essere impostato su zero se il provider di servizi consente a un'applicazione di usare un tipo di socket **RAW SOCK \_** per altri protocolli di rete diversi dal protocollo Internet per la famiglia di indirizzi.

Gli altri membri nella struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) indicano altre proprietà del supporto del protocollo per **SOCK \_ RAW** e indicano come deve essere trattato un socket **di SOCK \_ RAW.** Questi altri membri di **WSAPROTOCOL \_ INFO** per **SOCK \_ RAW** specificano in genere che il protocollo è senza connessione, orientato ai messaggi, supporta broadcast/multicast (i bit XP1 CONNECTIONLESS, XP1 MESSAGE ORIENTED, XP1 SUPPORT BROADCAST e XP1 SUPPORT MULTIPOINT sono impostati nel membro dwServiceFlags1) e possono avere una dimensione massima del messaggio di \_ \_ \_ \_ \_ \_ \_ 65.467 byte.

In Windows XP e versioni successive, il *NetSh.exe* comando può essere usato per determinare se i socket non elaborati sono supportati. Il comando seguente eseguito da una finestra CMD visualizza i dati del catalogo Winsock nella console:

**netsh winsock show catalog**

L'output includerà un elenco che contiene alcuni dei dati delle strutture [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) supportate nel computer locale. Cercare il termine RAW/IP o RAW/IPv6 nel campo Descrizione per trovare i protocolli che supportano i socket non elaborati.

## <a name="creating-a-raw-socket"></a>Creazione di un socket non elaborato

Per creare un socket di tipo **SOCK \_ RAW,** chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con il parametro *af* (famiglia di indirizzi) impostato su AF INET o \_ AF \_ INET6,   il parametro di tipo impostato su **SOCK \_ RAW** e il parametro del protocollo impostato sul numero di protocollo richiesto. Il *parametro* protocol diventa il valore del protocollo nell'intestazione IP ( SCTP è 132, ad esempio).

> [!Note]  
> Un'applicazione non può specificare zero  (0) come parametro di protocollo per le funzioni [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket),  [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)e [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) se il parametro di tipo è impostato su **SOCK \_ RAW.**

 

I socket non elaborati offrono la possibilità di modificare il trasporto sottostante, in modo che possano essere usati per scopi dannosi che rappresentano una minaccia per la sicurezza. Pertanto, solo i membri del gruppo Administrators possono creare socket di tipo SOCK \_ RAW Windows 2000 e versioni successive.

## <a name="send-and-receive-operations"></a>Operazioni di invio e ricezione

Dopo che un'applicazione ha creato un socket di tipo **SOCK \_ RAW,** questo socket può essere usato per inviare e ricevere dati. Tutti i pacchetti inviati o ricevuti su un socket di tipo **SOCK \_ RAW** vengono trattati come datagrammi in un socket non connesso.

Le regole seguenti si applicano alle operazioni su socket **\_ RAW SOCK:**

-   La [**funzione sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) [**o WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) viene in genere usata per inviare dati su un socket di tipo **SOCK \_ RAW.** L'indirizzo di destinazione può essere qualsiasi indirizzo valido nella famiglia di indirizzi del socket, incluso un indirizzo broadcast o multicast. Per inviare a un indirizzo di trasmissione, un'applicazione deve aver usato [**setockopt con**](/windows/desktop/api/winsock/nf-winsock-setsockopt) SO \_ BROADCAST abilitato. In caso contrario, **sendto** o **WSASendTo** avrà esito negativo con il codice di errore [WSAEACCES](windows-sockets-error-codes-2.md). Per ip, un'applicazione può inviare a qualsiasi indirizzo multicast (senza diventare un membro del gruppo).
-   Quando si inviano dati IPv4, un'applicazione può scegliere se specificare l'intestazione IPv4 nella parte anteriore del datagramma in uscita per il pacchetto. Se l'opzione socket **\_ HDRINCL IP** è impostata su true per un socket IPv4 (famiglia di indirizzi di AF INET), l'applicazione deve fornire l'intestazione IPv4 nei dati in uscita per le operazioni di \_ invio. Se questa opzione socket è false (impostazione predefinita), l'intestazione IPv4 non deve includere i dati in uscita per le operazioni di invio.
-   Quando si inviano dati IPv6, un'applicazione può scegliere se specificare l'intestazione IPv6 nella parte anteriore del datagramma in uscita per il pacchetto. Se l'opzione socket **\_ IPV6 HDRINCL** è impostata su true per un socket IPv6 (famiglia di indirizzi af INET6), l'applicazione deve fornire l'intestazione IPv6 nei dati in uscita per le operazioni di \_ invio. L'impostazione predefinita per questa opzione è false. Se questa opzione socket è false (impostazione predefinita), l'intestazione IPv6 non deve essere inclusa nei dati in uscita per le operazioni di invio. Per IPv6, non è necessario includere l'intestazione IPv6. Se le informazioni sono disponibili usando le funzioni socket, l'intestazione IPv6 non deve essere inclusa per evitare problemi di compatibilità in futuro. Questi problemi sono descritti nella RFC 3542 pubblicata da IETF. **L'uso dell'opzione socket \_ HDRINCL IPV6** non è consigliato e potrebbe essere deprecato in futuro.
-   La [**funzione recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) viene in genere usata per ricevere dati su un socket di tipo **SOCK \_ RAW.** Entrambe queste funzioni hanno un'opzione per restituire l'indirizzo IP di origine da cui è stato inviato il pacchetto. I dati ricevuti sono un datagramma da un socket non connesso.
-   Per IPv4 (famiglia di indirizzi di AF INET), un'applicazione riceve l'intestazione IP nella parte anteriore di ogni datagramma ricevuto indipendentemente dall'opzione \_ socket **\_ HDRINCL IP.**
-   Per IPv6 (famiglia di indirizzi di AF INET6), un'applicazione riceve tutti gli elementi dopo l'ultima intestazione IPv6 in ogni datagramma ricevuto indipendentemente dall'opzione \_ socket **\_ HDRINCL IPV6.** L'applicazione non riceve intestazioni IPv6 usando un socket non elaborato.
-   I datagrammi ricevuti vengono copiati in tutti i socket **\_ RAW SOCK** che soddisfano le condizioni seguenti:

    -   Il numero di protocollo specificato nel *parametro protocol* al momento della creazione del socket deve corrispondere al numero di protocollo nell'intestazione IP del datagramma ricevuto.
    -   Se per il socket è definito un indirizzo IP locale, deve corrispondere all'indirizzo di destinazione specificato nell'intestazione IP del datagramma ricevuto. Un'applicazione può specificare l'indirizzo IP locale chiamando la [**funzione bind.**](/windows/desktop/api/winsock/nf-winsock-bind) Se per il socket non viene specificato alcun indirizzo IP locale, i datagrammi vengono copiati nel socket indipendentemente dall'indirizzo IP di destinazione nell'intestazione IP del datagramma ricevuto.
    -   Se per il socket è definito un indirizzo estraneo, deve corrispondere all'indirizzo di origine specificato nell'intestazione IP del datagramma ricevuto. Un'applicazione può specificare l'indirizzo IP estraneo chiamando la [**funzione connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) o [**WSAConnect.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) Se non viene specificato alcun indirizzo IP estraneo per il socket, i datagrammi vengono copiati nel socket indipendentemente dall'indirizzo IP di origine nell'intestazione IP del datagramma ricevuto.

È importante comprendere che alcuni socket di tipo **SOCK \_ RAW** possono ricevere molti datagrammi imprevisti. Ad esempio, un programma PING può creare un socket di tipo **SOCK \_ RAW** per inviare richieste echo ICMP e ricevere risposte. Anche se l'applicazione prevede risposte echo ICMP, tutti gli altri messaggi ICMP (ad esempio ICMP HOST UNREACHABLE) possono essere recapitati \_ a questa applicazione. Inoltre, se in un computer sono aperti più socket **\_ RAW SOCK** contemporaneamente, gli stessi datagrammi possono essere recapitati a tutti i socket aperti. Un'applicazione deve avere un meccanismo per riconoscere i datagrammi di interesse e ignorare tutti gli altri. Per un programma PING, un meccanismo di questo tipo potrebbe includere il controllo dell'intestazione IP ricevuta per gli identificatori univoci nell'intestazione ICMP ,ad esempio l'ID processo dell'applicazione.

> [!Note]  
> Per usare un socket di tipo **SOCK \_ RAW** sono necessari privilegi amministrativi. Gli utenti che eseguono applicazioni Winsock che usano socket non elaborati devono essere membri del gruppo Administrators nel computer locale. In caso contrario, le chiamate socket non elaborati avranno esito negativo con codice di errore [WSAEACCES](windows-sockets-error-codes-2.md). In Windows Vista e versioni successive, l'accesso per i socket non elaborati viene applicato durante la creazione del socket. Nelle versioni precedenti di Windows, l'accesso per i socket non elaborati viene applicato durante altre operazioni socket.

 

## <a name="common-uses-of-raw-sockets"></a>Usi comuni dei socket non elaborati

Un uso comune dei socket non elaborati è la risoluzione dei problemi delle applicazioni che devono esaminare in dettaglio i pacchetti IP e le intestazioni. Ad esempio, un socket non elaborato può essere usato con SIO RCVALL IOCTL per consentire a un socket di ricevere tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia \_ di rete. Per altre informazioni, vedere le informazioni [**di riferimento su SIO \_ RCVALL.**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85))

## <a name="limitations-on-raw-sockets"></a>Limitazioni sui socket non elaborati

In Windows 7, Windows Vista, Windows XP con Service Pack 2 (SP2) e Windows XP con Service Pack 3 (SP3), la possibilità di inviare traffico su socket non elaborati è stata limitata in diversi modi:

-   I dati TCP non possono essere inviati tramite socket non elaborati.
-   I datagrammi UDP con un indirizzo di origine non valido non possono essere inviati tramite socket non elaborati. L'indirizzo di origine IP per qualsiasi datagramma UDP in uscita deve esistere in un'interfaccia di rete o il datagramma viene eliminato. Questa modifica è stata apportata per limitare la capacità di codice dannoso di creare attacchi Denial of Service distribuiti e limita la possibilità di inviare pacchetti falsificati (pacchetti TCP/IP con un indirizzo IP di origine contraffatto).
-   Non è consentita [**una chiamata**](/windows/desktop/api/winsock/nf-winsock-bind) alla funzione bind con un socket non elaborato per il protocollo TCP IPPROTO. \_
    > [!Note]  
    > La [**funzione di**](/windows/desktop/api/winsock/nf-winsock-bind) associazione con un socket non elaborato è consentita per altri protocolli,ad esempio \_ IPPROTO, UDP IPPROTO \_ o SCTP IPPROTO. \_

     

Queste restrizioni precedenti non si applicano a Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 o alle versioni del sistema operativo precedenti Windows XP con SP2.

> [!Note]  
> L'implementazione Microsoft di TCP/IP Windows è in grado di aprire un socket UDP o TCP non elaborato in base alle restrizioni precedenti. Altri provider Winsock potrebbero non supportare l'uso di socket non elaborati.

 

Esistono altre limitazioni per le applicazioni che usano un socket di tipo **SOCK \_ RAW.** Ad esempio, tutte le applicazioni in ascolto di un protocollo specifico riceveranno tutti i pacchetti ricevuti per questo protocollo. Questo potrebbe non essere quello desiderato per più applicazioni che usano un protocollo. Questo non è adatto anche per le applicazioni ad alte prestazioni. Per risolvere questi problemi, potrebbe essere necessario scrivere un driver di Windows di rete (driver di dispositivo) per il protocollo di rete specifico. In Windows Vista e versioni successive, il kernel Winsock (WSK), è possibile usare una nuova interfaccia di programmazione di rete in modalità kernel indipendente dal trasporto per scrivere un driver del protocollo di rete. In Windows Server 2003 e versioni precedenti, è possibile scrivere un provider Transport Driver Interface (TDI) e una DLL helper Winsock per supportare il protocollo di rete. Il protocollo di rete verrà quindi aggiunto al catalogo Winsock come protocollo supportato. Ciò consente a più applicazioni di aprire socket per questo protocollo specifico e il driver di dispositivo può tenere traccia del socket che riceve pacchetti ed errori specifici. Per informazioni sulla scrittura di un provider di protocolli di rete, vedere le sezioni relative a WSK e TDI in Windows Driver Kit (WDK).

Le applicazioni devono anche essere consapevoli dell'impatto che possono avere le impostazioni del firewall sull'invio e sulla ricezione di pacchetti tramite socket non elaborati.

 

 
