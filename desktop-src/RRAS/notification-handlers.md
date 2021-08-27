---
title: Gestori di notifica
description: Una chiamata RasDial asincrona deve specificare un gestore di notifica.
ms.assetid: 6d23d6ac-08ad-4fe2-a4af-021e4d384079
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7210072e0542eeb63e3de6116d61995ef2363ca7b43e7a9e2c309165c0e862
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074031"
---
# <a name="notification-handlers"></a>Gestori di notifica

Una chiamata [**RasDial asincrona**](/windows/desktop/api/Ras/nf-ras-rasdiala) deve specificare un gestore di notifica. Durante un'operazione di connessione asincrona, il Gestione connessioni accesso remoto usa [](connection-states.md) il gestore di notifica per informare il client RAS ogni volta che lo stato della connessione cambia o si verifica un errore.

Le azioni eseguite da un gestore di notifica possono essere suddivise nelle categorie seguenti:

-   [Gestione degli errori](handling-ras-errors.md),
-   Fornire commenti e suggerimenti all'utente mentre l'operazione di connessione procede attraverso i vari stati di connessione. Vedere [Notifiche in tempo reale.](informational-notifications.md)
-   Gestione degli [stati sospesi](paused-states.md).
-   Segnalazione all'applicazione client RAS al termine dell'operazione di connessione. Vedere [Notifiche di completamento.](completion-notifications.md)

Esistono tre tipi di gestori di notifica, ognuno dei quali riceve le stesse informazioni di base: lo stato della connessione corrente e un codice di errore diverso da zero solo se si è verificato un errore.



| valore                                | Definizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)   | Prototipo di funzione di callback che riceve solo lo stato di connessione corrente e le informazioni sul codice di errore.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) | Prototipo di funzione di callback che riceve l'handle di connessione **HRASCONN** e le informazioni estese sull'errore, oltre alle informazioni di base. Il parametro dell'handle di connessione [**rende RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) utile per le applicazioni client che supportano più operazioni di connessione simultanee. In questo modo il client può specificare la stessa funzione di callback per tutte le operazioni e consente alla funzione di callback di determinare quale connessione sta cambiando gli stati. |
| [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) | Funzione di callback simile a [**RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) Tuttavia, [**RasDialFunc2 è**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) stato migliorato per supportare le connessioni multilink.                                                                                                                                                                                                                                                                                                                             |
| Handle di finestra                        | Handle di finestra a cui RAS invia messaggi [**WM \_ RASDIALEVENT**](wm-rasdialevent.md) contenenti lo stato di connessione corrente e le informazioni sul codice di errore. Usare questo metodo se il codice sorgente deve essere compatibile con il Windows a 16 bit, perché il Windows a 16 bit non supporta nessuna delle funzioni di callback.                                                                                                                                                                            |



 

Il gestore di accesso Gestione connessioni sospende l'operazione di connessione fino alla fine del gestore di notifica. Per questo motivo, il gestore deve restituire il prima possibile, a meno che non si sia verificato un errore.

La [**funzione RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) non deve essere chiamata dall'interno di un gestore di notifica. Le altre funzioni di accesso remoto ( [**RasGetConnectStatus,**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) [**RasEnumEntries,**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) [**RasEnumConnections,**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)e [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)) possono essere chiamate dall'interno di un gestore.

 

 




