---
description: Windows Installer versione 2,0 avvia la ricerca di un'origine controllando il percorso di origine usato più di recente nell'elenco origine, quindi l'elenco delle origini di rete, le origini dei supporti e le origini URL infine.
ms.assetid: 21b1a31e-efe3-4d45-b1c5-fe6ed9b19fed
title: Criteri di resilienza dell'origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605c420198234405c23cb9672ca25c621b76390e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967903"
---
# <a name="source-resiliency-policy"></a>Criteri di resilienza dell'origine

Il programma di installazione inizia la ricerca di un'origine controllando il percorso di origine usato più di recente nell'elenco di origine, quindi l'elenco delle origini di rete, le origini multimediali e le origini URL infine. Per altre informazioni, vedere [resilienza dell'origine](source-resiliency.md). Se la ricerca ha esito negativo, il programma di installazione può presentare una [finestra di dialogo di esplorazione](browse-dialog.md) che consente all'utente di cercare l'origine manualmente. Impossibile visualizzare la finestra di dialogo Sfoglia se i [livelli dell'interfaccia utente](user-interface-levels.md) sono impostati su nessuno. Un amministratore controlla la visualizzazione della finestra di dialogo Sfoglia per gli utenti impostando criteri di sistema.

Con Windows Installer, per impostazione predefinita non è possibile utilizzare la finestra di dialogo Sfoglia per individuare le origini delle applicazioni gestite nei supporti e non è possibile installare applicazioni gestite. Un amministratore consente a un amministratore non di esplorare o installare le applicazioni gestite dai supporti usando i criteri [AllowLockdownBrowse](allowlockdownbrowse.md) e [AllowLockdownMedia](allowlockdownmedia.md) . Un amministratore disabilita la funzionalità di esplorazione o installazione delle applicazioni dai supporti usando i criteri [DisAbleBrowse](disablebrowse.md) e [DisAbleMedia](disablemedia.md) .

La tabella seguente riepiloga l'uso di questi criteri di sistema in Windows Installer.



| Criteri di sistema                                  | Applicazione non gestita utente non amministratore                                                                                                             | Applicazione gestita dall'utente non amministratore                                                                                                                 | Applicazione non gestita dell'applicazione gestita dall'amministratore                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AllowLockdownBrowse](allowlockdownbrowse.md) | Gli utenti possono installare applicazioni non gestite usando le origini presenti nei supporti. Gli utenti possono esplorare i supporti per le origini di applicazioni non gestite.<br/>    | Gli utenti non possono installare applicazioni gestite usando le origini presenti nei supporti. Gli utenti possono esplorare i supporti per le origini di applicazioni gestite.<br/>      | Gli amministratori possono installare le applicazioni utilizzando le origini presenti nei supporti. Gli amministratori possono sfogliare i file multimediali per le origini delle applicazioni.<br/>    |
| [AllowLockdownMedia](allowlockdownmedia.md)   | Gli utenti possono installare applicazioni non gestite usando le origini presenti nei supporti. Gli utenti possono esplorare i supporti per le origini di applicazioni non gestite.<br/>    | Gli utenti possono installare le applicazioni gestite usando le origini presenti nei supporti. Gli utenti non possono esplorare i supporti per le origini di applicazioni gestite.<br/>      | Gli amministratori possono installare le applicazioni utilizzando le origini presenti nei supporti. Gli amministratori possono sfogliare i file multimediali per le origini delle applicazioni.<br/>    |
| *Default*                                      | Gli utenti possono installare applicazioni non gestite usando le origini presenti nei supporti. Gli utenti possono esplorare i supporti per le origini di applicazioni non gestite.<br/>    | Gli utenti non possono installare applicazioni gestite usando le origini presenti nei supporti. Gli utenti non possono esplorare i supporti per le origini di applicazioni gestite.<br/>   | Gli amministratori possono installare le applicazioni utilizzando le origini presenti nei supporti. Gli amministratori possono sfogliare i file multimediali per le origini delle applicazioni.<br/>    |
| [DisAbleBrowse](disablebrowse.md)             | Gli utenti possono installare applicazioni non gestite usando le origini presenti nei supporti. Gli utenti non possono esplorare i supporti per le origini di applicazioni non gestite.<br/> | Gli utenti non possono installare applicazioni gestite usando le origini presenti nei supporti. Gli utenti non possono esplorare i supporti per le origini di applicazioni gestite. .<br/> | Gli amministratori possono installare le applicazioni utilizzando le origini presenti nei supporti. Gli amministratori non possono esplorare i supporti per le origini delle applicazioni.<br/> |
| [DisAbleMedia](disablemedia.md)               | Gli utenti non possono installare applicazioni non gestite usando le origini presenti nei supporti. Gli utenti possono esplorare i supporti per le origini di applicazioni non gestite.<br/> | Gli utenti non possono installare applicazioni gestite usando le origini presenti nei supporti. Gli utenti non possono esplorare i supporti per le origini di applicazioni gestite.<br/>   | Gli amministratori non possono installare le applicazioni utilizzando le origini presenti nei supporti. Gli amministratori possono sfogliare i file multimediali per le origini delle applicazioni.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 




