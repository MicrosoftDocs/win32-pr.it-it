---
title: Disconnessione in corso
description: Quando un'applicazione client RAS avvia un'operazione di connessione, la chiamata RasDial riceve un handle di connessione HRASCONN per identificare la connessione.
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fde205dfeb838639447c9f9359ee5b1258b2426eb55dbdd592291aea002fad6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101861"
---
# <a name="disconnecting"></a>Disconnessione in corso

Quando un'applicazione client RAS avvia un'operazione di connessione, la chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) riceve un handle di connessione **HRASCONN** per identificare la connessione. Se l'handle restituito **non è NULL,** il client deve infine chiamare la [**funzione RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) per terminare la connessione. Se si verifica un errore durante l'operazione di connessione, il client deve chiamare **RasHangUp** anche se la connessione non è mai stata stabilita.

L'applicazione che [**chiama RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) non deve uscire immediatamente perché il Gestione connessioni accesso remoto necessita di tempo per terminare correttamente la connessione. L'applicazione deve invece attendere che la funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) restituisca ERROR INVALID HANDLE, a indicare \_ che la connessione è stata \_ eliminata.

Un'applicazione client RAS potrebbe dover terminare una connessione anche se non dispone dell'handle restituito da [**RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala) Ad esempio, l'applicazione che ha chiamato **RasDial** potrebbe essere stata chiusa dopo che la connessione è stata stabilita correttamente. In questo caso, l'applicazione che si disconnette può usare [**la funzione RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) per ottenere tutte le connessioni correnti. Per ogni connessione, **RasEnumConnections** restituisce una struttura [**RASCONN**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) che contiene l'handle di connessione **HRASCONN** e il nome della voce della rubrica o il numero di telefono specificato al momento dell'avvio dell'operazione di connessione. Queste informazioni possono essere utilizzate per visualizzare un elenco di connessioni da cui l'utente può selezionare la connessione da terminare.

 

 