---
description: Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore avviando un'attività pianificata.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modello di attività con privilegi elevati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa485c47983760cc260a97cb52b58316a0d87bd4083d3ed09e72032f8fc7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672321"
---
# <a name="elevated-task-model"></a>Modello di attività con privilegi elevati

Nel modello di attività con privilegi elevati un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore avviando un'attività pianificata.

**Windows Server 2003 e Windows XP:** Il modello di attività con privilegi elevati non è supportato.

Le attività non utilizzano tutte le risorse di sistema dei servizi e le attività si chiudono automaticamente al termine. Prendere in considerazione l'uso di questo modello anziché [del modello di servizio del sistema operativo,](operating-system-service-model.md) a meno che non sia necessaria la compatibilità con i sistemi operativi precedenti.

Per utilizzare un'attività per eseguire operazioni con privilegi per un'applicazione utente standard, è necessario che siano soddisfatte le condizioni seguenti:

-   L'attività deve essere impostata per l'esecuzione come **SYSTEM.**
-   Il [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) associato all'attività deve essere configurato per consentire agli utenti standard di avviare l'attività.
-   Il servizio Utilità di pianificazione deve essere in esecuzione.

Per informazioni su come creare e avviare attività, vedere [Utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni che richiedono privilegi di amministratore](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modello broker amministratore](administrator-broker-model.md)
</dt> <dt>

[Modello a oggetti COM administrator](administrator-com-object-model.md)
</dt> <dt>

[Modello di servizio del sistema operativo](operating-system-service-model.md)
</dt> </dl>

 

 
