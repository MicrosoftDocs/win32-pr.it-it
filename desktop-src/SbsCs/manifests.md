---
description: I manifesti sono file XML che accompagnano e descrivono assembly affiancati o applicazioni isolate.
ms.assetid: 53c4c2e6-fff9-4506-b7e0-d091d2ec9883
title: Manifesti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2536e518f39791b400b9e99002b9575f4428d64d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310774"
---
# <a name="manifests"></a>Manifesti

I manifesti sono file XML che accompagnano e descrivono assembly affiancati o applicazioni isolate. I manifesti identificano in modo univoco l'assembly tramite l'elemento **assemblyIdentity** dell'assembly. Contengono informazioni utilizzate per l'associazione e l'attivazione, come le classi COM, le interfacce e le librerie dei tipi, che sono state tradizionalmente archiviate nel registro di sistema. I manifesti specificano anche i file che compongono l'assembly e possono includere le classi Windows se l'autore dell'assembly vuole che vengano sottoversioni. Gli assembly affiancati non sono registrati nel sistema, ma sono disponibili per le applicazioni e gli altri assembly nel sistema che specificano le dipendenze nei file manifesto.

I file manifesto consentono agli amministratori e alle applicazioni di gestire le versioni di assembly side-by-side dopo la distribuzione. Ogni assembly side-by-side deve avere un manifesto associato. L'installazione di Windows XP installa gli [assembly affiancati di Microsoft supportati](supported-microsoft-side-by-side-assemblies.md) con i relativi manifesti. Se si sviluppano assembly side-by-Side, è necessario installare anche i file manifesto. Per ulteriori informazioni, vedere [Installing side-by-side assemblys](installing-side-by-side-assemblies.md) and [manifest files Reference](manifest-files-reference.md).

I manifesti e i file di configurazione non sono localizzati.

Con gli assembly affiancati vengono usati i tipi di manifesti seguenti:

-   I [manifesti dell'assembly](assembly-manifests.md) descrivono gli assembly affiancati. Vengono usati per gestire i nomi, le versioni, le risorse e gli assembly dipendenti degli assembly side-by-side. I manifesti degli [assembly condivisi](/windows/desktop/Msi/shared-assemblies) vengono archiviati nella cartella WinSxS del sistema. I manifesti dell'assembly privato vengono archiviati come risorsa nella DLL o nella cartella dell'applicazione
-   I [manifesti dell'applicazione](application-manifests.md) descrivono [le applicazioni isolate](isolated-applications.md). Vengono utilizzati per gestire i nomi e le versioni degli assembly side-by-side condivisi a cui l'applicazione deve essere associata in fase di esecuzione. I manifesti dell'applicazione vengono copiati nella stessa cartella del file eseguibile dell'applicazione o inclusi come risorsa nel file eseguibile dell'applicazione.
-   [I file di configurazione dell'applicazione](application-configuration-files.md)sono manifesti utilizzati per eseguire l'override e il reindirizzamento delle versioni degli assembly dipendenti utilizzati dagli assembly side-by-side e dalle applicazioni.
-   [I file di configurazione del server di pubblicazione](publisher-configuration-files.md)sono manifesti utilizzati per reindirizzare la versione di un assembly affiancato a un'altra versione compatibile. La versione a cui viene reindirizzato l'assembly deve avere gli stessi valori Major. minor della versione originale.

 

 
