---
title: Novità (IMAPI)
description: La tabella seguente identifica le novità per ogni versione dell'API Image Mastering.
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a3b0ceb966f3f6db6583b86b616608da3bee4f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472177"
---
# <a name="whats-new-image-mastering-api"></a>Novità: API Image Mastering

La tabella seguente identifica le novità per ogni versione dell'API Image Mastering.




| Versione | Descrizione delle funzionalità | 
|---------|-------------------------|
| Versione 2.0 | Gran parte dell'API è stata riprogettata. La maggior parte delle funzionalità della versione 1.0 è ancora disponibile nella versione 2.0. Gli utenti che scrivono applicazioni di gestione delle immagini o eseguono lo sviluppo di nuovi dispositivi e formati sono invitati a usare la versione 2.0 anziché la versione 1.0.<br /> IMAPI 2.0 è incluso in Windows Vista. L'abilitazione della stessa funzionalità Windows XP e Windows Server 2003 richiede l'installazione del pacchetto di aggiornamento <a href="https://support.microsoft.com/kb/932716">KB932716.</a><br /> Point-Release note:<br /><ul><li>Un aggiornamento che offre supporto ad avvio multiplo tramite l'interfaccia <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a> è stato introdotto in Windows Vista con Service Pack 1 (SP1) e Windows Server 2008.<br /></li><li>Un aggiornamento delle funzionalità che offre supporto per la masterizzazione del formato BD-R\BD-RE, la creazione di immagini RAW CD Disc-at-Once e la verifica della masterizzazione sono stati inclusi nel Feature Pack di <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Windows per Archiviazione</a>. Questo aggiornamento delle funzionalità è supportato in Windows Vista con SP1, Windows XP con Service Pack 2 (SP2) e versioni successive e Windows Server 2003 con Service Pack 1 (SP1) e versioni successive. Inoltre, queste funzionalità sono incluse in Windows 7 e Windows Server 2008.<br /></li><li>Le funzionalità DI IMAPI 2.0 native di Windows 7 e Windows Server 2008 includono "Gapless Disaccoppiato" per cd audio e l'eliminazione di "Double Stashing" durante le operazioni di masterizzazione. Il doppio stashing è un processo, all'interno dell'operazione di masterizzazione più grande, in cui ogni file viene sfalsato prima di essere rilasciato su disco. Con la versione più recente di IMAPI 2.0, i file vengono selezionati in modo selettivo per lo stashing, lasciando i file rimanenti (per lo più file di grandi dimensioni) non disaccoccodati. Il risultato finale è lo spazio su disco salvato e il tempo dell'operazione.<br /></li></ul> | 
| Versione 1.0 | Versione iniziale. Consente a un'applicazione di eseguire lo stage e masterizzare una semplice immagine audio o dati in dispositivi CD-R e CD-RW. L'API supporta il formato Joliet e ISO 9660 per i dischi audio e di dati Redbook. Per informazioni sulla versione 1.0, vedere <a href="imapiv1.md">Supporto IMAPIv1.</a> Incluso in Windows XP.<br /> | 




 

## <a name="version-20"></a>Versione 2.0

-   Consente alle applicazioni di masterizzare nei formati dvd-R, DVD+R, DVD-RW, DVD+RW, DVD+DL, DVD-DL e DVD-RAM, BD-R e BD-RE.
-   Consente la registrazione su più unità contemporaneamente. Nella versione 1.0, un solo registratore del sistema può essere usato da IMAPI alla volta. Se si esegue un'applicazione versione 1.0 in Windows Vista, altre applicazioni possono usare simultaneamente interfacce IMAPI 1.0 o 2.0 in altre unità del sistema. Sebbene questo sia in genere considerato un vantaggio, le applicazioni che si basano sul comportamento del singolo masterizzatore di sistema possono richiedere aggiornamenti secondari.
-   L'accesso a un registratore viene negato quando scrive informazioni sul disco. In caso contrario, il registratore è disponibile per altri client.
-   Supporta più di un file stash in un computer client, mentre la versione 1.0 consentiva un solo file stash a livello di sistema.
-   In Windows Vista la versione 1.0 non contiene più componenti del servizio o della modalità kernel. Tuttavia, [**l'interfaccia IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) usa ancora i comandi IOCTL CDROM EXCLUSIVE ACCESS e \_ \_ \_ IOCTL \_ SCSI PASS THROUGH \_ \_ DIRECT per gestire l'accesso o la comunicazione con dispositivi \_ unità specifici.
-   In Windows Vista le interfacce della versione 1.0 ora chiamano le interfacce della versione 2.0.
-   Incluso in Windows Vista con SP1 e Windows Server 2008, IMAPI versione 2.0 offre supporto multiboot tramite [**l'interfaccia IFileSystemImage2.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2)
-   Consente l'uso di "Gapless Disaccodato" per i CD audio. Con Gapless Disaccocco, è possibile rimuovere il divario udibile tra le tracce audio.
-   Sostituito "Double Stashing" con un processo che seleziona in modo specifico i file per lo stashing e lascia i file rimanenti (per lo più file di grandi dimensioni) non-stashed. Il risultato finale è lo spazio su disco salvato e il tempo dell'operazione.
-   Con il [Feature Pack Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)per Archiviazione , le opzioni di verifica della masterizzazione sono state rese disponibili con una proprietà a cui si accede tramite I [**VerificationVerification.**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification)
