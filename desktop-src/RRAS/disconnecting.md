---
title: Disconnessione in corso
description: Quando un'applicazione client RAS avvia un'operazione di connessione, la chiamata RasDial riceve un handle di connessione HRASCONN per identificare la connessione.
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859a3751bcbaf7d95927cdf6d14de859ddcc731e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047281"
---
# <a name="disconnecting"></a>Disconnessione in corso

Quando un'applicazione client RAS avvia un'operazione di connessione, la chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) riceve un handle di connessione **HRASCONN** per identificare la connessione. Se l'handle restituito non è **null**, il client deve chiamare la funzione [**RasHangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) per terminare la connessione. Se si verifica un errore durante l'operazione di connessione, il client deve chiamare **RasHangup** anche se la connessione non è mai stata stabilita.

L'applicazione che chiama [**RasHangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) non deve uscire immediatamente perché la gestione connessione di accesso remoto richiede tempo per terminare correttamente la connessione. Al contrario, l'applicazione deve attendere fino a quando la funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) restituisce l'errore \_ handle non valido \_ , che indica che la connessione è stata eliminata.

Un'applicazione client RAS potrebbe dover terminare una connessione anche se non ha l'handle restituito da [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala). Ad esempio, l'applicazione che ha chiamato **RasDial** potrebbe essere stata chiusa dopo che la connessione è stata stabilita correttamente. In questo caso, l'applicazione di disconnessione può utilizzare la funzione [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) per ottenere tutte le connessioni correnti. Per ogni connessione, **RasEnumConnections** restituisce una struttura [**RASCONN**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) che contiene l'handle di connessione **HRASCONN** e il nome della voce o il numero di telefono del libro telefonico specificato quando è stata avviata l'operazione di connessione. Queste informazioni possono essere utilizzate per visualizzare un elenco di connessioni da cui l'utente può selezionare la connessione da terminare.

 

 