---
title: Stati sospesi
description: Durante un'operazione di connessione, a volte il server remoto non può continuare senza informazioni aggiuntive dall'utente locale.
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914acb85ccf74c92b4bd4119966a421faddeb011
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339055"
---
# <a name="paused-states"></a>Stati sospesi

Durante un'operazione di connessione, a volte il server remoto non può continuare senza informazioni aggiuntive dall'utente locale. A partire da Windows NT 3,5, la funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) supporta gli stati sospesi. Uno stato sospeso consente alla gestione connessione di accesso remoto di sospendere un'operazione di connessione in modo che l'applicazione client RAS possa raccogliere informazioni dall'utente.

Gli stati sospesi sono utili nelle situazioni seguenti:

-   Quando l'utente deve fornire un numero di [callback](callback-connections.md) .
-   Quando l'autenticazione utente non riesce, l'utente può digitare un nome utente e una password diversi.
-   Quando la password dell'utente è scaduta, l'utente può specificare una nuova password.

Per impostazione predefinita, il supporto dello stato sospeso è disabilitato. I client RAS che vogliono supportare gli stati sospesi devono impostare il \_ flag RDEOPTS PausedStates nella struttura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) passata come parametro a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Quando si verifica uno stato di sospensione, la gestione connessione di accesso remoto richiama il gestore di notifiche del client. Se il supporto dello stato sospeso è disabilitato, il messaggio di notifica indica un errore e l'operazione di connessione non riesce. Se è abilitata, la gestione connessione sospende l'operazione di connessione per attendere la risposta del client RAS. Il client RAS può riprendere l'operazione di connessione mediante una seconda chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) o terminarla chiamando la funzione [**RasHangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) .

Dopo aver ricevuto l'input dell'utente, il client RAS riavvia l'operazione di connessione chiamando di nuovo [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Questa seconda chiamata **RasDial** deve specificare le informazioni seguenti:

-   Handle di connessione restituito dalla chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) originale.
-   Lo stesso gestore di notifiche della chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) originale.
-   Input dell'utente nei membri appropriati della struttura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) . Gli altri membri della struttura **RASDIALPARAMS** devono avere le stesse informazioni specificate nella chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) originale.

Non è possibile effettuare la seconda chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) dall'interno del gestore di notifiche.

 

 