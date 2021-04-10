---
description: Le applicazioni che si basano sulle risorse di rete per l'installazione su richiesta sono soggette a errori di origine se la posizione di origine deve essere modificata per qualsiasi motivo o danneggiata.
ms.assetid: 3d6a0524-d5df-4d4c-b861-d4a7da95ce40
title: Resilienza di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46944804db1c4b91c6c6757303fd2af90638b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966488"
---
# <a name="source-resiliency"></a>Resilienza di origine

Le applicazioni che si basano sulle risorse di rete per l' [installazione su richiesta](installation-on-demand.md) sono soggette a errori di origine se la posizione di origine deve essere modificata per qualsiasi motivo o danneggiata. Il Windows Installer fornisce la resilienza dell'origine per le funzionalità installate su richiesta tramite un elenco di origine. L'elenco di origine contiene i percorsi cercati dal programma di installazione per i pacchetti di installazione. Le voci di questo elenco possono essere percorsi di rete, URL (Uniform Resource Locator) o Compact Disks. Se una di queste origini ha esito negativo, il programma di installazione può provare a eseguire rapidamente e facilmente il passaggio successivo.

Lo sviluppatore di applicazioni non deve incorporare informazioni speciali nel pacchetto del programma di installazione per garantire la resilienza dell'origine. Una volta installata l'applicazione, il programma di installazione ha il comportamento di aggiungere l'ultima origine correttamente utilizzata come voce nell'elenco di origine. Per impostazione predefinita, questa origine è la posizione da cui viene inizialmente installato il pacchetto di installazione ed è uguale alla proprietà [**SourceDir**](sourcedir.md) .

Un amministratore di sistema può modificare l'elenco di origine applicando una [trasformazione](merges-and-transforms.md) o modificando la proprietà dell'elenco di [**origine**](sourcelist.md) dalla riga di comando o nella [tabella delle proprietà](property-table.md).

Il programma di installazione inizia la ricerca di un'origine controllando il percorso di origine usato più di recente nell'elenco di origine. Se la ricerca ha esito negativo, il programma di installazione cerca nell'elenco le origini di rete, quindi le origini supporti e infine le origini URL. Gli amministratori di sistema possono modificare questo ordine di ricerca usando i criteri di sistema [SearchOrder](searchorder.md) . Se queste ricerche hanno esito negativo, il programma di installazione può presentare una [finestra di dialogo di esplorazione](browse-dialog.md) in modo che l'utente possa cercare l'origine manualmente. Impossibile visualizzare la finestra di dialogo Sfoglia se il livello dell'interfaccia utente è impostato su nessuno. Per informazioni dettagliate, vedere [livelli di interfaccia utente](user-interface-levels.md).

In genere, il programma di installazione deve visualizzare solo una finestra di dialogo Sfoglia se l'utente corrente è un amministratore o se l'installazione non richiede privilegi elevati. Un amministratore può controllare la visualizzazione della finestra di dialogo Sfoglia per gli utenti con i criteri [DisableBrowse](disablebrowse.md) e [AllowLockDownBrowse](allowlockdownbrowse.md) . Un amministratore controlla anche se gli utenti possono installare le applicazioni da origini presenti nei supporti usando i criteri [DisableMedia](disablemedia.md) e [AllowLockDownMedia](allowlockdownmedia.md) . L'uso di questi criteri dipende dalla versione Windows Installer. Per informazioni dettagliate, vedere gli argomenti seguenti:

-   [Criteri di resilienza dell'origine](source-resiliency-policy-windows-installer-version-2-0.md)

 

 



