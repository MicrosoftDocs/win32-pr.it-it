---
description: Provider di servizi di trasporto Windows socket (Winsock).
ms.assetid: 4ded519d-d9c2-4ef3-80f5-e6ec40adf938
title: Provider di servizi di trasporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d860db59b5a27d19cdc5263069161f105d79e15cfd7353789f8fdcf9944799ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927177"
---
# <a name="transport-service-providers"></a>Provider di servizi di trasporto

Un provider del servizio di trasporto specificato supporta uno o più protocolli. Ad esempio, un provider TCP/IP fornisce, come minimo, i protocolli TCP e UDP, mentre un provider IPX/SPX potrebbe fornire IPX, SPX e SPX II. Ogni protocollo supportato da un provider specifico è descritto da una struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) e il set totale di tali strutture può essere pensato come catalogo dei protocolli installati. Le applicazioni possono recuperare il contenuto di questo catalogo (per altre informazioni, vedere [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)e [**WSCEnumProtocols32)**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)e, esaminando le strutture **WSAPROTOCOL \_ INFO** disponibili, individuare gli attributi di comunicazione associati a ogni protocollo.

## <a name="layered-protocols-and-protocol-chains-in-the-spi"></a>Protocolli su più livelli e catene di protocolli in SPI

Windows I socket 2 supportano il concetto di protocollo a più livelli. Un protocollo a più livelli implementa solo funzioni di comunicazione di livello superiore, basandosi allo stesso tempo su uno stack di trasporto sottostante per lo scambio effettivo di dati con un endpoint remoto. Un esempio di questo protocollo a più livelli è un livello di sicurezza che aggiunge il protocollo al processo di creazione della connessione per eseguire l'autenticazione e stabilire uno schema di crittografia concordato a livello reciproco. Un protocollo di sicurezza di questo tipo richiede in genere i servizi di un protocollo di trasporto affidabile sottostante, ad esempio TCP o SPX. Il termine protocollo di base si riferisce a un protocollo, ad esempio TCP o SPX, che è in grado di eseguire comunicazioni dati con un endpoint remoto e il termine protocollo a più livelli viene usato per descrivere un protocollo che non può essere autonomo. Una catena di protocolli verrebbe quindi definita come uno o più protocolli a più livelli uniti e ancorati da un protocollo di base.

Questa disposizione dei protocolli a più livelli e dei protocolli di base in catene può essere eseguita disponendo i protocolli a più livelli per supportare l'interfaccia SPI di Winsock sia ai bordi superiore che inferiore. Viene creata una speciale [**struttura WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) che fa riferimento alla catena di protocolli nel suo complesso e descrive l'ordine esplicito in cui vengono uniti i protocolli a più livelli. Questa operazione è illustrata nell'immagine seguente.

![catena di protocolli](images/ovrvw2-3.png)

 

 
