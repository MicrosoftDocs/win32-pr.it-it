---
title: Novità (IMAPi)
description: La tabella seguente identifica le novità per ogni versione dell'API per la creazione di immagini master.
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77abc9db0c9d976eef632034a5620520bb29d73d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723830"
---
# <a name="whats-new-image-mastering-api"></a>Novità: API per la creazione di immagini master

La tabella seguente identifica le novità per ogni versione dell'API per la creazione di immagini master.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Versione</th>
<th>Descrizione delle funzionalità</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Versione 2,0</td>
<td>Gran parte dell'API è stata riprogettata. La maggior parte delle funzionalità della versione 1,0 è ancora disponibile nella versione 2,0. Gli sviluppatori che scrivono applicazioni di Master immagini o eseguono nuove attività di sviluppo di dispositivi e formati sono invitati a usare la versione 2,0 anziché la versione 1,0.<br/> IMAPi 2,0 è incluso in Windows Vista. L'abilitazione della stessa funzionalità per Windows XP e Windows Server 2003 richiede l'installazione del pacchetto di aggiornamento <a href="https://support.microsoft.com/kb/932716">KB932716</a> .<br/> Note Point-Release:<br/>
<ul>
<li>Un aggiornamento che offre supporto per più avvii tramite l'interfaccia <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a> è stato introdotto in Windows Vista con Service Pack 1 (SP1) e windows Server 2008.<br/></li>
<li>Un aggiornamento delle funzionalità che offre supporto per la creazione di master per il formato BD-R\BD-RE, la creazione di un'immagine CD-at-once non ELABORAta e la verifica di masterizzazione sono stati inclusi nel <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Feature Pack di Windows per l'archiviazione</a>. Questo aggiornamento delle funzionalità è supportato in Windows Vista con SP1, Windows XP con Service Pack 2 (SP2) e versioni successive e Windows Server 2003 con Service Pack 1 (SP1) e versioni successive. Inoltre, queste funzionalità sono incluse in Windows 7 e Windows Server 2008.<br/></li>
<li>Le funzionalità IMAPi 2,0 native di Windows 7 e Windows Server 2008 includono ' gapless Burning ' per CD audio e l'eliminazione di ' Double stashing ' durante le operazioni di masterizzazione. Il doppio accantonamento è un processo, all'interno dell'operazione di masterizzazione più grande, in cui ogni file viene accantonato prima di essere bruciato su disco. Con la versione più recente di IMAPi 2,0, i file vengono scelti selettivamente per l'accantonamento, lasciando i file rimanenti (per lo più file di grandi dimensioni) non accantonati. Il risultato finale è lo spazio su disco e il tempo di operazione salvati.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Versione 1,0</td>
<td>Versione iniziale. Consente a una fase di applicazione di masterizzare un'immagine semplice o audio nei dispositivi CD-R e CD-RW. L'API supporta il formato Joliet e ISO 9660 per i dischi dati e audio di Redbook. Per informazioni sulla versione 1,0, vedere <a href="imapiv1.md">supporto di IMAPIv1</a>. Incluso in Windows XP.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="version-20"></a>Versione 2,0

-   Consente alle applicazioni di eseguire il Burn sui formati DVD-R, DVD + R, DVD-RW, DVD + RW, DVD + DL, DVD-DL e DVD-RAM, BD-R e BD-RE.
-   Consente la registrazione di più unità nello stesso momento. Nella versione 1,0 solo un registratore del sistema può essere usato da IMAPi alla volta. Se si esegue una versione 1,0 dell'applicazione in Windows Vista, altre applicazioni possono utilizzare contemporaneamente le interfacce IMAPi 1,0 o 2,0 su altre unità del sistema. Sebbene questo sia in genere considerato un vantaggio, le applicazioni che si basavano sul comportamento del singolo bruciatore del sistema possono richiedere aggiornamenti secondari.
-   L'accesso a un registratore viene negato quando il registratore scrive le informazioni sul disco. In caso contrario, il registratore sarà disponibile per gli altri client.
-   Supporta più di un file stash in un computer client, mentre la versione 1,0 consentiva solo un file stash a livello di sistema.
-   In Windows Vista, la versione 1,0 non contiene più componenti in modalità kernel o di servizio. Tuttavia, l'interfaccia [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) usa ancora i \_ \_ \_ comandi di accesso esclusivo IOCTL cdrom e IOCTL \_ SCSI \_ pass \_ through \_ Direct per gestire l'accesso o la comunicazione a dispositivi di unità specifici.
-   In Windows Vista, le interfacce della versione 1,0 ora chiamano le interfacce della versione 2,0.
-   Incluso in Windows Vista con SP1 e Windows Server 2008, IMAPi vesion 2,0 offre supporto per il multiboot tramite l'interfaccia [**IFileSystemImage2**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2) .
-   Consente l'uso di ' gapless Burning ' per CD audio. Con la masterizzazione gapless, è possibile rimuovere il gap udibile tra le tracce audio.
-   Sostituito ' doppio stashing ' con un processo che seleziona in modo specifico i file per l'accantonamento e lascia i file rimanenti (per lo più file di grandi dimensioni) non accantonati. Il risultato finale è lo spazio su disco e il tempo di operazione salvati.
-   Con il [Feature Pack di Windows per l'archiviazione](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05), le opzioni di verifica dell'ustione sono rese disponibili con una proprietà a cui si accede tramite [**IBurnVerification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification).
