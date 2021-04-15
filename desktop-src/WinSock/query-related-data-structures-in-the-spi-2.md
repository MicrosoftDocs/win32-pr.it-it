---
description: La struttura WSAQUERYSET viene utilizzata per creare query per la funzione NSPLookupServiceBegin e per recapitare i risultati della query per la funzione NSPLookupServiceNext.
ms.assetid: 017b5828-bc6e-42b7-aba7-21648b2dd707
title: Query-Related le strutture dei dati in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ce5a7016bd2ad96f464137177036b470c64a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554976"
---
# <a name="query-related-data-structures-in-the-spi"></a>Query-Related le strutture dei dati in SPI

La struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) viene utilizzata per creare query per [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)e per recapitare i risultati delle query per [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext). Si tratta di una struttura complessa perché contiene puntatori a diverse altre strutture, alcune delle quali fanno riferimento ancora ad altre strutture. La relazione tra **WSAQUERYSET** e le strutture a cui fa riferimento è illustrata di seguito:

![strutture WSAQUERYSET](images/ovrvw3-2.png)

All'interno della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , la maggior parte dei membri è autonoma, ma alcuni meritano una spiegazione aggiuntiva. **DwSize** verrà compilato con sizeof ( **WSAQUERYSET**) e potrà essere usato dai provider dello spazio dei nomi per rilevare e adattare a versioni diverse della struttura **WSAQUERYSET** che possono essere visualizzate.

Il membro **dwOutputFlags** viene utilizzato da un provider dello spazio dei nomi per fornire dati aggiuntivi sui risultati della query. Per ulteriori informazioni, vedere [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext).

La struttura [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) a cui fa riferimento **lpVersion** viene usata sia per il vincolo di query che per i risultati. Per le query, il membro **dwVersion** indica la versione desiderata del servizio. Il membro **ecHow** è un tipo enumerato che specifica come verrà eseguito il confronto. Le scelte sono COMP \_ Equals, che richiede una corrispondenza esatta nella versione, oppure comp \_ NOTLESS, che specifica che il numero di versione del servizio non deve essere inferiore al valore di **dwVersion**.

L'interpretazione di **dwNameSpace** e **lpNSProviderId** dipende dal modo in cui viene utilizzata la struttura e viene descritta ulteriormente nelle singole descrizioni di funzioni che utilizzano questa struttura.

Il membro **lpszContext** si applica agli spazi dei nomi gerarchici e specifica il punto iniziale di una query o la posizione all'interno della gerarchia in cui risiede il servizio. Le regole generali sono le seguenti:

-   Il valore **null**, Blank ("") avvierà la ricerca nel contesto predefinito.
-   Il valore " \\ " avvia la ricerca nella parte superiore dello spazio dei nomi.
-   Qualsiasi altro valore avvia la ricerca nel punto designato.

I provider che non supportano containment possono restituire un errore se è specificato un valore diverso da "" o " \\ ". I provider che supportano il contenimento limitato, ad esempio i gruppi, devono accettare "", " \\ " o un punto designato. I contesti sono specifici dello spazio dei nomi. Se **dwNameSpace** è NS \_ All, solo "" o " \\ " devono essere passati come contesto perché sono riconosciuti da tutti gli spazi dei nomi.

Il membro **lpszQueryString** viene utilizzato per fornire informazioni aggiuntive sulle query specifiche dello spazio dei nomi, ad esempio una stringa che descrive un nome di protocollo di trasporto e di servizio noto, come in "FTP/TCP".

La struttura [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) a cui fa riferimento **lpafpProtocols** viene utilizzata solo a scopo di query e fornisce un elenco di protocolli per vincolare la query. Questi protocolli sono rappresentati come coppie (famiglia di indirizzi, protocollo), perché i valori del protocollo hanno un significato solo nel contesto di una famiglia di indirizzi.

La matrice della struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) a cui fa riferimento **lpcsaBuffer** contiene tutte le informazioni necessarie per un servizio da usare per stabilire un ascolto o un client da usare per stabilire una connessione al servizio. I membri **LocalAddr** e **IndirizzoRemoto** contengono entrambi direttamente una struttura di [**\_ indirizzi del socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) . Un servizio creerebbe un socket usando la tupla (LocalAddr. lpSockaddr->\_ gruppo SA, iSocketType, iProtocol). Il socket viene associato a un indirizzo locale usando LocalAddr. lpSockaddr e LocalAddr. lpSockaddrLength. Il client crea il relativo socket con la tupla (IndirizzoRemoto. lpSockaddr->\_ gruppo SA, iSocketType, iProtocol) e usa la combinazione di IndirizzoRemoto. lpSockaddr e IndirizzoRemoto. lpSockaddrLength quando si effettua una connessione remota.

 

 
