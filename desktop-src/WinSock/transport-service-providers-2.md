---
description: Provider di servizi di trasporto e Windows Sockets (Winsock).
ms.assetid: 4ded519d-d9c2-4ef3-80f5-e6ec40adf938
title: Provider di servizi di trasporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114eefa67bbb2d7afdf46b74f1a9524e7a77b7c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306891"
---
# <a name="transport-service-providers"></a>Provider di servizi di trasporto

Un provider di servizi di trasporto specificato supporta uno o più protocolli. Un provider TCP/IP, ad esempio, fornirebbe come minimo i protocolli TCP e UDP, mentre un provider IPX/SPX potrebbe fornire IPX, SPX e SPX II. Ogni protocollo supportato da un determinato provider è descritto da una struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) e il set totale di tali strutture può essere considerato come il catalogo dei protocolli installati. Le applicazioni possono recuperare il contenuto di questo catalogo (per altre informazioni, vedere [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)) ed esaminando le strutture di **\_ informazioni WSAPROTOCOL** disponibili, individuare gli attributi di comunicazione associati a ogni protocollo.

## <a name="layered-protocols-and-protocol-chains-in-the-spi"></a>Protocolli sovrapposti e catene di protocolli in SPI

Windows Sockets 2 supporta il concetto di protocollo a più livelli. Un protocollo a più livelli è uno che implementa solo funzioni di comunicazione di livello superiore, mentre si basa su uno stack di trasporto sottostante per lo scambio effettivo di dati con un endpoint remoto. Un esempio di protocollo di questo tipo è un livello di sicurezza che aggiunge il protocollo al processo di creazione della connessione per poter eseguire l'autenticazione e stabilire uno schema di crittografia concordato a vicenda. Un protocollo di sicurezza di questo tipo richiede in genere i servizi di un protocollo di trasporto affidabile sottostante, ad esempio TCP o SPX. Il termine protocollo di base si riferisce a un protocollo come TCP o SPX che è completamente in grado di eseguire le comunicazioni dati con un endpoint remoto e il termine protocollo a più livelli viene usato per descrivere un protocollo che non può essere autonomo. Una catena di protocolli verrebbe quindi definita come uno o più protocolli sovrapposti e ancorato da un protocollo di base.

Questa stringa di protocolli a più livelli e protocolli di base in catene può essere eseguita con la disposizione per i protocolli a più livelli per supportare l'SPI di Winsock sia nei bordi superiore che in quello inferiore. Viene creata una speciale struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) che fa riferimento alla catena di protocolli nel suo complesso e descrive l'ordine esplicito in cui vengono aggiunti i protocolli a più livelli. Questa operazione è illustrata nell'immagine seguente.

![catena di protocolli](images/ovrvw2-3.png)

 

 
