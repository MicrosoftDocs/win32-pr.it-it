---
description: I manifesti sono file XML che accompagnano e descrivono assembly side-by-side o applicazioni isolate.
ms.assetid: 53c4c2e6-fff9-4506-b7e0-d091d2ec9883
title: Manifesti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974aaea3dad60c80456d0acd085d610c81b93716342962abcd465adaf9efdf48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977211"
---
# <a name="manifests"></a>Manifesti

I manifesti sono file XML che accompagnano e descrivono assembly side-by-side o applicazioni isolate. I manifesti identificano in modo univoco l'assembly tramite **l'elemento assemblyIdentity** dell'assembly. Contengono informazioni usate per l'associazione e l'attivazione, ad esempio classi COM, interfacce e librerie dei tipi, tradizionalmente archiviate nel Registro di sistema. I manifesti specificano anche i file che costituiscono l'assembly e possono includere Windows classi se l'autore dell'assembly vuole che ne venga verificata la versione. Gli assembly side-by-side non sono registrati nel sistema, ma sono disponibili per le applicazioni e altri assembly nel sistema che specificano le dipendenze nei file manifesto.

I file manifesto consentono ad amministratori e applicazioni di gestire le versioni side-by-side degli assembly dopo la distribuzione. A ogni assembly side-by-side deve essere associato un manifesto. L'installazione Windows XP installa gli assembly [side-by-side Microsoft supportati](supported-microsoft-side-by-side-assemblies.md) con i relativi manifesti. Se si sviluppano assembly side-by-side personalizzati, è necessario installare anche i file manifesto. Per altre informazioni, vedere [Installazione di assembly side-by-side](installing-side-by-side-assemblies.md) e riferimenti [ai file manifesto](manifest-files-reference.md).

I manifesti e i file di configurazione non sono localizzati.

Con gli assembly side-by-side vengono usati i tipi di manifesti seguenti:

-   [I manifesti degli](assembly-manifests.md) assembly descrivono gli assembly side-by-side. Vengono usati per gestire i nomi, le versioni, le risorse e gli assembly dipendenti degli assembly side-by-side. I manifesti [degli assembly condivisi](/windows/desktop/Msi/shared-assemblies) vengono archiviati nella cartella WinSxS del sistema. I manifesti di assembly privati vengono archiviati come risorsa nella DLL o nella cartella dell'applicazione
-   [I manifesti dell'applicazione](application-manifests.md) [descrivono le applicazioni isolate.](isolated-applications.md) Vengono usati per gestire i nomi e le versioni degli assembly side-by-side condivisi a cui l'applicazione deve essere associata in fase di esecuzione. I manifesti dell'applicazione vengono copiati nella stessa cartella del file eseguibile dell'applicazione o inclusi come risorsa nel file eseguibile dell'applicazione.
-   [I file di configurazione](application-configuration-files.md)dell'applicazione sono manifesti usati per eseguire l'override e reindirizzare le versioni degli assembly dipendenti usati da applicazioni e assembly side-by-side.
-   [Publisher file di configurazione](publisher-configuration-files.md), sono manifesti usati per reindirizzare la versione di un assembly side-by-side a un'altra versione compatibile. La versione a cui viene reindirizzato l'assembly deve avere gli stessi valori major.minor della versione originale.

 

 
