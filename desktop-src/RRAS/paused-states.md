---
title: Stati sospesi
description: Durante un'operazione di connessione, è possibile che il server remoto non possa procedere senza informazioni aggiuntive dell'utente locale.
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec66a63adbee524ec231b5c9dd9b0b410c8f4fbc73746ae9b924294c680b4a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029141"
---
# <a name="paused-states"></a>Stati sospesi

Durante un'operazione di connessione, è possibile che il server remoto non possa procedere senza informazioni aggiuntive dell'utente locale. A partire da Windows NT 3.5, la [**funzione RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) supporta gli stati sospesi. Uno stato sospeso consente al Gestione connessioni di accesso remoto di sospendere un'operazione di connessione in modo che l'applicazione client RAS possa raccogliere informazioni dall'utente.

Gli stati sospesi sono utili nelle situazioni seguenti:

-   Quando l'utente deve fornire un numero [di callback.](callback-connections.md)
-   Quando l'autenticazione utente ha esito negativo, l'utente può digitare un nome utente e una password diversi.
-   Quando la password dell'utente è scaduta, l'utente può specificare una nuova password.

Per impostazione predefinita, il supporto dello stato sospeso è disabilitato. I client RAS che vogliono supportare gli stati sospesi devono impostare il flag RDEOPTS \_ PausedStates nella [**struttura RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) passata come parametro su [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Quando si verifica uno stato sospeso, l'Gestione connessioni di accesso remoto richiama il gestore di notifica del client. Se il supporto dello stato sospeso è disabilitato, il messaggio di notifica indica un errore e l'operazione di connessione non riesce. Se è abilitato, il Gestione connessioni sospende l'operazione di connessione per attendere la risposta del client RAS. Il client RAS può riprendere l'operazione di connessione tramite una seconda chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) o terminarla chiamando la [**funzione RasHangUp.**](/windows/desktop/api/Ras/nf-ras-rashangupa)

Dopo aver ottenere l'input dell'utente, il client RAS riavvia l'operazione di connessione chiamando [**di nuovo RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala) Questa seconda **chiamata RasDial** deve specificare le informazioni seguenti:

-   Handle di connessione restituito dalla chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) originale.
-   Lo stesso gestore di notifica della chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) originale.
-   Input dell'utente nei membri appropriati della [**struttura RASDIALPARAMS.**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) Gli altri membri **della struttura RASDIALPARAMS** devono avere le stesse informazioni specificate nella chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) originale.

La seconda [**chiamata RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) non può essere effettuata dall'interno del gestore di notifica.

 

 