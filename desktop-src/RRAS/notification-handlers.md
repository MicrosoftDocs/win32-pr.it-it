---
title: Gestori di notifiche
description: Una chiamata RasDial asincrona deve specificare un gestore di notifiche.
ms.assetid: 6d23d6ac-08ad-4fe2-a4af-021e4d384079
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe735a17de4386bc48648cd20decd218ab102d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955784"
---
# <a name="notification-handlers"></a>Gestori di notifiche

Una chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asincrona deve specificare un gestore di notifiche. Durante un'operazione di connessione asincrona, la gestione connessione di accesso remoto utilizza il gestore delle notifiche per informare il client RAS ogni volta che lo [stato della connessione](connection-states.md) cambia o si verifica un errore.

Le azioni eseguite da un gestore di notifiche possono essere divise nelle categorie seguenti:

-   [Gestione degli errori](handling-ras-errors.md),
-   Invio di commenti e suggerimenti all'utente durante l'esecuzione dell'operazione di connessione nei vari Stati di connessione. Vedere [notifiche informative](informational-notifications.md).
-   Gestione [degli stati sospesi](paused-states.md).
-   Segnalazione dell'applicazione client RAS al completamento dell'operazione di connessione. Vedere [notifiche di completamento](completion-notifications.md).

Sono disponibili tre tipi di gestori di notifiche, ognuno dei quali riceve le stesse informazioni di base: lo stato di connessione corrente e un codice di errore diverso da zero solo se si è verificato un errore.



| valore                                | Definizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)   | Prototipo di funzione di callback che riceve solo lo stato di connessione corrente e le informazioni sul codice di errore.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) | Prototipo di funzione di callback che riceve l'handle di connessione **HRASCONN** e le informazioni estese sull'errore oltre alle informazioni di base. Il parametro dell'handle di connessione rende [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) utile per le applicazioni client che supportano più operazioni di connessione simultanee. Ciò consente al client di specificare la stessa funzione di callback per tutte le operazioni e consente alla funzione di callback di determinare quale connessione sta cambiando gli Stati. |
| [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) | Funzione di callback simile a [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1). Tuttavia, [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) è stato migliorato per supportare le connessioni a più collegamenti.                                                                                                                                                                                                                                                                                                                             |
| Handle finestra                        | Handle di finestra a cui RAS Invia messaggi [**WM \_ RASDIALEVENT**](wm-rasdialevent.md) contenenti lo stato di connessione corrente e le informazioni sul codice di errore. Utilizzare questo metodo se il codice sorgente deve essere compatibile con Windows a 16 bit, perché Windows a 16 bit non supporta nessuna delle funzioni di callback.                                                                                                                                                                            |



 

La gestione connessione di accesso remoto sospende l'operazione di connessione fino alla restituzione del gestore di notifiche. Per questo motivo, il gestore deve restituire il prima possibile a meno che non si sia verificato un errore.

La funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) non deve essere chiamata dall'interno di un gestore di notifiche. Le altre funzioni di accesso remoto ( [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa), [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa), [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa), [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)e [**RasHangup**](/windows/desktop/api/Ras/nf-ras-rashangupa)) possono essere chiamate dall'interno di un gestore.

 

 




