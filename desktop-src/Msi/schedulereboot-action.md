---
description: Inserire l'azione ScheduleReboot nella sequenza di azione per richiedere all'utente il riavvio del sistema alla fine dell'installazione. Usare l'azione ForceReboot per richiedere un riavvio durante l'installazione.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Azione ScheduleReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881841"
---
# <a name="schedulereboot-action"></a>Azione ScheduleReboot

Inserire l'azione ScheduleReboot nella sequenza di azione per richiedere all'utente il riavvio del sistema alla fine dell'installazione. Usare l' [azione ForceReboot](forcereboot-action.md) per richiedere un riavvio durante l'installazione.

Se l'installazione ha un'interfaccia utente, il programma di installazione visualizza una finestra di messaggio e un pulsante alla fine dell'installazione che chiede se l'utente vuole riavviare il sistema. Prima di completare l'installazione, l'utente deve rispondere a questa richiesta. Se l'installazione non ha un'interfaccia utente, il sistema viene riavviato automaticamente alla fine.

Se il programma di installazione determina che è necessario un riavvio, viene automaticamente richiesto all'utente di riavviare al termine dell'installazione, indipendentemente dal fatto che siano presenti azioni ForceReboot o ScheduleReboot nella sequenza. Ad esempio, il programma di installazione richiede automaticamente un riavvio se è necessario sostituire i file in uso durante l'installazione.

È possibile disattivare determinate richieste di [**riavvio**](reboot.md) impostando la proprietà restart.

Se il Windows Installer rileva l'azione [ForceReboot](forcereboot-action.md) o ScheduleReboot durante un'installazione con [più pacchetti](multiple-package-installations.md), il programma di installazione arresterà e eseguirà il rollback dell'installazione. È possibile installare altri pacchetti che appartengono all'installazione con più pacchetti, che non contengono un'azione ForceReboot o ScheduleReboot.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Non esistono restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

Ad esempio, questa azione può essere usata per forzare il programma di installazione a richiedere un riavvio dopo l'installazione dei driver che richiedono un riavvio. Se il programma di installazione tenta di sostituire i file in uso, viene automaticamente richiesto di riavviare l'utente anche se ScheduleReboot non è stato usato.

L'azione ScheduleReboot viene in genere posizionata alla fine della sequenza, ma può essere inserita in qualsiasi punto della sequenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riavvio del sistema](system-reboots.md)
</dt> </dl>

 

 



