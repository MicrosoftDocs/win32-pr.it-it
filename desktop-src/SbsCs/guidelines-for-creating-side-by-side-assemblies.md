---
description: Le linee guida seguenti illustrano come creare assembly affiancati COM o Win32.
ms.assetid: e10fe92c-bce8-420e-a84c-2748e929eb1b
title: Linee guida per la creazione di assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af8e8fd2bd31a65477b44d3afcf2156d5160a72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128830"
---
# <a name="guidelines-for-creating-side-by-side-assemblies"></a>Linee guida per la creazione di assembly affiancati

Le linee guida seguenti illustrano come creare assembly affiancati COM o Win32. Se la funzionalità necessaria è fornita da uno degli assembly affiancati di [Microsoft supportati](supported-microsoft-side-by-side-assemblies.md), potrebbe non essere necessario creare assembly side-by-side. In questo caso, utilizzare gli assembly forniti da Microsoft e seguire le procedure per l'utilizzo di assembly affiancati in [utilizzando applicazioni isolate e assembly affiancati](using-isolated-applications-and-side-by-side-assemblies.md).

Per prima cosa, valutare se il componente rende un candidato adatto per un assembly affiancato. Per ulteriori informazioni, vedere [se si desidera fornire un componente condiviso come assembly side-by-side.](should-you-provide-a-shared-component-as-a-side-by-side-assembly.md)

Per creare un assembly affiancato, attenersi alle seguenti linee guida:

-   Decidere quali risorse includere nell'assembly. Tenere presente che un assembly è costituito da uno o più file che vengono sempre forniti insieme alle applicazioni e ai clienti. L'assembly funge da unità di base utilizzata per la denominazione, l'associazione, il controllo delle versioni, la distribuzione e la [configurazione predefinita](default-configuration.md). Come regola generale, quando si è certi che due risorse appartengano nello stesso assembly, è consigliabile crearle per passare a assembly distinti. In genere, un assembly affiancato è costituito da una singola DLL.
-   Creazione di un [manifesto](manifests.md) dell'assembly per l'assembly. Il manifesto deve descrivere l'oggetto COM o le librerie dei tipi nell'assembly. Per ulteriori informazioni su ciò che deve essere creato in un manifesto dell'assembly, vedere [manifesti dell'assembly](assembly-manifests.md).
-   Valutare l'utilizzo di oggetti quando nel sistema viene eseguita più di una versione dell'assembly. Determinare se versioni diverse dell'assembly richiedono strutture di dati separate, ad esempio file mappati alla memoria, named pipe, messaggi e classi di Windows registrate, memoria condivisa, semafori, mutex e driver hardware. Tutte le strutture di dati utilizzate nelle versioni degli assembly devono essere versioni compatibili con le versioni precedenti. Decidere quali strutture di dati possono essere usate tra le versioni e quali strutture di dati devono essere private di una versione. Determinare se le strutture di dati condivise richiedono oggetti di sincronizzazione distinti, ad esempio semafori e mutex.
-   Creare la DLL per lavorare correttamente come assembly affiancato rispettando le linee guida per la [creazione di una dll per un assembly affiancato](authoring-a-dll-for-a-side-by-side-assembly.md).
-   Creazione di un set di file di intestazione e funzioni helper per fornire un modo semplice per la versione delle chiavi del registro di sistema contenenti lo stato dell'assembly. Gli assembly salvano in genere le impostazioni dello stato nelle chiavi del registro di sistema. Le impostazioni del registro di sistema devono essere scritte in base a una singola versione per isolare più versioni di assembly che possono essere eseguite contemporaneamente. Progettare l'assembly affiancato e la DLL per archiviare e gestire correttamente lo stato dell'assembly durante gli scenari di condivisione side-by-side. Seguire le linee guida [per la creazione dell'archiviazione dello stato per gli assembly affiancati](authoring-state-storage-for-side-by-side-assemblies.md).
-   Gli sviluppatori di applicazioni che utilizzano [assembly privati](/windows/desktop/Msi/private-assemblies) devono proteggere la directory dell'applicazione. Se l'applicazione viene installata usando il [Windows Installer](../msi/windows-installer-portal.md), la directory dell'applicazione può essere protetta tramite la tabella LockPermissions. In genere, al sistema viene assegnato l'accesso in lettura, scrittura ed esecuzione agli assembly privati. a tutti gli altri processi viene assegnato solo l'accesso in lettura e esecuzione.
-   Testare l'assembly usando gli scenari con la condivisione side-by-side per assicurarsi che sia un assembly side-by-side valido. La corretta installazione dell'assembly non è sufficiente per garantire che funzioni come previsto.
-   Adottare un metodo per la numerazione degli aggiornamenti per l'assembly. Ogni assembly è associato a un numero di versione in quattro parti. Da sinistra a destra, le parti principale, secondaria, di build e di revisione sono separate da punti. Modificare il numero principale o secondario di un assembly per una versione incompatibile con le versioni precedenti. Modificare solo le parti di compilazione e revisione per le modifiche compatibili con le versioni precedenti nell'assembly. Uno sviluppatore può ad esempio adottare un metodo di numerazione in cui tutte le 1.0.0. \* i numeri di versione si riferiscono alle versioni di aggiornamento per l'assembly versione 1.0.0.0.

 

 
