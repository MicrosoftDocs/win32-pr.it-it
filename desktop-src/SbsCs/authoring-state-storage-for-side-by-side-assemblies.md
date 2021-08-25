---
description: Quando si creano assembly side-by-side personalizzati, seguire le linee guida per la creazione di assembly side-by-side e creare qualsiasi DLL da includere nell'assembly in base alle linee guida in Creazione di una DLL per un assembly side-by-side.
ms.assetid: 0e98bbcd-7e23-4a33-b0fa-1f936d0ef96b
title: Creazione di Archiviazione per assembly side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dd3b3dc62726c45a03fd388864faa7f359112687f0c03fb133276eef2280ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885521"
---
# <a name="authoring-state-storage-for-side-by-side-assemblies"></a>Creazione di Archiviazione per assembly side-by-side

Quando si creano assembly side-by-side personalizzati, seguire le linee guida per la creazione di assembly [side-by-side](guidelines-for-creating-side-by-side-assemblies.md) e creare qualsiasi DLL da includere nell'assembly in base alle linee guida in Creazione di una DLL per un assembly [side-by-side](authoring-a-dll-for-a-side-by-side-assembly.md).

Attenersi alle linee guida seguenti per l'archiviazione dello stato:

-   Progettare l'archiviazione dello stato in modo che sia compatibile con le versioni precedenti e in avanti. Si prevede che le versioni siano usate in qualsiasi ordine: ad esempio, v1, v3 e quindi v2.
-   Inizializzare e impostare le impostazioni predefinite per l'assembly nel codice dell'assembly. Non salvare le impostazioni predefinite nel Registro di sistema.
-   Le impostazioni del Registro di sistema devono essere scritte in base alle singole versioni per isolare più versioni di assembly che possono essere eseguite contemporaneamente. Progettare l'assembly side-by-side per archiviare e gestire correttamente lo stato dell'assembly durante scenari di condivisione side-by-side.
-   Gli assembly archiviano in genere le informazioni sullo stato nelle chiavi del Registro di sistema. Creare un set di file di intestazione e funzioni helper per fornire un modo semplice per eseguire la versione delle chiavi del Registro di sistema contenenti lo stato dell'assembly.
-   Tutte le informazioni sullo stato dell'assembly salvate nel Registro di sistema devono essere isolate da altre versioni dell'assembly. Le impostazioni di stato archiviate nel Registro di sistema devono essere salvate in singole sezioni di versione del Registro di sistema. Questa operazione è necessaria nelle parti HKLM e HKCU del Registro di sistema. Ad esempio, archiviare le impostazioni dello stato HKCU per la versione dell'assembly XXXX nella chiave del Registro di sistema seguente:

    **HKCU** \\ **MyCompany** \\ **MyComponent** \\ **VersionXXXX**

-   Le informazioni sullo stato archiviate nel Registro di sistema dagli assembly condivisi devono essere salvate in singole sezioni di versione del Registro di sistema. Ad esempio, un'impostazione di stato denominata EnableSuperCoolFeature potrebbe avere valore **TRUE** o **FALSE.** Archiviare il valore per [*un assembly side-by-side condiviso*](s-sbscs-gly.md) come segue:

    **HKEY \_ CurrentUser** \\ **Software** \\ **MyCompany** \\ **MyComponent** \\ **Version01.01** \\ **EnableSuperCoolFeature = TRUE**

-   Tutte le informazioni sullo stato archiviate nel Registro di sistema da assembly privati devono essere salvate in singole sezioni dell'applicazione del Registro di sistema. In questo modo le impostazioni dello stato dell'assembly vengono isolate nell'applicazione. È possibile usare la [**funzione GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) per configurare una radice virtuale. Ad esempio, se la versione dell'assembly XXYY è un assembly privato di "SomeApplication", una chiamata a **GetModuleFileName** restituisce "SomeApplication" e le impostazioni dello stato privato per l'assembly devono essere scritte nella chiave seguente:

    **HKCU** \\ **MyCompany** \\ **MyComponent** \\ **VersionXXYY** \\ **SomeApplication**

-   Rendere private le impostazioni dello stato condiviso archiviate nel Registro di sistema nel contesto dell'assembly in esecuzione. È possibile usare la [**funzione GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) per configurare una radice virtuale. Questa operazione deve essere eseguita per i rami HKLM e HKCU.
-   Idealmente, è consigliabile adottare un modello di persistenza in cui l'applicazione rende persistente lo stato e non modifica il Registro di sistema. Un'applicazione non deve toccare direttamente le voci del Registro di sistema del componente. L'assembly deve invece offrire funzioni API che salvano o ripristinano impostazioni compatibili side-by-side.
-   Gli assembly possono salvare le impostazioni di stato negli archivi esterni al Registro di sistema per consentire all'assembly di interagire con lo stato globale. Gli assembly side-by-side possono usare gli archivi compatibili side-by-side seguenti:
    -   Archivio protetto (*pstore*)
    -   Una cache WinInet
    -   Oggetto Microsoft SQL Server

 

 
