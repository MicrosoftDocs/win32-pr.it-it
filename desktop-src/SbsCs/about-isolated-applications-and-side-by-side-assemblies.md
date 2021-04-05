---
description: Le applicazioni isolate e gli assembly affiancati forniscono una soluzione che riduce i conflitti di controllo delle versioni DLL. Consentono alle applicazioni di condividere in modo sicuro gli assembly. Per altre informazioni, vedere assembly condivisi.
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: Informazioni sulle applicazioni isolate e gli assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9099ca2e41d61c84e2952661b33ca008651f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131610"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>Informazioni sulle applicazioni isolate e gli assembly affiancati

[Le applicazioni isolate](isolated-applications.md) e gli [assembly affiancati](about-side-by-side-assemblies-.md) forniscono una soluzione che riduce i [*conflitti di controllo delle versioni dll*](d-sbscs-gly.md). Consentono alle applicazioni di condividere in modo sicuro gli assembly. Per altre informazioni, vedere [assembly condivisi](/windows/desktop/Msi/shared-assemblies).

Un assembly è un'unità fondamentale per la denominazione, l'associazione, il controllo delle versioni, la distribuzione o la configurazione di un blocco di codice di programmazione. Le applicazioni con funzionalità comuni possono eseguire blocchi condivisi del codice di programmazione, detti moduli o assembly di codice. Questi assembly di codice possono essere inseriti in dll o assembly COM. L'infrastruttura per la condivisione sicura degli assembly è detta condivisione degli assembly side-by-side.

Gli [assembly affiancati](about-side-by-side-assemblies-.md) sono assembly di codice descritti da [manifesti](manifests.md) e creati in modo che più versioni possano essere eseguite contemporaneamente senza conflitti. Quando gli sviluppatori creano manifesti e scrivono applicazioni per l'uso della [condivisione di assembly affiancata](side-by-side-assembly-sharing.md), è possibile eseguire più versioni di assembly nel sistema e ogni applicazione può specificare la versione dell'assembly da usare.

Un [*assembly side-by-side*](s-sbscs-gly.md) tipico è una singola DLL con un singolo manifesto. Gli assembly affiancati archiviano le informazioni relative all'associazione e all'attivazione COM, tradizionalmente salvate nel registro di sistema, nei manifesti. In alcuni casi, le versioni dell'assembly specificato nei manifesti possono essere modificate, a livello globale o per applicazione, da autori di assembly, sviluppatori di applicazioni o amministratori. Per ulteriori informazioni, vedere configurazione [predefinita](default-configuration.md), [configurazione del server di pubblicazione](publisher-configuration.md)e [configurazione per ogni applicazione](per-application-configuration.md).

Gli sviluppatori possono utilizzare gli assembly affiancati forniti da Microsoft o da altri autori di assembly affiancati nelle rispettive applicazioni. Gli sviluppatori possono, ad esempio, ottenere le funzionalità dei controlli comuni aggiornati, ad esempio i temi, progettando le applicazioni in modo da usare l'assembly affiancato che contiene Comctl32.dll 6,0. Per l'elenco degli assembly affiancati e dei manifesti forniti con Windows XP, vedere [assembly affiancati di Microsoft supportati](supported-microsoft-side-by-side-assemblies.md). Gli sviluppatori possono anche creare assembly affiancati. Per ulteriori informazioni, vedere [linee guida per la creazione di assembly affiancati](guidelines-for-creating-side-by-side-assemblies.md).

 

 
