---
description: Inserire l'azione ScheduleReboot nella sequenza di azioni per richiedere all'utente un riavvio del sistema al termine dell'installazione. Usare l'azione ForceReboot per richiedere un riavvio durante l'installazione.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Azione ScheduleReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e796338c04f47ff4b2907dcf8d1531d438622a2f28a653e8ac4672a8b445e1b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041521"
---
# <a name="schedulereboot-action"></a>Azione ScheduleReboot

Inserire l'azione ScheduleReboot nella sequenza di azioni per richiedere all'utente un riavvio del sistema al termine dell'installazione. Usare [l'azione ForceReboot](forcereboot-action.md) per richiedere un riavvio durante l'installazione.

Se l'installazione ha un'interfaccia utente, il programma di installazione visualizza una finestra di messaggio e un pulsante al termine dell'installazione per chiedere se l'utente vuole riavviare il sistema. L'utente deve rispondere a questo prompt prima di completare l'installazione. Se l'installazione non ha un'interfaccia utente, il sistema viene riavviato automaticamente alla fine.

Se il programma di installazione determina che è necessario un riavvio, richiede automaticamente all'utente di riavviare al termine dell'installazione, indipendentemente dal fatto che nella sequenza siano presenti azioni ForceReboot o ScheduleReboot. Ad esempio, il programma di installazione richiede automaticamente un riavvio se deve sostituire i file in uso durante l'installazione.

È possibile eliminare determinate richieste di riavvio impostando la [**proprietà REBOOT.**](reboot.md)

Se il Windows installer rileva l'azione [ForceReboot](forcereboot-action.md) o ScheduleReboot durante un'installazione con più [pacchetti,](multiple-package-installations.md)il programma di installazione verrà interrotta ed eseguito il rollback dell'installazione. È possibile installare altri pacchetti che appartengono all'installazione a più pacchetti, che non contengono un'azione ForceReboot o ScheduleReboot.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

Non sono presenti restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

Ad esempio, questa azione può essere usata per forzare il programma di installazione a richiedere un riavvio dopo l'installazione dei driver che richiedono un riavvio. Se il programma di installazione tenta di sostituire i file in uso, richiede automaticamente all'utente di riavviare anche se ScheduleReboot non è stato usato.

L'azione ScheduleReboot viene in genere posizionata alla fine della sequenza, ma può essere inserita in qualsiasi punto della sequenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riavvii del sistema](system-reboots.md)
</dt> </dl>

 

 



