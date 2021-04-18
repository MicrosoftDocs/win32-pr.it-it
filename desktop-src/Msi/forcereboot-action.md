---
description: L'azione ForceReboot chiede all'utente di riavviare il sistema durante l'installazione.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Azione ForceReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314272"
---
# <a name="forcereboot-action"></a>Azione ForceReboot

L'azione ForceReboot chiede all'utente di riavviare il sistema durante l'installazione. L'azione ForceReboot è diversa dall' [azione ScheduleReboot](schedulereboot-action.md) in quanto l'azione ScheduleReboot viene utilizzata per pianificare una richiesta di riavvio al termine dell'installazione.

Se l'installazione ha un'interfaccia utente, il programma di installazione visualizza una finestra di dialogo in ogni azione ForceReboot che richiede all'utente di riavviare il sistema. Prima di continuare con l'installazione, l'utente deve rispondere a questa richiesta. Se l'installazione non ha un'interfaccia utente, il sistema viene riavviato automaticamente all'azione ForceReboot.

Se il programma di installazione determina che è necessario un riavvio, viene automaticamente richiesto all'utente di riavviare al termine dell'installazione, indipendentemente dal fatto che siano presenti azioni ForceReboot o ScheduleReboot nella sequenza. Ad esempio, il programma di installazione richiede automaticamente un riavvio se è necessario sostituire eventuali file utilizzati durante l'installazione.

Non visualizzare alcune richieste di riavvio impostando la proprietà [**reboot**](reboot.md) .

Se il Windows Installer rileva l'azione ForceReboot o [ScheduleReboot](schedulereboot-action.md) durante un'installazione con [più pacchetti](multiple-package-installations.md), il programma di installazione arresterà e eseguirà il rollback dell'installazione. È possibile installare altri pacchetti che appartengono all'installazione con più pacchetti, che non contengono un'azione ForceReboot o ScheduleReboot.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Le azioni seguenti si verificano comunemente insieme come un gruppo nella sequenza di azione. È consigliabile che l'azione ForceReboot venga pianificata per essere eseguita dopo questo gruppo. Se l'azione ForceReboot è stata pianificata prima dell' [azione RegisterProduct](registerproduct-action.md), il programma di installazione richiede nuovamente l'origine del pacchetto di installazione dopo il riavvio. La sequenza preferita per ForceReboot si trova quindi immediatamente dopo questa sequenza di azioni.

-   [RegisterProduct](registerproduct-action.md)
-   [RegisterUser](registeruser-action.md)
-   [PublishProduct](publishproduct-action.md)
-   [PublishFeatures](publishfeatures-action.md)
-   [CreateShortcuts](createshortcuts-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)

L'azione ForceReboot deve essere compresa tra [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) nella sequenza di azione della [tabella InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

L'azione ForceReboot deve sempre essere utilizzata con un'istruzione condizionale in modo che il programma di installazione avvii un riavvio solo quando necessario. Ad esempio, è possibile che sia necessario un riavvio solo se viene sostituito un particolare file o se è installato un particolare componente. Ogni installazione del prodotto è univoca ed è possibile che sia necessaria un'azione personalizzata per determinare se è necessario un riavvio. La condizione sull'azione ForceReboot USA in genere la proprietà [**AFTERREBOOT**](afterreboot.md) .

ForceReboot esegue le operazioni di sistema generate da qualsiasi azione precedente prima di richiedere un riavvio o un riavvio. Ad esempio, le operazioni di sistema generate da [InstallFiles](installfiles-action.md) e [WriteRegistryValori consente](writeregistryvalues-action.md) vengono eseguite prima di un riavvio.

L'azione ForceReboot scrive una chiave del registro di sistema che determina l'avvio del programma di installazione dopo il riavvio. Il percorso di questa chiave è **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riavvio del sistema](system-reboots.md)
</dt> </dl>

 

 



