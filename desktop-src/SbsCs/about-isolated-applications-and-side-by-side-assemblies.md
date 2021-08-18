---
description: Le applicazioni isolate e gli assembly side-by-side offrono una soluzione che riduce i conflitti di controllo delle versioni delle DLL. Consentono alle applicazioni di condividere in modo sicuro gli assembly. Per altre informazioni, vedere Assembly condivisi.
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: Informazioni sulle applicazioni isolate e sugli assembly side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ab72689173d4e8942d10dfc62259091574634227c3f4d252b0d87853ec9be7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142664"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>Informazioni sulle applicazioni isolate e sugli assembly side-by-side

[Le applicazioni isolate](isolated-applications.md) e [gli assembly side-by-side](about-side-by-side-assemblies-.md) forniscono una soluzione che riduce i conflitti [*di controllo delle versioni delle DLL.*](d-sbscs-gly.md) Consentono alle applicazioni di condividere in modo sicuro gli assembly. Per altre informazioni, vedere [Assembly condivisi](/windows/desktop/Msi/shared-assemblies).

Un assembly è un'unità fondamentale per la denominazione, l'associazione, il controllo delle versioni, la distribuzione o la configurazione di un blocco di codice di programmazione. Le applicazioni con funzionalità comuni possono eseguire blocchi condivisi di codice di programmazione definiti moduli o assembly di codice. Questi assembly di codice possono essere inseriti in DLL o assembly COM. L'infrastruttura per la condivisione sicura degli assembly viene definita condivisione di assembly side-by-side.

[Gli assembly side-by-side](about-side-by-side-assemblies-.md) sono assembly di codice descritti dai [manifesti](manifests.md) e creati in modo che più versioni possano essere eseguite contemporaneamente senza conflitti tra loro. Quando gli sviluppatori scrivono manifesti e scrivono applicazioni per usare la condivisione di [assembly side-by-side,](side-by-side-assembly-sharing.md)è possibile eseguire più versioni di assembly nel sistema e ogni applicazione può specificare la versione dell'assembly da usare.

Un assembly [*side-by-side tipico*](s-sbscs-gly.md) è una singola DLL con un singolo manifesto. Gli assembly side-by-side archiviano le informazioni sull'associazione e sull'attivazione COM, tradizionalmente salvate nel Registro di sistema, nei manifesti. In alcuni casi, le versioni dell'assembly specificate nei manifesti possono essere modificate, a livello globale o per applicazione, da editori di assembly, sviluppatori di applicazioni o amministratori. Per altre informazioni, vedere [configurazione predefinita,](default-configuration.md)configurazione [del server di pubblicazione](publisher-configuration.md)e configurazione per [applicazione.](per-application-configuration.md)

Gli sviluppatori possono usare gli assembly side-by-side forniti da Microsoft o da altri editori di assembly side-by-side nelle applicazioni. Ad esempio, gli sviluppatori possono ottenere la funzionalità dei controlli comuni aggiornati, ad esempio il testo, progettando le applicazioni in modo da usare l'assembly side-by-side che contiene Comctl32.dll 6.0. Per l'elenco di assembly e manifesti side-by-side forniti con Windows XP, vedere [Assembly Microsoft side-by-side supportati.](supported-microsoft-side-by-side-assemblies.md) Gli sviluppatori possono anche creare assembly side-by-side personalizzati. Per altre informazioni, vedere Linee guida per [la creazione di assembly side-by-side.](guidelines-for-creating-side-by-side-assemblies.md)

 

 
