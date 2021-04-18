---
description: In questa sezione viene fornita una panoramica della divisione di responsabilità tra il \_32.dll WS2 e i provider di servizi di trasporto.
ms.assetid: e1ea1e99-a2bc-4e76-91f6-e388c39dfbbb
title: Divisione del trasporto delle responsabilità tra i provider di servizi e DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142ac98c95e95c310c2eefb7bfdaf1f70a03bf28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315764"
---
# <a name="transport-division-of-responsibilities-between-dll-and-service-providers"></a>Divisione del trasporto delle responsabilità tra i provider di servizi e DLL

In questa sezione viene fornita una panoramica della divisione di responsabilità tra il \_32.dll WS2 e i provider di servizi di trasporto.

## <a name="ws2_32dll-functionality-for-transport"></a>WS2 \_32.dll funzionalità per il trasporto

L'attività principale della parte relativa al trasporto di dati del \_32.dll WS2 è quella di fungere da Gestione traffico tra i provider di servizi e le applicazioni. Con molti provider di servizi diversi che interagiscono con la stessa applicazione, ogni provider di servizi interagisce rigorosamente con la32.dll di WS2 \_ . La DLL si occupa di:

-   Selezione di un provider di servizi appropriato per la creazione di socket in base a una descrizione del protocollo.
-   L'invio di chiamate di procedure dell'applicazione che coinvolgono un socket al provider di servizi appropriato che ha creato o controlla tale socket. I provider di servizi non sono consapevoli di ciò che si sta verificando.

Non è necessario preoccuparsi dei dettagli della cooperabilità tra loro o anche dell'esistenza di altri provider di servizi. Astrarre i provider di servizi in un'interfaccia DLL coerente ed eseguendo questa funzione di routing automatico del traffico, il \_32.dll WS2 consente alle applicazioni di interagire con diversi provider senza richiedere che le applicazioni siano in grado di riconoscere le divisioni tra i provider, in cui sono installati provider diversi.

Il \_32.dll WS2 si basa sui parametri delle funzioni di creazione socket API ( [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)) per determinare il provider di servizi da utilizzare. Il provider del servizio di trasporto selezionato verrà richiamato tramite la funzione [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) . Nel caso della funzione **socket** , il WS2 \_32.dll trova la prima voce nel set di strutture di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) installate che corrisponde ai valori specificati nella tupla formata dai parametri (*famiglia di indirizzi*, *tipo di socket*, *protocollo*). Per mantenere la compatibilità con le versioni precedenti, WS2 \_32.dll considera il valore zero per la *famiglia di indirizzi* o il *tipo di socket* come valore jolly. Il valore zero per il protocollo non è considerato un valore con caratteri jolly da WS2 \_32.dll a meno che tale comportamento non sia indicato per un particolare protocollo, in quanto il valore PFL \_ corrisponde al \_ flag zero del protocollo \_ nella struttura delle **\_ informazioni di WSAPROTOCOL** .

Per la funzione [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) , se viene specificato null per *lpProtocolInfo*, il comportamento è esattamente come descritto solo per [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket). Se si fa riferimento a una struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) , tuttavia, la32.dll WS2 non \_ esegue alcuna funzione corrispondente ma inoltra immediatamente la richiesta di creazione del socket al provider del servizio di trasporto associato alla struttura di **\_ informazioni WSAPROTOCOL** indicata. I valori per la tupla (*famiglia di indirizzi,* *tipo di socket*) vengono forniti intatti al provider di servizi nella funzione [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) . I provider di servizi possono ignorare o prestare attenzione ai valori dei parametri (*famiglia di indirizzi,* *tipo di socket*), come appropriato, ma non devono indicare una condizione di errore quando il valore della famiglia di *indirizzi* o del *tipo di socket* è zero. Inoltre, i provider di servizi non devono indicare una condizione di errore quando la costante del manifesto dalle \_ informazioni sul protocollo \_ è contenuta in qualsiasi parametro (*famiglia di indirizzi,* *tipo di socket*). Questo valore indica semplicemente che l'applicazione desidera usare i valori trovati nei parametri corrispondenti della struttura di **\_ informazioni di WSAPROTOCOL** : (**iAddressFamily**, **iSocketType**, **iProtocol**).

Come parte della creazione del socket, un provider di servizi informa WS2 \_32.dll sull'associazione tra se stesso e il nuovo socket mediante parametri passati a [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) o [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle). Il \_32.dll WS2 tiene traccia dell'associazione tra handle di socket e provider di servizi particolari. Ogni volta che viene chiamata una funzione dell'interfaccia dell'applicazione che fa riferimento a un handle di socket, WS2 \_32.dll cerca l'associazione e chiama la corrispondente funzione dell'interfaccia del provider di servizi del provider di servizi appropriato.

Oltre al servizio di routing del traffico principale, WS2 \_32.dll offre diversi altri servizi, ad esempio l'enumerazione del protocollo, la gestione del descrittore di socket (allocazione, deallocazione e associazione di valori di contesto per provider di servizi non file System, gestione dell'hook di blocco in base ai singoli thread, utilità di scambio di byte, Accodamento di chiamate di procedure asincrone (APC) per facilitare la chiamata delle routine di completamento di I/O e la negoziazione della versione tra le applicazioni e il \_32.dll WS2, nonché tra i \_ provider di servizi e32.dll WS2.

## <a name="transport-service-provider-functionality"></a>Funzionalità del provider di servizi di trasporto

I provider di servizi implementano il protocollo di trasporto effettivo, che include funzioni come la configurazione di connessioni, il trasferimento di dati, l'esercizio del controllo di flusso e il controllo degli errori e così via. Il \_32.dll WS2 non ha alcuna conoscenza del modo in cui vengono realizzate le richieste ai provider di servizi; questo dipende dall'implementazione del provider di servizi. L'implementazione di tali funzioni può variare significativamente da un provider a un altro. I provider di servizi nascondono i dettagli specifici dell'implementazione del modo in cui vengono eseguite le operazioni di rete.

I provider di servizi di trasporto possono essere divisi in due categorie: quelli i cui descrittori di socket sono veri file system handle (e sono in seguito definiti provider del file system installabile (IFS). i restanti sono detti provider non IFS. Il \_32.dll WS2 passa sempre il descrittore di socket del provider di servizi di trasporto su un'applicazione Windows Sockets, in modo che le applicazioni siano libere di sfruttare i descrittori di socket file System handle.

Per riepilogare: i provider di servizi implementano i protocolli specifici della rete di basso livello. Il \_32.dll WS2 fornisce la gestione del traffico di livello medio che interconnette questi protocolli di trasporto con le applicazioni. Le applicazioni a loro volta forniscono i criteri di utilizzo di questi flussi di traffico e di operazioni specifiche della rete per eseguire le funzioni desiderate dall'utente.

 

 
