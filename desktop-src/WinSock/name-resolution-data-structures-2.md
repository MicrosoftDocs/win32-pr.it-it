---
description: Strutture dei dati di risoluzione dei nomi in Windows Sockets (Winsock).
ms.assetid: 87c54141-41e2-4eaa-ae3b-84598e8281d9
title: Strutture dei dati di risoluzione dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf1f76607ade81503a1057dc21890ac38d5ec265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571588"
---
# <a name="name-resolution-data-structures"></a>Strutture dei dati di risoluzione dei nomi

Sono disponibili diverse strutture di dati importanti che vengono utilizzate ampiamente in tutte le funzioni di risoluzione dei nomi.

## <a name="query-related-data-structures"></a>Strutture dei dati di Query-Related

La struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) viene utilizzata per creare query per [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)e per recapitare i risultati delle query per [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta). Si tratta di una struttura complessa perché contiene puntatori a diverse altre strutture, alcune delle quali fanno riferimento ancora ad altre strutture. La relazione tra la struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) e le strutture a cui fa riferimento è illustrata di seguito.

![relazione tra WSAQUERYSET e le strutture associate](images/ovrvw3-2.png)

All'interno della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , la maggior parte del membro è autonoma, ma alcuni meritano una spiegazione aggiuntiva. Il membro **dwSize** deve sempre essere compilato con sizeof (**WSAQUERYSET**), perché viene usato dai provider dello spazio dei nomi per rilevare e adattare a versioni diverse della struttura **WSAQUERYSET** che possono apparire nel tempo.

Il membro **dwOutputFlags** viene utilizzato da un provider dello spazio dei nomi per fornire informazioni aggiuntive sui risultati della query. Per informazioni dettagliate, vedere la funzione [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) .

La struttura [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) a cui fa riferimento il membro **lpVersion** viene usata sia per il vincolo di query che per i risultati. Per le query, il membro **dwVersion** indica la versione desiderata del servizio. Il membro **ecHow** è un tipo enumerato che specifica come può essere eseguito il confronto. Le scelte sono COMP \_ Equals, che richiede una corrispondenza esatta nella versione, oppure comp \_ NOTLESS, che specifica che il numero di versione del servizio non deve essere inferiore al valore del membro **dwVersion** .

L'interpretazione di **dwNameSpace** e **lpNSProviderId** dipende dal modo in cui viene utilizzata la struttura e viene descritta ulteriormente nelle singole descrizioni di funzioni che utilizzano questa struttura.

Il membro **lpszContext** si applica agli spazi dei nomi gerarchici e specifica il punto iniziale di una query o la posizione all'interno della gerarchia in cui risiede il servizio. Le regole generali sono le seguenti:

-   Il valore **null**, Blank ("") avvia la ricerca nel contesto predefinito.
-   Il valore " \\ " avvia la ricerca nella parte superiore dello spazio dei nomi.
-   Qualsiasi altro valore avvia la ricerca nel punto designato.

I provider che non supportano containment possono restituire un errore se è specificato un valore diverso da "" o " \\ ". I provider che supportano il contenimento limitato, ad esempio i gruppi, devono accettare "", " \\ " o un punto designato. I contesti sono specifici dello spazio dei nomi. Se il membro **dwNameSpace** è NS \_ All, è necessario passare come contesto solo "" o " \\ ", perché sono riconosciuti da tutti gli spazi dei nomi.

Il membro **lpszQueryString** viene utilizzato per fornire informazioni aggiuntive sulle query specifiche dello spazio dei nomi, ad esempio una stringa che descrive un nome di protocollo di trasporto e di servizio noto, come in "FTP/TCP".

La struttura [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) a cui fa riferimento il membro **lpafpProtocols** viene utilizzata solo a scopo di query e fornisce un elenco di protocolli per vincolare la query. Questi protocolli sono rappresentati come coppie (famiglia di indirizzi, protocollo), perché i valori del protocollo hanno un significato solo nel contesto di una famiglia di indirizzi.

La matrice della struttura [**di \_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) a cui fa riferimento il membro **lpcsaBuffer** contiene tutte le informazioni necessarie per un servizio da usare per stabilire un ascolto o per un client da usare per stabilire una connessione al servizio. I membri **LocalAddr** e **IndirizzoRemoto** contengono entrambi direttamente una struttura di [**\_ indirizzi del socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) .

Un servizio creerebbe un socket chiamando il [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o la funzione [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) usando la tupla di *LocalAddr. lpSockaddr->\_ gruppo SA*, *iSocketType* e *iProtocol* come parametri. Un servizio associa il socket a un indirizzo locale chiamando la funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) usando *LocalAddr. lpSockaddr* e *LocalAddr. lpSockaddrLength* come parametri.

Un client crea il relativo socket chiamando il [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o la funzione [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) usando la tupla di *LocalAddr. lpSockaddr->\_ gruppo SA*, *iSocketType* e *iProtocol* come parametri. Un client usa la combinazione di *IndirizzoRemoto. lpSockaddr* e *IndirizzoRemoto. lpSockaddrLength* come parametri quando si effettua una connessione remota usando la funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)o [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) .

## <a name="service-class-data-structures"></a>Strutture di dati della classe di servizio

Quando viene installata una nuova classe di servizio, è necessario preparare e fornire una struttura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . Questa struttura è costituita anche da sottostrutture che contengono una serie di membri che si applicano a spazi dei nomi specifici. Una struttura di dati di informazioni sulle classi è la seguente:

![architettura di strutture di dati della classe di servizio](images/ovrvw3-3.png)

Per ogni classe di servizio è presente una sola struttura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . All'interno della struttura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) , l'identificatore univoco della classe del servizio è contenuto nel membro **lpServiceClassId** e a una stringa di visualizzazione associata viene fatto riferimento dal membro **lpServiceClassName** . Si tratta della stringa restituita dalla funzione [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) .

Il membro **lpClassInfos** nella struttura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) fa riferimento a una matrice di strutture **WSANSCLASSINFO** , ciascuna delle quali fornisce un membro denominato e tipizzato che si applica a uno spazio dei nomi specificato. Esempi di valori per il membro **lpszName** includono: "SAPID", "TCPPort", "portaUDP" e così via. Queste stringhe sono in genere specifiche dello spazio dei nomi identificato nel membro **dwNameSpace** . I valori tipici per il membro **dwValueType** potrebbero essere reg \_ DWORD, reg \_ SZ e così via. Il membro **dwValueSize** indica la lunghezza dell'elemento dati a cui punta **lpValue**.

L'intera raccolta di dati rappresentati in una struttura **WSASERVICECLASSINFO** viene fornita a ogni provider dello spazio dei nomi quando viene richiamata la funzione [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) . Ogni singolo provider dello spazio dei nomi quindi setaccia l'elenco di strutture **WSANSCLASSINFO** e mantiene le informazioni applicabili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)
</dt> <dt>

[**\_informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[Modello di risoluzione dei nomi](name-resolution-model-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> <dt>

[**\_indirizzo socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)
</dt> <dt>

[Riepilogo delle funzioni di risoluzione dei nomi](summary-of-name-resolution-functions-2.md)
</dt> <dt>

[**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)
</dt> </dl>

 

 
