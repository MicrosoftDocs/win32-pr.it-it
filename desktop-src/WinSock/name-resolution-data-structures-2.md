---
description: Strutture di dati di risoluzione dei nomi in Windows Sockets (Winsock).
ms.assetid: 87c54141-41e2-4eaa-ae3b-84598e8281d9
title: Strutture dei dati di risoluzione dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e6f3b889d295241bb0cdb9c0182babf0c5b8115e7eff7e86c27b65c992c452
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794791"
---
# <a name="name-resolution-data-structures"></a>Strutture dei dati di risoluzione dei nomi

Esistono diverse importanti strutture di dati che vengono usate ampiamente in tutte le funzioni di risoluzione dei nomi.

## <a name="query-related-data-structures"></a>Query-Related strutture di dati

La [**struttura WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) viene usata per creare query [**per WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)e per recapitare i risultati delle query per [**WSALookupServiceNext.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) Si tratta di una struttura complessa perché contiene puntatori a diverse altre strutture, alcune delle quali fanno riferimento ad altre strutture. La relazione tra la [**struttura WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) e le strutture a cui fa riferimento è illustrata come segue.

![relazione tra wsaqueryset e le strutture associate](images/ovrvw3-2.png)

[**All'interno della struttura WSAQUERYSET,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) la maggior parte dei membri è auto-esplicativa, ma alcuni meritano una spiegazione aggiuntiva. Il membro **dwSize** deve sempre essere compilato con sizeof(**WSAQUERYSET**), perché viene usato dai provider dello spazio dei nomi per rilevare e adattarsi a versioni diverse della struttura **WSAQUERYSET** che possono essere visualizzate nel tempo.

Il **membro dwOutputFlags** viene usato da un provider dello spazio dei nomi per fornire informazioni aggiuntive sui risultati della query. Per informazioni dettagliate, vedere la [**funzione WSALookupServiceNext.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)

La [**struttura WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) a cui fa riferimento il membro **lpversion** viene usata sia per il vincolo di query che per i risultati. Per le query, **il membro dwVersion** indica la versione desiderata del servizio. Il **membro ecHow** è un tipo enumerato che specifica come eseguire il confronto. Le opzioni sono COMP EQUALS che richiede che si verifichi una corrispondenza esatta nella versione o COMP NOTLESS che specifica che il numero di versione del servizio non è inferiore al valore del \_ \_ membro **dwVersion.**

L'interpretazione di **dwNameSpace** e **lpNSProviderId** dipende dal modo in cui viene usata la struttura e viene descritta ulteriormente nelle descrizioni delle singole funzioni che utilizzano questa struttura.

Il **membro lpszContext** si applica agli spazi dei nomi gerarchici e specifica il punto iniziale di una query o la posizione all'interno della gerarchia in cui risiede il servizio. Le regole generali sono le seguenti:

-   Il valore **NULL**, vuoto ("") avvia la ricerca nel contesto predefinito.
-   Il valore " \\ " avvia la ricerca all'inizio dello spazio dei nomi.
-   Qualsiasi altro valore avvia la ricerca nel punto designato.

I provider che non supportano il contenimento possono restituire un errore se viene specificato un valore diverso da "" \\ o "". I provider che supportano il contenimento limitato, ad esempio i gruppi, devono accettare "", \\ " " o un punto designato. I contesti sono specifici dello spazio dei nomi. Se il **membro dwNameSpace** è NS ALL, solo "" o " " devono essere passati come contesto perché sono riconosciuti \_ da tutti gli spazi dei \\ nomi.

Il **membro lpszQueryString** viene usato per fornire informazioni aggiuntive specifiche dello spazio dei nomi, ad esempio una stringa che descrive un nome noto del servizio e del protocollo di trasporto, come in "FTP/TCP".

La [**struttura AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) a cui fa riferimento il membro **lpafpProtocols** viene usata solo a scopo di query e fornisce un elenco di protocolli per vincolare la query. Questi protocolli sono rappresentati come coppie (famiglia di indirizzi, protocollo), poiché i valori del protocollo hanno significato solo all'interno del contesto di una famiglia di indirizzi.

La matrice della struttura [**CSADDR \_ INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) a cui fa riferimento il membro **lpcsaBuffer** contiene tutte le informazioni necessarie per un servizio da usare per stabilire un ascolto o per un client da usare per stabilire una connessione al servizio. I **membri LocalAddr** **e RemoteAddr** contengono entrambi direttamente una [**struttura SOCKET \_ ADDRESS.**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)

Un servizio creerebbe un socket chiamando la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) usando la tupla *di LocalAddr.lpSockaddr->sa \_ family,* *iSocketType* e *iProtocol* come parametri. Un servizio associa il socket a un indirizzo locale chiamando la funzione [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) usando *LocalAddr.lpSockaddr* e *LocalAddr.lpSockaddrLength* come parametri.

Un client crea il socket chiamando la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) usando la tupla *di LocalAddr.lpSockaddr->sa \_ family*, *iSocketType* e *iProtocol* come parametri. Un client usa la combinazione di *RemoteAddr.lpSockaddr* e *RemoteAddr.lpSockaddrLength* come parametri quando si stabilisce una connessione remota usando la funzione connect [**,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)o [**WSAConnect.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)

## <a name="service-class-data-structures"></a>Strutture di dati della classe di servizio

Quando viene installata una nuova classe di servizio, è necessario preparare e fornire una struttura [**WSASERVICECLASSINFO.**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) Questa struttura è anche costituita da sottostrutture che contengono una serie di membri che si applicano a spazi dei nomi specifici. Una struttura di dati delle informazioni sulla classe è la seguente:

![Architettura delle strutture di dati delle classi di servizio](images/ovrvw3-3.png)

Per ogni classe di servizio è presente una singola [**struttura WSASERVICECLASSINFO.**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) All'interno della struttura [**WSASERVICECLASSINFO,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) l'identificatore univoco della classe di servizio è contenuto nel membro **lpServiceClassId** e il membro **lpServiceClassName** fa riferimento a una stringa di visualizzazione associata. Si tratta della stringa restituita dalla [**funzione WSAGetServiceClassNameByClassId.**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)

Il membro **lpClassInfos** nella struttura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) fa riferimento a una matrice di strutture **WSANSCLASSINFO,** ognuna delle quali fornisce un membro denominato e tipiato che si applica a uno spazio dei nomi specificato. Esempi di valori per il membro **lpszName** includono: "SapId", "TcpPort", "UdpPort" e così via. Queste stringhe sono in genere specifiche dello spazio dei nomi identificato nel **membro dwNameSpace.** I valori tipici per **il membro dwValueType** possono essere REG \_ DWORD, REG \_ SZ e così via. Il **membro dwValueSize** indica la lunghezza dell'elemento di dati a cui punta **lpValue**.

L'intera raccolta di dati rappresentati in una **struttura WSASERVICECLASSINFO** viene fornita a ogni provider dello spazio dei nomi quando viene richiamata la funzione [**WSAInstallServiceClass.**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) Ogni singolo provider dello spazio dei nomi passa quindi al set di dati l'elenco delle strutture **WSANSCLASSINFO** e mantiene le informazioni applicabili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)
</dt> <dt>

[**CSADDR \_ INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[Modello di risoluzione dei nomi](name-resolution-model-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> <dt>

[**INDIRIZZO \_ SOCKET**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)
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

 

 
