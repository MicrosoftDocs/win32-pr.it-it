---
description: Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore avviando un'attività pianificata.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modello di attività con privilegi elevati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348931"
---
# <a name="elevated-task-model"></a>Modello di attività con privilegi elevati

Nel modello di attività con privilegi elevati, un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore avviando un'attività pianificata.

**Windows Server 2003 e Windows XP:** Il modello di attività con privilegi elevati non è supportato.

Le attività non utilizzano il numero di risorse di sistema dei servizi e le attività si chiudono automaticamente al termine dell'operazione. È consigliabile utilizzare questo modello anziché il [modello di servizio del sistema operativo](operating-system-service-model.md) a meno che non sia necessaria la compatibilità con le versioni precedenti dei sistemi operativi precedenti.

Per utilizzare un'attività per eseguire operazioni con privilegi per un'applicazione utente standard, è necessario che siano soddisfatte le condizioni seguenti:

-   L'attività deve essere impostata per l'esecuzione come **System**.
-   Il [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) associato all'attività deve essere configurato in modo da consentire agli utenti standard di avviare l'attività.
-   Il servizio Utilità di pianificazione deve essere in esecuzione.

Per informazioni su come creare e avviare le attività, vedere [utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni che richiedono privilegi di amministratore](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modello di broker amministratore](administrator-broker-model.md)
</dt> <dt>

[Modello a oggetti COM dell'amministratore](administrator-com-object-model.md)
</dt> <dt>

[Modello di servizio del sistema operativo](operating-system-service-model.md)
</dt> </dl>

 

 
