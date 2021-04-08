---
title: Connessioni di callback
description: RAS supporta le connessioni in cui il server remoto si blocca e quindi richiama il client per stabilire la connessione.
ms.assetid: 25f0e84d-8900-4efe-b07d-59f25186c976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aabe3bf5503f16d7d27e44e02dc19ccb2a6f2e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729823"
---
# <a name="callback-connections"></a>Connessioni di callback

RAS supporta le connessioni in cui il server remoto si blocca e quindi richiama il client per stabilire la connessione.

Per ogni utente che può connettersi a un server RAS, il server archivia un attributo di callback che controlla il modo in cui viene eseguita la connessione. L'attributo predefinito non è un callback, il che significa che l'utente può connettersi al server RAS senza un callback. In alternativa, l'amministratore del server RAS può assegnare a un utente l'attributo di callback set-by-Caller.

Per un utente che ha assegnato la restrizione predefinita, l'amministratore specifica un numero di telefono che deve essere richiamato dal server RAS per stabilire una connessione. L'utente non può specificare un numero diverso e la connessione non può essere eseguita senza un callback.

Un'operazione di callback del set di impostazioni viene gestita automaticamente dalla gestione connessione di accesso remoto e dal server remoto. L'applicazione client RAS non deve eseguire alcuna operazione oltre a fornire commenti e suggerimenti all'utente quando il gestore delle notifiche viene chiamato durante i vari Stati dell'operazione di callback.

Un utente assegnato il privilegio set by Caller può scegliere di connettersi con o senza un callback. La chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) usa il membro **SzCallbackNumber** della struttura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) per indicare la scelta.

Il membro **szCallbackNumber** può semplicemente specificare il numero di callback. in alternativa, per stabilire la connessione senza callback, **szCallbackNumber** può puntare a una stringa vuota "". In entrambi i casi, la gestione connessione di accesso remoto gestisce automaticamente l'operazione di connessione. Come per un'operazione di callback del set di impostazioni, il client RAS non deve eseguire alcuna azione diversa da per fornire commenti e suggerimenti all'utente.

Se la chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) Abilita [gli stati sospesi](paused-states.md), **szCallbackNumber** può puntare a una stringa asterisco, " \* ", per indicare che l'operazione di connessione deve entrare in uno stato di sospensione per consentire all'utente di digitare il numero di callback. In questo caso, l'operazione di connessione per un oggetto impostato dall'utente chiamante entra in uno stato di sospensione dopo che il server remoto ha autenticato l'utente. Durante lo stato sospeso, il client RAS Ottiene l'input del numero di callback dall'utente. Il client riprende quindi l'operazione di connessione effettuando una seconda chiamata a **RasDial** in cui **szCallbackNumber** specifica il numero fornito dall'utente.

> [!Note]  
> Se gli stati sospesi non sono abilitati, esiste un significato diverso quando **szCallbackNumber** punta a una stringa asterisco " \* ". In questo caso, l'asterisco indica che il numero di callback viene archiviato nel file della rubrica telefonica specificato dalla chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .

 

In caso di callback, la chiamata a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) non restituisce alcun risultato finché il server non ha richiamato il client.

 

 