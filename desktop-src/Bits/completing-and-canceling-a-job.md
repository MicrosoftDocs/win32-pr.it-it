---
title: Completamento e annullamento di un processo
description: Per completare un processo di trasferimento, chiamare il metodo Metodo ibackgroundcopyjob complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- trasferimento BITS processo, annullamento
- annullamento di un bit di processo
- trasferimento BITS processo, completamento
- completamento di un bit di processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470979"
---
# <a name="completing-and-canceling-a-job"></a>Completamento e annullamento di un processo

Per completare un processo di trasferimento, chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Per i processi di download, è possibile chiamare il metodo **complete** prima che tutti i file del processo siano stati trasferiti (prima che lo stato del processo sia il \_ processo BG \_ stato \_ trasferito). Solo i file che sono stati trasferiti nel client prima di chiamare il metodo **complete** sono disponibili per l'utente.

Per i processi di caricamento, chiamare il metodo [**complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) solo se lo stato del processo è BG \_ processo \_ stato \_ trasferito. Per determinare quando lo stato del processo è BG \_ \_ , stato del processo \_ trasferito, eseguire il [polling](polling-for-the-status-of-the-job.md) della proprietà stato del processo o registrarsi per ricevere la \_ notifica degli \_ \_ [eventi](registering-a-com-callback.md)trasferiti al processo BG Notify.

Per annullare un processo di trasferimento, chiamare il metodo [**Metodo ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) . Il metodo **Cancel** rimuove il processo dalla coda di trasferimento e rimuove i file temporanei dal client. In genere, questo metodo viene chiamato se non si riesce a risolvere un errore associato al processo.

Il metodo [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) Annulla un caricamento se il caricamento non è completo. Se il caricamento è completo e il processo è di tipo BG \_ Reply di caricamento del tipo di processo \_ \_ \_ , il metodo annulla la risposta.

Se non si chiama il metodo [**complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o il metodo [**Metodo ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) entro 90 giorni (impostazione predefinita di [JobInactivityTimeout](group-policies.md) criteri di gruppo), il servizio annulla il processo. Se il servizio annulla il processo, i file scaricati e il file di risposta non sono disponibili per il client. l'annullamento del processo non influisce sui file che sono stati caricati correttamente. È sempre necessario chiamare il metodo **complete** o **Cancel** e non basarsi sul criterio JobInactivityTimeout per la pulizia dei processi. I processi rimasti nella coda possono impedire agli utenti di creare altri processi se viene raggiunto il limite dei criteri MaxJobsPerUser o MaxJobsPerMachine.

 

 




