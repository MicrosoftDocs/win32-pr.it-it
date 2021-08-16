---
title: Completamento e annullamento di un processo
description: Per completare un processo di trasferimento, chiamare il metodo IBackgroundCopyJob Complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- trasferimento del processo BITS, annullamento
- annullamento di un bit del processo
- trasferimento del processo BITS, completamento
- completamento di un processo BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 348ee7c4ad4b9a38350e6a1f25d8d05d206b299518cf25197b643dbcb15cb4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835056"
---
# <a name="completing-and-canceling-a-job"></a>Completamento e annullamento di un processo

Per completare un processo di trasferimento, chiamare il [**metodo IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Per i processi di download, è possibile chiamare il **metodo Complete** prima che tutti i file nel processo siano stati trasferiti (prima che lo stato del processo sia BG JOB \_ STATE \_ \_ TRANSFERRED). Solo i file che BITS ha trasferito correttamente al client prima di chiamare il **metodo Complete** sono disponibili per l'utente.

Per i processi di caricamento, chiamare [**il metodo Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) solo se lo stato del processo è BG JOB STATE \_ \_ \_ TRANSFERRED. Per determinare quando lo stato del processo è BG JOB STATE TRANSFERRED, eseguire il polling della proprietà state del processo o registrarsi per ricevere la notifica \_ \_ \_ dell'evento BG NOTIFY JOB [](polling-for-the-status-of-the-job.md) \_ \_ \_ TRANSFERRED. [](registering-a-com-callback.md)

Per annullare un processo di trasferimento, chiamare il [**metodo IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) Il **metodo Cancel** rimuove il processo dalla coda di trasferimento e rimuove i file temporanei dal client. In genere, questo metodo viene chiamato se non è possibile risolvere un errore associato al processo.

Il [**metodo Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) annulla un caricamento se il caricamento non è completo. Se il caricamento è completo e il processo è di tipo BG JOB TYPE UPLOAD REPLY, il \_ metodo annulla la \_ \_ \_ risposta.

Se non si chiama il metodo [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o il metodo [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) entro 90 giorni (valore [predefinito JobInactivityTimeout](group-policies.md) Criteri di gruppo), il servizio annulla il processo. Se il servizio annulla il processo, i file scaricati e il file di risposta non sono disponibili per il client. L'annullamento del processo non influisce sui file caricati correttamente. È sempre necessario chiamare il **metodo Complete** o **Cancel** e non basarsi sui criteri JobInactivityTimeout per la pulizia dei processi. I processi rimasti nella coda possono impedire agli utenti di creare altri processi se viene raggiunto il limite di criteri MaxJobsPerUser o MaxJobsPerMachine.

 

 




