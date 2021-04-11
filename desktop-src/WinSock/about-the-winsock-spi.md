---
description: Winsock fornisce un'interfaccia del provider di servizi per la creazione di servizi Winsock, comunemente noti come Winsock SPI.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: Informazioni su Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129231"
---
# <a name="about-the-winsock-spi"></a>Informazioni su Winsock SPI

Winsock fornisce un'interfaccia del provider di servizi per la creazione di servizi Winsock, comunemente noti come Winsock SPI. Esistono due tipi di provider di servizi: provider di trasporto e provider dello spazio dei nomi. Esempi di provider di trasporto includono gli stack di protocolli, ad esempio TCP/IP o IPX/SPX, mentre un esempio di provider dello spazio dei nomi è un'interfaccia per il DNS (Domain Naming System) di Internet. Le sezioni separate della specifica dell'interfaccia del provider di servizi si applicano a ogni tipo di provider di servizi.

I provider di servizi di [trasporto](transport-service-providers-2.md) e [spazio dei nomi](name-space-service-providers-2.md) devono essere registrati con WS2 \_32.dll al momento dell'installazione. Questa registrazione deve essere eseguita una sola volta per ogni provider, in quanto le informazioni necessarie vengono conservate nell'archivio permanente.

 

 



