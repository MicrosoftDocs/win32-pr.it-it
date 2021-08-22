---
description: Windows Il programma di installazione è conforme Windows Resource Protection (WRP) durante l'installazione di file di sistema, cartelle e informazioni del Registro di sistema essenziali in Windows Server 2008 e versioni successive e Windows Vista e versioni successive.
ms.assetid: 38865ee1-22ef-430b-99ce-1c6983c3b51f
title: Uso Windows programma di installazione e Windows resource protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ed70b502754dcc54c0954d21e6213d815ba0fa98927f5a67680700a4dd802
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012639"
---
# <a name="using-windows-installer-and-windows-resource-protection"></a>Uso Windows programma di installazione e Windows resource protection

Windows Il programma di installazione è conforme Windows Resource Protection (WRP) durante l'installazione di file di sistema, cartelle e informazioni del Registro di sistema essenziali in Windows Server 2008 e versioni successive e Windows Vista e versioni successive.

WRP in Windows Server 2008 e Windows Vista sostituisce Windows File Protection (WFP) in Windows Server 2003, Windows XP e Windows 2000. Windows Gli sviluppatori del programma di installazione devono prendere nota delle modifiche seguenti nel modo in cui il programma di installazione gestisce le risorse protette in Windows Server 2008 e versioni successive e Windows Vista e versioni successive:

-   Quando viene eseguito in Windows Server 2008 e versioni successive o Windows Vista e versioni successive, il programma di installazione di Windows ignora l'installazione di qualsiasi file protetto da WRP, il programma di installazione immette un avviso nel file di log e continua con il resto dell'installazione senza errori. In Windows Server 2003, Windows XP e Windows 2000, quando il programma di installazione di Windows ha rilevato un file protetto da WFP, il programma di installazione richiede l'installazione del file da parte del Programma di installazione di Windows.
-   WRP in Windows Server 2008 e versioni successive o versioni successive Windows Vista e versioni successive possono proteggere le chiavi del Registro di sistema oltre ai file. Se il programma di installazione di Windows rileva una chiave del Registro di sistema protetta da WRP, il programma di installazione ignora l'installazione di tale chiave del Registro di sistema, il programma di installazione immette un avviso nel file di log e continua con il resto dell'installazione senza errori.
-   Si noti che se un componente Windows Installer contiene un file o una chiave del Registro di sistema protetta da WRP, questa risorsa deve essere usata come KeyPath per il componente. In questo caso, Windows programma di installazione non installa, aggiorna o rimuove il componente. Non includere risorse protette in un pacchetto di installazione. È invece consigliabile usare i [meccanismi di sostituzione delle](../wfp/supported-file-replacement-mechanisms.md) risorse supportati per Windows Resource [Protection.](../wfp/windows-resource-protection-portal.md)

Per altre informazioni su WRP, vedere Windows [Resource Protection](../wfp/windows-resource-protection-portal.md) e informazioni fornite in [Microsoft Technet.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))

## <a name="wfp-for-windows-server-2003-and-windows-xp2000"></a>WFP per Windows Server 2003 e Windows XP/2000

Windows Il programma di installazione Windows Protezione file (WFP) durante l'installazione di file di sistema essenziali in Windows Server 2003, Windows XP e Windows 2000. Se un file di sistema protetto viene modificato da un'installazione automatica di un'applicazione, WFP ripristina il file alla versione del file verificata.

Windows Il programma di installazione non tenta mai di installare o sostituire un file protetto. Quando l'azione [InstallFiles](installfiles-action.md) o qualsiasi altra azione pianificata prima di InstallFiles tenta di installare un file protetto in Windows Server 2003, Windows XP o Windows 2000, il programma di installazione chiama WFP con una richiesta di installazione o sostituzione del file protetto. Il programma di installazione richiede l'installazione del file da WFP immediatamente dopo l'esecuzione dell'azione InstallFiles. WFP installa o sostituisce il file nel sistema dell'utente con una versione memorizzata nella cache del file protetto. Si noti che ciò non garantisce che la versione del file installata dalla cache sia la versione richiesta dall'applicazione. Dopo che WFP ha installato il file, il programma di installazione determina se questa versione corrisponde alla versione nel pacchetto. Se la versione del file nel pacchetto è maggiore della versione installata, il programma di installazione informa l'utente che non è in grado di aggiornare il sistema e che potrebbe essere necessario un aggiornamento del sistema operativo per l'applicazione.

Se un'azione sequenziata dopo [InstallFiles](installfiles-action.md) tenta di installare o sostituire un file protetto non già installato nel sistema, il programma di installazione non può chiamare WFP per installare il file. In questo caso, il programma di installazione informa l'utente che non può aggiornare il sistema e che potrebbe essere necessario un aggiornamento del sistema operativo per l'applicazione.

Il programma di installazione controlla anche con WFP quando si rimuovono i file e non tenta mai di rimuovere i file di sistema protetti.

## <a name="component-key-files-protected-by-wfp"></a>File di chiave del componente protetti da WFP

Si noti che se un Windows installer contiene un file WFP, questo file deve essere specificato come percorso della chiave per il componente.

Quando il programma di installazione tenta di installare il file di chiave di un componente in Windows Server 2003, Windows XP o Windows 2000, chiama prima WFP per determinare se il file di chiave è protetto. Quando il file di chiave di un componente è protetto da WFP e tale file di chiave è già installato, il programma di installazione aggiorna il componente solo se la versione del file di chiave nel pacchetto è maggiore della versione installata. Se il pacchetto di installazione specifica che un componente deve essere installato e il file di chiave del componente non è attualmente installato, indipendentemente dal fatto che il file di chiave sia protetto, il programma di installazione installa il componente. Dopo l'installazione, qualsiasi componente con un file di chiave protetto da WFP viene installato in modo permanente e il programma di installazione non rimuove né sostituisce mai il componente.

## <a name="installation-of-assemblies-by-wfp"></a>Installazione di assembly da parte del Wfp

WFP per gli assembly è diverso da WFP per i file di sistema.

WFP protegge Windows Server 2003, Windows XP e Windows 2000 file di sistema rilevando i tentativi di sostituire i file di sistema protetti. Questa protezione viene attivata dopo che WFP riceve una notifica di modifica della directory per un file in una directory protetta. Quando il WFP riceve questa notifica, determina quale file è stato modificato. Se il file è protetto, WFP cerca la firma del file in un file di catalogo statico per determinare se il nuovo file è la versione corretta. Se la versione del file non è corretta, il sistema sostituisce il file con la versione corretta dal supporto di cache o di distribuzione.

Al contrario, il WFP degli assembly è dinamico. Wfp viene esteso ai file quando vengono aggiunti all'assembly cache side-by-side condivisa. Se un assembly viene danneggiato, WFP richiederà che il programma di installazione sostituisca il file. Windows Il programma di installazione potrebbe o meno non essere in grado di sostituire il file a seconda che il pacchetto di origine sia accessibile. Se il pacchetto di origine non è accessibile, WFP inserirà una finestra di dialogo che indica che non è possibile ripristinare il file.

Si noti che gli assembly side-by-side condivisi non gestiti, installati in %windir% \\ winsxs, sono protetti da WFP. Gli assembly privati non gestiti, installati nella directory dell'applicazione, non sono protetti da WFP. Gli assembly globali gestiti installati nella directory dell'applicazione o %windir% \\ assembly \\ gac non sono protetti da WFP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Protezione delle risorse](../wfp/windows-resource-protection-portal.md)
</dt> </dl>

 

 
