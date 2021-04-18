---
description: Quando viene installata una nuova classe di servizio, è necessario preparare e fornire una struttura WSASERVICECLASSINFO. Questa struttura è costituita anche da sottostrutture che contengono una serie di parametri che si applicano a spazi dei nomi specifici.
ms.assetid: fb225e0c-a0c7-44e1-80fb-7b924b371afa
title: Strutture di dati della classe di servizio in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bf249c7437751e7c6d08b2fdf3830e92921ce7
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104570658"
---
# <a name="service-class-data-structures-in-the-spi"></a>Strutture di dati della classe di servizio in SPI

Quando viene installata una nuova classe di servizio, è necessario preparare e fornire una struttura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . Questa struttura è costituita anche da sottostrutture che contengono una serie di parametri che si applicano a spazi dei nomi specifici.

![Diagramma che illustra la struttura, le sottostrutture e i parametri WSASERVICECLASSINFO che si applicano a spazi dei nomi specifici.](images/ovrvw3-3.png)

Per ogni classe di servizio è presente una sola struttura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . All'interno della struttura **WSASERVICECLASSINFO** , l'identificatore univoco della classe del servizio è contenuto in **lpServiceClassId** e a una stringa di visualizzazione associata viene fatto riferimento da **lpServiceClassName**.

Il membro **lpClassInfos** nella struttura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) fa riferimento a una matrice di strutture [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) , ciascuna delle quali fornisce un parametro denominato e tipizzato che si applica a uno spazio dei nomi specificato. Esempi di valori per il membro **lpszName** includono: SAPID, TCPPort, portaUDP e così via. Queste stringhe sono in genere specifiche dello spazio dei nomi identificato in **dwNameSpace**. I valori tipici per **dwValueType** potrebbero essere reg \_ DWORD, reg \_ SZ e così via. Il membro **dwValueSize** indica la lunghezza dell'elemento dati a cui punta **lpValue**.

L'intera raccolta di dati rappresentati in una struttura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) viene fornita a ogni provider dello spazio dei nomi tramite [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass). Ogni singolo provider dello spazio dei nomi quindi setaccia l'elenco di strutture [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) e mantiene le informazioni applicabili. Questa architettura prevede anche l'esistenza futura di un provider speciale per lo spazio dei nomi che conserva tutte le informazioni dello schema della classe di servizio per tutti gli spazi dei nomi. Il \_32.dll WS2 esegue una query su questo provider per ottenere i dati **WSASERVICECLASSINFO** necessari per fornire ai provider dello spazio dei nomi quando viene richiamato [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) per avviare una query e quando [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice) viene richiamato per registrare un servizio. Il provider dello spazio dei nomi non deve basarsi su questa funzionalità per il tempo e deve disporre di un metodo specifico del provider per ottenere le informazioni necessarie sullo schema della classe di servizio. In assenza di un provider che archivia tutti gli schemi della classe di servizio per tutti gli spazi dei nomi, il \_32.dll WS2 utilizzerà [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) per ottenere tali informazioni da ogni singolo provider dello spazio dei nomi.

 

 



