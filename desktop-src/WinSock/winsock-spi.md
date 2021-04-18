---
description: Windows Sockets (Winsock) Service Provider Interface (SPI).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: SPI di Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313223"
---
# <a name="winsock-spi"></a>SPI di Winsock

L'interfaccia del provider di servizi Winsock, o Winsock SPI, è una disciplina specializzata di Winsock utilizzata per creare i provider. i provider di trasporto, ad esempio gli stack di protocolli TCP/IP o IPX/SPX, usano il protocollo SPI SPI, così come i provider di spazio dei nomi, ad esempio il DNS (Domain Naming System) di Internet.

La programmazione di rete tradizionale, ad esempio l'abilitazione delle applicazioni per la comunicazione in rete, non richiede l'uso di interfacce Winsock SPI; usare invece le interfacce standard [Winsock](winsock-reference.md) .

 

Winsock SPI usa la convenzione di denominazione dei prefissi di funzione seguente.



| Prefisso | Significato                          | Descrizione                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Provider di servizi Windows Sockets | Punti di ingresso del provider di servizi di trasporto           |
| WPU    | Chiamata del provider Windows Sockets  | WS2 \_32.dll punti di ingresso per i provider di servizi    |
| WSC    | Configurazione di Windows Sockets    | \_Punti di ingresso di WS232.dll per le applet di installazione |
| NSP    | Provider dello spazio dei nomi               | Punti di ingresso del provider dello spazio dei nomi                   |



 

 

 



