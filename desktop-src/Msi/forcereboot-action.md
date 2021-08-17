---
description: L'azione ForceReboot richiede all'utente di riavviare il sistema durante l'installazione.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Azione ForceReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41af6b656222a31ab75c9df3f2fa9f94af415f94d6d0b50010c0b25c5742502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636072"
---
# <a name="forcereboot-action"></a>Azione ForceReboot

L'azione ForceReboot richiede all'utente di riavviare il sistema durante l'installazione. L'azione ForceReboot è diversa dall'azione [ScheduleReboot,](schedulereboot-action.md) in cui l'azione ScheduleReboot viene usata per pianificare un prompt per il riavvio al termine dell'installazione.

Se l'installazione ha un'interfaccia utente, il programma di installazione visualizza una finestra di dialogo a ogni azione ForceReboot che richiede all'utente di riavviare il sistema. L'utente deve rispondere a questo prompt prima di continuare con l'installazione. Se l'installazione non ha un'interfaccia utente, il sistema viene riavviato automaticamente all'azione ForceReboot.

Se il programma di installazione determina che è necessario un riavvio, chiede automaticamente all'utente di riavviare al termine dell'installazione, indipendentemente dal fatto che nella sequenza siano presenti azioni ForceReboot o ScheduleReboot. Ad esempio, il programma di installazione richiede automaticamente un riavvio se deve sostituire i file usati durante l'installazione.

Eliminare determinate richieste di riavvio impostando la [**proprietà REBOOT.**](reboot.md)

Se il Windows installer rileva l'azione ForceReboot o [ScheduleReboot](schedulereboot-action.md) durante un'installazione con più [pacchetti,](multiple-package-installations.md)il programma di installazione verrà interrotta ed eseguito il rollback dell'installazione. È possibile installare altri pacchetti che appartengono all'installazione a più pacchetti, che non contengono un'azione ForceReboot o ScheduleReboot.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

Le azioni seguenti si verificano comunemente insieme come gruppo nella sequenza di azioni. È consigliabile che l'azione ForceReboot venga pianificata dopo questo gruppo. Se l'azione ForceReboot è pianificata prima [dell'azione RegisterProduct](registerproduct-action.md), il programma di installazione richiede nuovamente l'origine del pacchetto di installazione dopo il riavvio. Pertanto, la sequenza preferita per ForceReboot segue immediatamente questa sequenza di azione.

-   [RegisterProduct](registerproduct-action.md)
-   [RegisterUser](registeruser-action.md)
-   [PublishProduct](publishproduct-action.md)
-   [PublishFeatures](publishfeatures-action.md)
-   [CreateShortcuts](createshortcuts-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)

L'azione ForceReboot deve essere compresa tra [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) nella sequenza di azione [della tabella InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

L'azione ForceReboot deve sempre essere usata con un'istruzione condizionale in modo che il programma di installazione attiva un riavvio solo quando necessario. Ad esempio, un riavvio può essere necessario solo se un file specifico viene sostituito o se viene installato un componente specifico. Ogni installazione del prodotto è univoca e potrebbe essere necessaria un'azione personalizzata per determinare se è necessario un riavvio. La condizione nell'azione ForceReboot usa in genere la [**proprietà AFTERREBOOT.**](afterreboot.md)

ForceReboot esegue le operazioni di sistema generate da qualsiasi azione precedente prima di richiedere un riavvio o un riavvio. Ad esempio, le operazioni di sistema generate [da InstallFiles](installfiles-action.md) e [WriteRegistryValues](writeregistryvalues-action.md) vengono eseguite prima di un riavvio.

L'azione ForceReboot scrive una chiave del Registro di sistema che determina l'avvio del programma di installazione dopo il riavvio. Il percorso di questa chiave è **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riavvii del sistema](system-reboots.md)
</dt> </dl>

 

 



