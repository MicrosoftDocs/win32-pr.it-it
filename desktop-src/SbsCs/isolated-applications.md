---
description: Le applicazioni isolate sono applicazioni autodescrittive installate con manifesti. Le applicazioni isolate possono utilizzare sia assembly privati che assembly condivisi.
ms.assetid: 66c65b92-7c49-4932-b8c5-91b20fb0a038
title: Applicazioni isolate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10c1b3f175ec05751bfc84e3826b19c9c9db01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484636"
---
# <a name="isolated-applications"></a>Applicazioni isolate

Le applicazioni isolate sono applicazioni autodescrittive installate con [manifesti](manifests.md). Le applicazioni isolate possono utilizzare sia [assembly privati](/windows/desktop/Msi/private-assemblies) che [assembly condivisi](/windows/desktop/Msi/shared-assemblies).

Un'applicazione viene considerata completamente isolata se tutti i relativi componenti sono [assembly side-by-side](about-side-by-side-assemblies-.md) condivisi o assembly privati. Viene chiamato parzialmente isolato se usa alcuni componenti che non sono assembly affiancati. Si noti che se un'applicazione usa alcuni componenti che non sono assembly affiancati o USA assembly privati, l'applicazione potrebbe essere interessata dall'installazione o dalla rimozione di altre applicazioni nel sistema. Per ulteriori informazioni, vedere [condivisione di assembly affiancati](side-by-side-assembly-sharing.md).

Gli sviluppatori sono invitati a progettare applicazioni isolate e a aggiornare le applicazioni esistenti in applicazioni isolate per i motivi seguenti:

-   Le applicazioni isolate sono più stabili e aggiornate in modo affidabile perché non sono interessate dall'installazione, dalla rimozione o dall'aggiornamento di altre applicazioni nel sistema.
-   Le applicazioni isolate possono essere progettate in modo da essere sempre eseguite utilizzando le stesse versioni degli assembly con cui sono state compilate e testate.
-   Le applicazioni isolate possono utilizzare la funzionalità fornita dagli assembly affiancati resi disponibili da Microsoft. Per ulteriori informazioni, vedere [assembly affiancati di Microsoft supportati](supported-microsoft-side-by-side-assemblies.md).
-   Le applicazioni isolate non sono associate alla pianificazione di spedizione degli assembly affiancati, perché le applicazioni e gli amministratori possono aggiornare la configurazione dopo la distribuzione senza dover reinstallare l'applicazione. Questa situazione non è applicabile nel caso in cui venga resa disponibile una sola versione dell'assembly.
-   È possibile installare un'applicazione completamente isolata utilizzando il comando **xcopy** . [Windows Installer](../msi/windows-installer-portal.md) possibile utilizzare anche per installare un'applicazione isolata senza conseguenze per il registro di sistema. Per ulteriori informazioni, vedere [installazione di assembly Win32](../msi/installation-of-win32-assemblies.md).

In alcuni casi, le applicazioni esistenti possono essere aggiornate in un'applicazione isolata senza dover riscrivere il codice dell'applicazione. È possibile creare un [manifesto dell'applicazione](application-manifests.md) che descrive le dipendenze dell'applicazione [dagli assembly affiancati](about-side-by-side-assemblies-.md). Se l'applicazione usa componenti che non sono assembly affiancati, questi possono essere distribuiti come [assembly privati](/windows/desktop/Msi/private-assemblies). Si noti che la possibilità di eseguire questa operazione con componenti di terze parti può dipendere dalla gestione delle licenze perché il componente deve essere creato come assembly. Ad esempio, creando un manifesto dell'applicazione e specificando una dipendenza dai controlli comuni affiancati (COMCTL32), un'applicazione in esecuzione in Windows XP può sfruttare i vantaggi offerti dai *temi* di Windows. È sempre necessario testare l'applicazione per assicurarsi che sia compatibile con la nuova versione dell'assembly COMCTL32.

Potrebbe non essere possibile aggiornare tutte le applicazioni esistenti in un'applicazione completamente isolata. Alcuni assembly di sistema di [protezione dei file di Windows](/windows/desktop/Wfp/windows-resource-protection-portal) , ad esempio, non sono disponibili come assembly side-by-side e non possono essere installati con l'applicazione come assembly privato. Potrebbe essere possibile isolare parzialmente tali applicazioni specificando dipendenze degli assembly affiancati per alcuni assembly dell'applicazione in un manifesto dell'applicazione.

 

 
