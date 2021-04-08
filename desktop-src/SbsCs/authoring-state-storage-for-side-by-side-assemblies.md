---
description: Quando si creano assembly affiancati, attenersi alle linee guida per la creazione di assembly affiancati e creare eventuali DLL da includere nell'assembly in base alle linee guida per la creazione di una DLL per un assembly affiancato.
ms.assetid: 0e98bbcd-7e23-4a33-b0fa-1f936d0ef96b
title: Creazione dell'archiviazione dello stato per gli assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee388cf680ee3a186a225ca7e3bde8b6eae625d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757310"
---
# <a name="authoring-state-storage-for-side-by-side-assemblies"></a>Creazione dell'archiviazione dello stato per gli assembly affiancati

Quando si creano assembly affiancati, attenersi alle [linee guida per la creazione di assembly affiancati](guidelines-for-creating-side-by-side-assemblies.md) e creare eventuali dll da includere nell'assembly in base alle linee guida per la creazione di [una dll per un assembly affiancato](authoring-a-dll-for-a-side-by-side-assembly.md).

Rispettare le linee guida seguenti per l'archiviazione dello stato:

-   Progettare l'archiviazione dello stato in modo che sia compatibile con le versioni precedenti e successive. Si prevede che le versioni vengano utilizzate in qualsiasi ordine, ad esempio V1, V3, quindi V2.
-   Inizializzare e impostare le impostazioni predefinite per l'assembly nel codice dell'assembly. Non salvare le impostazioni predefinite nel registro di sistema.
-   Le impostazioni del registro di sistema devono essere scritte in base a una singola versione per isolare più versioni di assembly che possono essere eseguite contemporaneamente. Progettare un assembly side-by-side per archiviare e gestire correttamente lo stato dell'assembly durante gli scenari di condivisione side-by-side.
-   Gli assembly comunemente archiviano le informazioni sullo stato nelle chiavi del registro di sistema. Creazione di un set di file di intestazione e funzioni helper per fornire un modo semplice per la versione delle chiavi del registro di sistema contenenti lo stato dell'assembly.
-   Le informazioni sullo stato dell'assembly salvate nel registro di sistema devono essere isolate dalle altre versioni dell'assembly. Le impostazioni di stato archiviate nel registro di sistema devono essere salvate in singole sezioni del registro di sistema. Questa operazione è necessaria nelle parti HKLM e HKCU del registro di sistema. Ad esempio, archiviare le impostazioni dello stato HKCU per l'assembly versione XXXX sotto la chiave del registro di sistema seguente:

    **HKCU** \\ **MyCompany** \\ **Componente** \\ di **VersionXXXX**

-   Tutte le informazioni sullo stato archiviate nel registro di sistema da assembly condivisi devono essere salvate nelle singole sezioni della versione del registro di sistema. Ad esempio, un'impostazione di stato denominata EnableSuperCoolFeature potrebbe avere un valore **true** o **false**. Archiviare il valore per un [*assembly side-by-side condiviso*](s-sbscs-gly.md) come segue:

    **HKEY \_ CurrentUser** \\ **software** \\ **MyCompany MyCompany** \\  \\ **versione 01.01** \\ **EnableSuperCoolFeature = true**

-   Tutte le informazioni sullo stato archiviate nel registro di sistema da assembly privati devono essere salvate nelle singole sezioni dell'applicazione del registro di sistema. Questo consente di isolare le impostazioni dello stato dell'assembly nell'applicazione. Per configurare una radice virtuale, è possibile usare la funzione [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) . Se ad esempio la versione dell'assembly XXYY è un assembly privato di "SomeApplication", una chiamata a **GetModuleFileName** restituisce "SomeApplication" e le impostazioni di stato privato per l'assembly devono essere scritte con la chiave seguente:

    **HKCU** \\ **MyCompany** \\ **Componente** \\ di **VersionXXYY** \\ **SomeApplication**

-   Rendere le impostazioni dello stato condivise archiviate nel registro di sistema private al contesto dell'assembly eseguito da. Per configurare una radice virtuale, è possibile usare la funzione [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) . Questa operazione deve essere eseguita per i rami HKLM e HKCU.
-   Idealmente, è consigliabile adottare un modello di persistenza in cui l'applicazione rende persistente lo stato e non modifica il registro di sistema. Non è necessario che un'applicazione tocchi direttamente le voci del registro di sistema del componente. L'assembly deve invece offrire funzioni API che salvano o ripristinano le impostazioni compatibili side-by-side.
-   Gli assembly possono salvare le impostazioni dello stato nei negozi esterni al registro di sistema per consentire all'assembly di interagire con lo stato globale. Gli assembly affiancati possono usare i seguenti archivi compatibili side-by-Side:
    -   Archivio protetto (*PStore*)
    -   Una cache WinInet
    -   Microsoft SQL Server

 

 
