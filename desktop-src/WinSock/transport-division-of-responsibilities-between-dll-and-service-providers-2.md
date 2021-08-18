---
description: Questa sezione offre una panoramica della divisione di responsabilità tra i32.dll Ws2 e i provider di \_ servizi di trasporto.
ms.assetid: e1ea1e99-a2bc-4e76-91f6-e388c39dfbbb
title: Divisione del trasporto di responsabilità tra DLL e provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c256cb03bcc9e3f8746db5196c21fc2de0a8b157304a205587b275acc0bbb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733221"
---
# <a name="transport-division-of-responsibilities-between-dll-and-service-providers"></a>Divisione del trasporto di responsabilità tra DLL e provider di servizi

Questa sezione offre una panoramica della divisione di responsabilità tra i32.dll Ws2 e i provider di \_ servizi di trasporto.

## <a name="ws2_32dll-functionality-for-transport"></a>Funzionalità32.dll Ws2 \_ per il trasporto

L'attività principale della parte relativa al trasporto dati del32.dll Ws2 è quella di fungere da gestione del traffico tra provider di \_ servizi e applicazioni. Con diversi provider di servizi che interagiscono con la stessa applicazione, ogni provider di servizi interagisce esclusivamente con il32.dll \_ Ws2. La DLL si occupa di:

-   Selezione di un provider di servizi appropriato per la creazione di socket in base a una descrizione del protocollo.
-   Inoltro di chiamate di procedura dell'applicazione che coinvolgono un socket al provider di servizi appropriato che ha creato o controlla tale socket. I provider di servizi non sono consapevoli del fatto che si stia verificando una qualsiasi di queste.

Non devono preoccuparsi dei dettagli della collaborazione tra loro o anche dell'esistenza di altri provider di servizi. Astraendo i provider di servizi in un'interfaccia DLL coerente ed eseguendo questa funzione di routing automatico del traffico, il32.dll Ws2 consente alle applicazioni di interagire con un'ampia gamma di provider senza richiedere che le applicazioni siano consapevoli delle divisioni tra provider, in cui sono installati provider \_ diversi.

L'32.dll Ws2 si basa sui parametri delle funzioni di creazione del socket API ( socket e \_ [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)) per determinare quale provider di servizi utilizzare. [](/windows/desktop/api/Winsock2/nf-winsock2-socket) Il provider del servizio di trasporto selezionato verrà richiamato tramite la [**funzione WSPSocket.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) Nel caso della funzione **socket,** il32.dll Ws2 trova la prima voce nel set di strutture \_ [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) installate checorrispondono ai valori forniti nella tupla formata dai parametri ( famiglia di indirizzi , *tipo di socket*, *protocollo*). Per mantenere la compatibilità con le versioni precedenti, il32.dll Ws2 considera il valore zero per la famiglia di indirizzi o il tipo \_ *di socket* come valore jolly.  Il valore zero per protocol non viene considerato un valore jolly dal32.dll Ws2, a meno che tale comportamento non venga indicato per un protocollo specifico con il flag PFL MATCHES PROTOCOL ZERO impostato nella struttura \_ \_ \_ \_ **WSAPROTOCOL \_ INFO.**

Per la [**funzione WSASocket,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) se viene fornito null per *lpProtocolInfo*, il comportamento è esattamente come descritto per [**il socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket). Se si fa riferimento a una struttura [**WSAPROTOCOL \_ INFO,**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) tuttavia, il32.dll Ws2 non esegue alcuna funzione corrispondente, ma inoltra immediatamente la richiesta di creazione del socket al provider del servizio di trasporto associato alla struttura \_ **WSAPROTOCOL \_ INFO** indicata. I valori per la tupla (*address family,* *socket type,*) vengono forniti intatti al provider di servizi nella [**funzione WSPSocket.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) I provider di servizi possono ignorare o prestare attenzione ai valori dei parametri ( famiglia di *indirizzi,* tipo *di socket,*) come appropriato, ma non devono indicare una condizione di errore quando il valore della famiglia di indirizzi o del tipo *di socket* è zero.  Inoltre, i provider di servizi non devono indicare una condizione di errore quando la costante del manifesto FROM PROTOCOL INFO è contenuta in uno dei parametri ( famiglia di indirizzi, tipo \_ \_ di *socket,*). Questo valore indica semplicemente che l'applicazione vuole usare i valori trovati nei parametri corrispondenti della struttura **WSAPROTOCOL \_ INFO:** (**iAddressFamily**, **iSocketType**, **iProtocol**).

Come parte della creazione del socket, un provider di servizi informa il32.dll Ws2 sull'associazione tra se stesso e il nuovo socket tramite parametri passati a \_ [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) o [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle). L'32.dll Ws2 tiene traccia di questa associazione tra handle \_ di socket e provider di servizi specifici. Ogni volta che viene chiamata una funzione dell'interfaccia dell'applicazione che fa riferimento a un handle socket, il32.dll Ws2 cerca l'associazione e chiama la funzione di interfaccia del provider di servizi corrispondente del provider di \_ servizi appropriato.

Oltre al principale servizio di routing del traffico, il32.dll Ws2 fornisce una serie di altri servizi, ad esempio l'enumerazione del protocollo, Gestione dei descrittori socket (allocazione, deallocazione e associazione di valori di contesto) per i provider di servizi non di sistema, blocco della gestione hook per thread, utilità di scambio di byte, accodamento di chiamate di procedura asincrone (API) per facilitare la chiamata di routine di completamento I/O e negoziazione della versione tra le applicazioni e il32.dll Ws2, nonché tra il \_32.dll Ws2 e i provider di \_ \_ servizi.

## <a name="transport-service-provider-functionality"></a>Funzionalità del provider di servizi di trasporto

I provider di servizi implementano il protocollo di trasporto effettivo che include funzioni come la configurazione delle connessioni, il trasferimento dei dati, l'esercizio del controllo di flusso e del controllo degli errori e così via. L'32.dll Ws2 non ha alcuna conoscenza del modo in cui vengono realizzate le richieste ai provider di servizi. Questa operazione è in base \_ all'implementazione del provider di servizi. L'implementazione di tali funzioni può differire notevolmente da un provider a un altro. I provider di servizi nascondono i dettagli specifici dell'implementazione del modo in cui vengono eseguite le operazioni di rete.

I provider di servizi di trasporto possono essere suddivisi in due categorie: quelli i cui descrittori di socket sono handle file system reali (e sono successivamente definiti provider del file system installabile). Il resto viene definito provider non IFS. Il32.dll Ws2 passa sempre il descrittore socket del provider del servizio di trasporto \_ all'applicazione Windows Sockets, quindi le applicazioni sono libere di sfruttare i descrittori socket che file system handle, se lo desiderano.

Per riepilogare: i provider di servizi implementano i protocolli specifici della rete di basso livello. Ws232.dll la gestione del traffico di livello medio che collega questi protocolli \_ di trasporto con le applicazioni. Le applicazioni forniscono a loro volta i criteri per l'uso di questi flussi di traffico e delle operazioni specifiche della rete per eseguire le funzioni desiderate dall'utente.

 

 
