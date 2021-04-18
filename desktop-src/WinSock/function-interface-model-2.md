---
description: Il trasporto e lo spazio dei nomi Windows Sockets&\# 8211; i provider di servizi sono dll con un singolo punto di ingresso della routine esportato per la funzione di inizializzazione del provider di servizi WSPStartup o NSPStartup.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Modello di interfaccia di funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306976"
---
# <a name="function-interface-model"></a>Modello di interfaccia di funzione

Trasporto e spazio dei nomi Windows Sockets: i provider di servizi sono dll con un singolo punto di ingresso della procedura esportato per la funzione di inizializzazione del provider di servizi [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) o [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup). Tutte le altre funzioni del provider di servizi vengono rese accessibili a WS2 \_32.dll tramite la tabella dispatch del provider di servizi. Le DLL del provider di servizi vengono caricate in memoria da WS2 \_32.dll solo quando sono necessarie e vengono scaricate quando i servizi non sono più necessari.

SPI definisce inoltre diverse circostanze in cui un provider di servizi di trasporto chiama il32.dll WS2 \_ (chiamate) per ottenere i servizi di supporto dll. Alla DLL del provider del servizio di trasporto viene assegnata la tabella WS2 del \_32.dll di invio tramite il parametro *UpcallTable* a [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).

I provider di servizi devono avere l'estensione del nome file modificata da "DLL" a ". WSP "or". NSP ". Questo requisito non è rigoroso. Un provider di servizi continuerà a funzionare con il \_32.dll WS2 con qualsiasi estensione di file.

Winsock SPI usa la convenzione di denominazione dei prefissi di funzione seguente:

| Prefisso | Significato                          | Descrizione                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Provider di servizi Windows Sockets | Punti di ingresso del provider di servizi di trasporto           |
| WPU    | Chiamata del provider Windows Sockets  | WS2 \_32.dll punti di ingresso per i provider di servizi    |
| WSC    | Configurazione di Windows Sockets    | \_Punti di ingresso di WS232.dll per le applet di installazione |
| NSP    | Provider dello spazio dei nomi               | Punti di ingresso del provider dello spazio dei nomi                   |



 

Come descritto in precedenza, questi punti di ingresso non vengono esportati (ad eccezione di [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) e [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), ma è possibile accedervi tramite uno scambio di tabelle di invio.

 

 



