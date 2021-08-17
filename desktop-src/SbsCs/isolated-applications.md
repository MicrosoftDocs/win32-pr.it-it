---
description: Le applicazioni isolate sono applicazioni autodescrittori installate con manifesti. Le applicazioni isolate possono usare sia assembly privati che assembly condivisi.
ms.assetid: 66c65b92-7c49-4932-b8c5-91b20fb0a038
title: Applicazioni isolate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abe13dc452c81b2a763706036e1f59400f31ccd138c95a9ab241481898aee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142124"
---
# <a name="isolated-applications"></a>Applicazioni isolate

Le applicazioni isolate sono applicazioni autodescrittori installate [con manifesti](manifests.md). Le applicazioni isolate possono utilizzare [sia assembly privati](/windows/desktop/Msi/private-assemblies) che assembly [condivisi.](/windows/desktop/Msi/shared-assemblies)

Un'applicazione viene considerata completamente isolata se tutti i relativi componenti sono assembly [side-by-side](about-side-by-side-assemblies-.md) condivisi o assembly privati. Viene chiamato parzialmente isolato se usa alcuni componenti che non sono assembly side-by-side. Si noti che se un'applicazione usa alcuni componenti che non sono assembly side-by-side o usa assembly privati, l'installazione o la rimozione di altre applicazioni nel sistema potrebbe essere interessata dall'installazione o dalla rimozione di altre applicazioni. Per altre informazioni, vedere [Condivisione di assembly side-by-side.](side-by-side-assembly-sharing.md)

Gli sviluppatori sono invitati a progettare applicazioni isolate e ad aggiornare le applicazioni esistenti in applicazioni isolate per i motivi seguenti:

-   Le applicazioni isolate sono più stabili e aggiornate in modo affidabile perché non sono interessate dall'installazione, dalla rimozione o dall'aggiornamento di altre applicazioni nel sistema.
-   Le applicazioni isolate possono essere progettate in modo che siano sempre eseguite usando le stesse versioni di assembly con cui sono state compilate e testate.
-   Le applicazioni isolate possono usare le funzionalità fornite dagli assembly side-by-side resi disponibili da Microsoft. Per altre informazioni, vedere [Assembly side-by-side Microsoft supportati.](supported-microsoft-side-by-side-assemblies.md)
-   Le applicazioni isolate non sono collegate alla pianificazione della spedizione degli assembly side-by-side perché le applicazioni e gli amministratori possono aggiornare la configurazione dopo la distribuzione senza dover reinstallare l'applicazione. Ciò non si applica nel caso in cui venga resa disponibile una sola versione dell'assembly.
-   È possibile installare un'applicazione completamente isolata usando il **comando xcopy.** [Windows programma di installazione](../msi/windows-installer-portal.md) può essere usato anche per installare un'applicazione isolata senza alcun impatto sul Registro di sistema. Per altre informazioni, vedere [Installazione di assembly Win32.](../msi/installation-of-win32-assemblies.md)

In alcuni casi, le applicazioni esistenti possono essere aggiornate in un'applicazione isolata senza dover riscrivere il codice dell'applicazione. È [possibile creare](application-manifests.md) un manifesto dell'applicazione che descrive le dipendenze dell'applicazione da assembly [side-by-side.](about-side-by-side-assemblies-.md) Se l'applicazione usa componenti che non sono assembly side-by-side, questi possono essere distribuiti [come assembly privati.](/windows/desktop/Msi/private-assemblies) Si noti che la possibilità di eseguire questa operazione con componenti di terze parti può dipendere dalle licenze perché il componente dovrà essere creato come assembly. Ad esempio, creando un manifesto dell'applicazione e specificando una dipendenza dai controlli comuni side-by-side (COMCTL32), un'applicazione in esecuzione in Windows XP può sfruttare i Windows di . È sempre consigliabile testare l'applicazione per assicurarsi che sia compatibile con la nuova versione dell'assembly COMCTL32.

Potrebbe non essere possibile aggiornare ogni applicazione esistente in un'applicazione completamente isolata. Ad esempio, alcuni assembly Windows file protection [(WFP)](/windows/desktop/Wfp/windows-resource-protection-portal) non sono disponibili come assembly side-by-side e non possono essere installati con l'applicazione come assembly privato. È possibile isolare parzialmente tali applicazioni specificando dipendenze di assembly side-by-side per alcuni assembly dell'applicazione in un manifesto dell'applicazione.

 

 
