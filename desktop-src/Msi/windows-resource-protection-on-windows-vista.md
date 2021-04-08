---
description: Windows Installer rispetta Protezione risorse di Windows (WRP) quando si installano i file di sistema essenziali, le cartelle e le informazioni del registro di sistema in Windows Server 2008 e versioni successive e Windows Vista e versioni successive.
ms.assetid: 38865ee1-22ef-430b-99ce-1c6983c3b51f
title: Utilizzo di Windows Installer e Protezione risorse di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72808184ff11b29bfeb02dda576e9393e34189fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967730"
---
# <a name="using-windows-installer-and-windows-resource-protection"></a>Utilizzo di Windows Installer e Protezione risorse di Windows

Windows Installer rispetta Protezione risorse di Windows (WRP) quando si installano i file di sistema essenziali, le cartelle e le informazioni del registro di sistema in Windows Server 2008 e versioni successive e Windows Vista e versioni successive.

WRP in Windows Server 2008 e Windows Vista sostituisce protezione file Windows (WFP) in Windows Server 2003, Windows XP e Windows 2000. Windows Installer gli sviluppatori devono tenere presenti le seguenti modifiche nel modo in cui il programma di installazione gestisce le risorse protette in Windows Server 2008 e versioni successive e Windows Vista e versioni successive:

-   Quando è in esecuzione in Windows Server 2008 e versioni successive o Windows Vista e versioni successive, il Windows Installer ignora l'installazione di tutti i file protetti da WRP, il programma di installazione immette un avviso nel file di log e continua con il resto dell'installazione senza errori. In Windows Server 2003, Windows XP e Windows 2000, quando il Windows Installer ha rilevato un file protetto da WFP, il programma di installazione richiederà l'installazione del file da parte di Pam.
-   WRP in Windows Server 2008 e versioni successive o Windows Vista e versioni successive possono proteggere le chiavi del registro di sistema oltre ai file. Se il Windows Installer rileva una chiave del registro di sistema protetta da WRP, il programma di installazione ignora l'installazione della chiave del registro di sistema, il programma di installazione immette un avviso nel file di log e continua con il resto dell'installazione senza errori.
-   Si noti che se un componente Windows Installer contiene una chiave del registro di sistema o un file protetto da WRP, è necessario usare questa risorsa come percorso di chiave per il componente. In questo caso, Windows Installer non installa, aggiorna o rimuove il componente. Non includere risorse protette in un pacchetto di installazione. È invece consigliabile usare i [meccanismi di sostituzione delle risorse supportati](../wfp/supported-file-replacement-mechanisms.md) per [Protezione risorse di Windows](../wfp/windows-resource-protection-portal.md).

Per ulteriori informazioni su WRP, vedere [Protezione risorse di Windows](../wfp/windows-resource-protection-portal.md) e informazioni fornite in [Microsoft TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)).

## <a name="wfp-for-windows-server-2003-and-windows-xp2000"></a>WFP per Windows Server 2003 e Windows XP/2000

Windows Installer rispetta la protezione dei file di Windows (WFP) quando si installano i file di sistema essenziali in Windows Server 2003, Windows XP e Windows 2000. Se un file di sistema protetto viene modificato da un'installazione automatica di un'applicazione, Pam ripristina il file nella versione verificata.

Windows Installer non tenta mai di installare o sostituire un file protetto. Quando l'azione [InstallFiles](installfiles-action.md) o qualsiasi altra azione pianificata prima di InstallFiles tenta di installare un file protetto in windows Server 2003, Windows XP o Windows 2000, il programma di installazione chiama WFP con una richiesta di installazione o sostituzione del file protetto. Il programma di installazione richiede l'installazione del file da WFP immediatamente dopo l'esecuzione dell'azione InstallFiles. Pam installa o sostituisce il file nel sistema dell'utente con una versione memorizzata nella cache del file protetto. Si noti che questo non garantisce che la versione del file installata dalla cache sia la versione richiesta dall'applicazione. Dopo l'installazione del file da parte di WFP, il programma di installazione determina se questa versione corrisponde alla versione nel pacchetto. Se la versione del file nel pacchetto è superiore alla versione installata, il programma di installazione informa l'utente che non è possibile aggiornare il sistema e che potrebbe essere necessario un aggiornamento del sistema operativo per l'applicazione.

Se una qualsiasi azione sequenziata dopo [InstallFiles](installfiles-action.md) tenta di installare o sostituire un file protetto non è già installato nel sistema, il programma di installazione non è in grado di chiamare WFP per installare il file. In questo caso, il programma di installazione informa l'utente che non è possibile aggiornare il sistema e che potrebbe essere necessario un aggiornamento del sistema operativo per l'applicazione.

Il programma di installazione controlla anche con WFP quando si rimuovono i file e non tenta mai di rimuovere i file di sistema protetti.

## <a name="component-key-files-protected-by-wfp"></a>File di chiave del componente protetti da WFP

Si noti che se un componente Windows Installer contiene un file WFP, questo file deve essere specificato come percorso della chiave per il componente.

Quando il programma di installazione tenta di installare il file di chiave di un componente in Windows Server 2003, Windows XP o Windows 2000, chiama prima WFP per determinare se il file di chiave è protetto. Quando il file di chiave di un componente è protetto da WFP e tale file di chiave è già installato, il programma di installazione aggiorna il componente solo se la versione del file di chiave nel pacchetto è superiore alla versione installata. Se il pacchetto di installazione specifica che è installato un componente e il file di chiave del componente non è attualmente installato, a prescindere dal fatto che il file di chiave sia protetto, il programma di installazione installa il componente. Quando viene installato un componente con un file di chiave protetto da WFP, questo viene installato in modo permanente e il programma di installazione non rimuove o sostituisce mai il componente.

## <a name="installation-of-assemblies-by-wfp"></a>Installazione degli assembly tramite WFP

Il WFP per gli assembly è diverso da WFP per i file di sistema.

Pam protegge i file di sistema di Windows Server 2003, Windows XP e Windows 2000 rilevando i tentativi di sostituzione dei file di sistema protetti. Questa protezione viene attivata dopo che PAM riceve una notifica di modifica della directory per un file in una directory protetta. Quando PAM riceve questa notifica, determina quale file è stato modificato. Se il file è protetto, PAM cerca la firma del file in un file di catalogo statico per determinare se il nuovo file è la versione corretta. Se la versione del file non è corretta, il sistema sostituisce il file con la versione corretta dalla cache o dal supporto di distribuzione.

Il PAM degli assembly, invece, è dinamico. Il WFP viene esteso ai file man mano che vengono aggiunti all'Assembly Cache affiancata condivisa. Se un assembly viene danneggiato, Pam chiederà di sostituire il file con il programma di installazione. Windows Installer possibile o non essere in grado di sostituire il file a seconda che il pacchetto di origine sia accessibile o meno. Se il pacchetto di origine non è accessibile, Pam inserisce una finestra di dialogo che informa che non è in grado di ripristinare il file.

Si noti che gli assembly side-by-side condivisi non gestiti, installati in% windir% \\ WinSxS, sono protetti da WFP. Gli assembly privati non gestiti, installati nella directory dell'applicazione, non sono protetti da WFP. Gli assembly globali gestiti installati nella directory dell'applicazione o nella GAC di% windir% \\ assembly \\ non sono protetti da WFP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protezione risorse di Windows](../wfp/windows-resource-protection-portal.md)
</dt> </dl>

 

 
