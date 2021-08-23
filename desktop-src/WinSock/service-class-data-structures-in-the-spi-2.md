---
description: Quando viene installata una nuova classe di servizio, è necessario preparare e fornire una struttura WSASERVICECLASSINFO. Questa struttura è anche costituita da sottostrutture che contengono una serie di parametri che si applicano a spazi dei nomi specifici.
ms.assetid: fb225e0c-a0c7-44e1-80fb-7b924b371afa
title: Strutture di dati della classe di servizio nell'spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53eb2fd61c5ec6295b65128048bc9fe477ae63f78f89bfba4be73798002ead88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993567"
---
# <a name="service-class-data-structures-in-the-spi"></a>Strutture di dati della classe di servizio nell'spi

Quando viene installata una nuova classe di servizio, è necessario preparare e fornire una struttura [**WSASERVICECLASSINFO.**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) Questa struttura è anche costituita da sottostrutture che contengono una serie di parametri che si applicano a spazi dei nomi specifici.

![Diagramma che mostra la struttura, le sottostrutture e i parametri WSASERVICECLASSINFO applicabili a spazi dei nomi specifici.](images/ovrvw3-3.png)

Per ogni classe di servizio è presente una singola [**struttura WSASERVICECLASSINFO.**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) All'interno della struttura **WSASERVICECLASSINFO,** l'identificatore univoco della classe di servizio è contenuto in **lpServiceClassId** e una stringa di visualizzazione associata fa riferimento **a lpServiceClassName**.

Il membro **lpClassInfos** nella struttura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) fa riferimento a una matrice di strutture [**WSANSCLASSINFO,**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) ognuna delle quali fornisce un parametro denominato e tipiato che si applica a uno spazio dei nomi specificato. Esempi di valori per **il membro lpszName** includono: SAPID, TCPPORT, UDPPORT e così via. Queste stringhe sono in genere specifiche dello spazio dei nomi identificato in **dwNameSpace**. I valori tipici **per dwValueType** possono essere REG \_ DWORD, REG \_ SZ e così via. Il **membro dwValueSize** indica la lunghezza dell'elemento di dati a cui punta **lpValue**.

L'intera raccolta di dati rappresentati in [**una struttura WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) viene fornita a ogni provider dello spazio dei nomi [**tramite NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass). Ogni singolo provider dello spazio dei nomi passa quindi al set di dati l'elenco delle [**strutture WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) e mantiene le informazioni applicabili. Questa architettura prevede anche la futura esistenza di un provider dello spazio dei nomi speciale che manterrà tutte le informazioni sullo schema della classe di servizio per tutti gli spazi dei nomi. Il32.dll Ws2 esegue una query su questo provider per ottenere i dati WSASERVICECLASSINFO necessari per fornire ai provider dello spazio dei nomi quando viene richiamato \_ [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) per avviare una query e quando viene richiamato  [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice) per registrare un servizio. Il provider dello spazio dei nomi non deve basarsi su questa funzionalità per il momento e deve disporre di un mezzo specifico del provider per ottenere le informazioni necessarie sullo schema della classe di servizio. In assenza di un provider che archivia tutti gli schemi della classe del servizio per tutti gli spazi dei nomi, il32.dll Ws2 userà \_ [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) per ottenere tali informazioni da ogni singolo provider dello spazio dei nomi.

 

 



