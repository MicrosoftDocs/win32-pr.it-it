---
description: 'Windows Sockets 2 incorpora il concetto di protocollo a più livelli: uno che implementa solo funzioni di comunicazione di livello superiore, basandosi su uno stack di trasporto sottostante per lo scambio effettivo di dati con un endpoint remoto.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Protocolli su più livelli e catene di protocolli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e60943bac5545fd7bb2bc87709d08c59d3addab205d14cab80687596721b973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858451"
---
# <a name="layered-protocols-and-protocol-chains"></a>Protocolli su più livelli e catene di protocolli

Windows Sockets 2 incorpora il concetto di protocollo a più livelli: uno che implementa solo funzioni di comunicazione di livello superiore, basandosi su uno stack di trasporto sottostante per lo scambio effettivo di dati con un endpoint remoto. Un esempio di questo tipo di protocollo a più livelli è un livello di sicurezza che aggiunge un protocollo al processo di connessione socket per eseguire l'autenticazione e stabilire uno schema di crittografia. Un protocollo di sicurezza di questo tipo richiede in genere i servizi di un protocollo di trasporto sottostante e affidabile, ad esempio TCP o SPX.

Il termine *protocollo di base* si riferisce a un protocollo, ad esempio TCP o SPX, in grado di eseguire comunicazioni dati con un endpoint remoto. Un *protocollo a più livelli* è un  protocollo che non può essere autonomo, mentre una catena di protocolli è uno o più protocolli a più livelli uniti e ancorati da un protocollo di base.

È possibile creare una catena di protocolli se si progettano protocolli a più livelli per supportare l'interfaccia SPI di Windows Sockets 2 ai bordi superiore e inferiore. Una speciale [**struttura WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) fa riferimento alla catena di protocolli nel suo complesso e descrive l'ordine esplicito in cui vengono uniti i protocolli su più livelli. Questa operazione è illustrata nella figura seguente. Poiché solo i protocolli di base e le catene di protocolli sono utilizzabili direttamente dalle applicazioni, sono gli unici elencati quando i protocolli installati vengono enumerati con la [**funzione WSAEnumProtocols.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)

![architettura del protocollo a più livelli](images/ovrvw2-3.png)

 

 
