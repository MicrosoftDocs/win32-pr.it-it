---
description: 'Windows Sockets 2 incorpora il concetto di protocollo a più livelli: uno che implementa solo funzioni di comunicazione di livello superiore mentre si basa su uno stack di trasporto sottostante per lo scambio effettivo di dati con un endpoint remoto.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Protocolli sovrapposti e catene di protocolli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf74a11dffca9d8c49c61af82132857f5510e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129163"
---
# <a name="layered-protocols-and-protocol-chains"></a>Protocolli sovrapposti e catene di protocolli

Windows Sockets 2 incorpora il concetto di protocollo a più livelli: uno che implementa solo funzioni di comunicazione di livello superiore mentre si basa su uno stack di trasporto sottostante per lo scambio effettivo di dati con un endpoint remoto. Un esempio di questo tipo di protocollo a più livelli è un livello di sicurezza che aggiunge un protocollo al processo di connessione socket per poter eseguire l'autenticazione e stabilire uno schema di crittografia. Un protocollo di sicurezza di questo tipo richiede in genere i servizi di un protocollo di trasporto sottostante e affidabile, ad esempio TCP o SPX.

Il termine *protocollo di base* fa riferimento a un protocollo, ad esempio TCP o SPX, che è completamente in grado di eseguire le comunicazioni dati con un endpoint remoto. Un *protocollo* a più livelli è un protocollo che non può essere autonomo, mentre una *catena* di protocolli è uno o più protocolli sovrapposti e ancorato da un protocollo di base.

È possibile creare una catena di protocolli se si progettano i protocolli a più livelli per supportare Windows Sockets 2 SPI a entrambi i bordi superiore e inferiore. Una struttura [**di \_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) speciale si riferisce alla catena di protocolli nel suo complesso e descrive l'ordine esplicito in cui vengono aggiunti i protocolli a più livelli. Questa procedura è illustrata nella figura seguente. Poiché solo i protocolli di base e le catene di protocollo sono utilizzabili direttamente dalle applicazioni, sono elencate solo quando i protocolli installati vengono enumerati con la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .

![architettura del protocollo a più livelli](images/ovrvw2-3.png)

 

 
