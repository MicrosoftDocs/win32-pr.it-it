---
description: Le linee guida seguenti illustrano come creare assembly side-by-side COM o Win32 personalizzati.
ms.assetid: e10fe92c-bce8-420e-a84c-2748e929eb1b
title: Linee guida per la creazione di assembly side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19054f0c48f74a373f0ce502cb6b52374db5ded00fcde3c284fad2609ba21e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885251"
---
# <a name="guidelines-for-creating-side-by-side-assemblies"></a>Linee guida per la creazione di assembly side-by-side

Le linee guida seguenti illustrano come creare assembly side-by-side COM o Win32 personalizzati. Potrebbe non essere necessario creare assembly side-by-side se la funzionalità necessaria viene fornita da uno degli assembly [side-by-side Microsoft supportati.](supported-microsoft-side-by-side-assemblies.md) In questo caso, usare gli assembly forniti da Microsoft e seguire le procedure per l'uso di assembly side-by-side in [Using Isolated Applications and Side-by-side Assemblies](using-isolated-applications-and-side-by-side-assemblies.md).

Prima di tutto, valutare se il componente costituisce un candidato adatto per un assembly side-by-side. Per altre informazioni, [vedere È necessario fornire un componente condiviso come assembly side-by-side?](should-you-provide-a-shared-component-as-a-side-by-side-assembly.md)

Per creare un assembly side-by-side, seguire queste linee guida:

-   Decidere quali risorse includere nell'assembly. Tenere presente che un assembly è costituito da uno o più file che vengono sempre forniti insieme ad applicazioni e clienti. L'assembly funge da unità fondamentale usata per la denominazione, l'associazione, il controllo delle versioni, la distribuzione e [la configurazione predefinita.](default-configuration.md) Come regola generale, quando non si sa se due risorse appartengono allo stesso assembly, è consigliabile crearlo per passare ad assembly separati. In genere, un assembly side-by-side è costituito da una singola DLL.
-   Creare un manifesto [dell'assembly](manifests.md) per l'assembly. Il manifesto deve descrivere l'oggetto COM o le librerie dei tipi nell'assembly. Per altre informazioni sugli elementi da creare in un manifesto dell'assembly, vedere [Manifesti dell'assembly.](assembly-manifests.md)
-   Valutare l'utilizzo degli oggetti quando nel sistema vengono eseguite più versioni dell'assembly. Determinare se versioni diverse dell'assembly richiedono strutture di dati separate, ad esempio file mappati alla memoria, named pipe, classi e messaggi Windows registrati, memoria condivisa, semafori, mutex e driver hardware. Tutte le strutture di dati usate tra le versioni degli assembly devono essere versioni compatibili con le versioni precedenti. Decidere quali strutture di dati possono essere usate tra le versioni e quali strutture di dati devono essere private per una versione. Determinare se le strutture di dati condivise richiedono oggetti di sincronizzazione separati, ad esempio semafori e mutex.
-   Creare la DLL in modo che funzioni correttamente come assembly side-by-side rispettando le linee guida riportate in Creazione di una DLL per un [assembly side-by-side.](authoring-a-dll-for-a-side-by-side-assembly.md)
-   Creare un set di file di intestazione e funzioni helper per fornire un modo semplice per creare versioni delle chiavi del Registro di sistema contenenti lo stato dell'assembly. Gli assembly in genere salvano le impostazioni di stato nelle chiavi del Registro di sistema. Le impostazioni del Registro di sistema devono essere scritte in base a una singola versione per isolare più versioni di assembly che possono essere eseguite contemporaneamente. Progettare l'assembly e la DLL side-by-side per archiviare e gestire correttamente lo stato dell'assembly durante scenari di condivisione side-by-side. Seguire le linee guida [in Creazione di Archiviazione per assembly side-by-side.](authoring-state-storage-for-side-by-side-assemblies.md)
-   Gli sviluppatori di applicazioni che [usano assembly privati devono](/windows/desktop/Msi/private-assemblies) proteggere la directory dell'applicazione. Se l'applicazione viene installata usando il Windows [di installazione](../msi/windows-installer-portal.md)di , la directory dell'applicazione può essere protetta tramite la tabella LockPermissions. In genere, al sistema viene assegnato l'accesso in lettura, scrittura ed esecuzione agli assembly privati. a tutti gli altri processi viene assegnato solo l'accesso in lettura e di esecuzione.
-   Testare l'assembly usando scenari con condivisione side-by-side per assicurarsi che sia un assembly side-by-side valido. La corretta installazione dell'assembly non è sufficiente per garantire che funzioni come previsto.
-   Adottare un metodo per numerare gli aggiornamenti per l'assembly. Ogni assembly è associato a un numero di versione in quattro parti. Da sinistra a destra, le parti principali, secondarie, di compilazione e di revisione sono separate da punti. Modificare il numero principale o secondario di un assembly per una versione non compatibile con le versioni precedenti. Modificare solo le parti di compilazione e revisione per le modifiche compatibili con le versioni precedenti dell'assembly. Ad esempio, uno sviluppatore potrebbe adottare un metodo di numerazione in cui tutti gli elementi 1.0.0. \* I numeri di versione si riferiscono alle versioni di aggiornamento alla versione dell'assembly 1.0.0.0.

 

 
