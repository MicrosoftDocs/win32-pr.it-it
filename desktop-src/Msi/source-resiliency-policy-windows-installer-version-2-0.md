---
description: Windows La versione 2.0 del programma di installazione inizia a cercare un'origine controllando il percorso di origine usato più di recente nell'elenco di origine, quindi l'elenco di origini di rete, le origini multimediali e infine le origini URL.
ms.assetid: 21b1a31e-efe3-4d45-b1c5-fe6ed9b19fed
title: Criteri di resilienza dell'origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4951c1183da8998986863fe5dae744fc58c23387306c91153b50ab63e38e0a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039711"
---
# <a name="source-resiliency-policy"></a>Criteri di resilienza dell'origine

Il programma di installazione inizia a cercare un'origine controllando il percorso di origine usato più di recente nell'elenco di origine, quindi l'elenco delle origini di rete, quindi le origini multimediali e infine le origini URL. Per altre informazioni, vedere [Resilienza dell'origine.](source-resiliency.md) Se la ricerca non riesce, il programma di installazione potrebbe presentare [una finestra di dialogo sfoglia](browse-dialog.md) che consente all'utente di cercare manualmente l'origine. La finestra di dialogo Sfoglia non può essere visualizzata se i [livelli dell'interfaccia](user-interface-levels.md) utente sono impostati su Nessuno. Un amministratore controlla la visualizzazione della finestra di dialogo Sfoglia per gli utenti impostando i criteri di sistema.

Con Windows programma di installazione, gli utenti non amministratori per impostazione predefinita non possono usare la finestra di dialogo Sfoglia per individuare le origini dell'applicazione gestita nei supporti e non possono installare applicazioni gestite. Un amministratore consente a un utente non amministratore di esplorare o installare applicazioni gestite da supporti usando i criteri [AllowLockdownBrowse](allowlockdownbrowse.md) e [AllowLockdownMedia.](allowlockdownmedia.md) Un amministratore disabilita la funzionalità per esplorare o installare applicazioni dai supporti usando i criteri [DisAbleBrowse](disablebrowse.md) [e DisAbleMedia.](disablemedia.md)

Nella tabella seguente viene riepilogato l'uso di questi criteri di sistema Windows Programma di installazione.



| Criteri di sistema                                  | Applicazione non gestione dell'utente non amministratore                                                                                                             | Applicazione gestita dall'utente non amministratore                                                                                                                 | Applicazione gestita dall'amministratore Applicazione non gestita                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AllowLockdownBrowse](allowlockdownbrowse.md) | Gli utenti possono installare applicazioni non gestite usando origini che si trovano nei supporti. Gli utenti possono cercare i supporti per le origini delle applicazioni non gestite.<br/>    | Gli utenti non possono installare applicazioni gestite usando origini che si trovano nei supporti. Gli utenti possono cercare i supporti per le origini delle applicazioni gestite.<br/>      | Gli amministratori possono installare le applicazioni usando le origini presenti nei supporti. Gli amministratori possono esplorare i supporti per le origini delle applicazioni.<br/>    |
| [AllowLockdownMedia](allowlockdownmedia.md)   | Gli utenti possono installare applicazioni non gestite usando origini che si trovano nei supporti. Gli utenti possono cercare i supporti per le origini delle applicazioni non gestite.<br/>    | Gli utenti possono installare applicazioni gestite usando origini che si trovano nei supporti. Gli utenti non possono cercare i supporti per le origini delle applicazioni gestite.<br/>      | Gli amministratori possono installare le applicazioni usando le origini presenti nei supporti. Gli amministratori possono esplorare i supporti per le origini delle applicazioni.<br/>    |
| *Default*                                      | Gli utenti possono installare applicazioni non gestite usando origini che si trovano nei supporti. Gli utenti possono cercare i supporti per le origini delle applicazioni non gestite.<br/>    | Gli utenti non possono installare applicazioni gestite usando origini che si trovano nei supporti. Gli utenti non possono cercare i supporti per le origini delle applicazioni gestite.<br/>   | Gli amministratori possono installare le applicazioni usando le origini presenti nei supporti. Gli amministratori possono esplorare i supporti per le origini delle applicazioni.<br/>    |
| [DisAbleBrowse](disablebrowse.md)             | Gli utenti possono installare applicazioni non gestite usando origini che si trovano nei supporti. Gli utenti non possono cercare i supporti per le origini delle applicazioni non gestite.<br/> | Gli utenti non possono installare applicazioni gestite usando origini che si trovano nei supporti. Gli utenti non possono cercare i supporti per le origini delle applicazioni gestite. .<br/> | Gli amministratori possono installare le applicazioni usando le origini presenti nei supporti. Gli amministratori non possono cercare i supporti per le origini delle applicazioni.<br/> |
| [DisAbleMedia](disablemedia.md)               | Gli utenti non possono installare applicazioni non gestite usando origini che si trovano nei supporti. Gli utenti possono cercare i supporti per le origini delle applicazioni non gestite.<br/> | Gli utenti non possono installare applicazioni gestite usando origini che si trovano nei supporti. Gli utenti non possono cercare i supporti per le origini delle applicazioni gestite.<br/>   | Gli amministratori non possono installare le applicazioni usando origini presenti nei supporti. Gli amministratori possono esplorare i supporti per le origini delle applicazioni.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resilienza dell'origine](source-resiliency.md)
</dt> </dl>

 

 




