---
description: La libreria di amministrazione MTS fornita con le interfacce di amministrazione COM+ garantisce la compatibilità con le versioni precedenti della libreria di amministrazione di MTS 2.0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Libreria di amministrazione MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e449e99ef675f7f8ce893a358806926cd3d1a63ed13e5cc9fff01b97d0742d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306159"
---
# <a name="mts-administration-library"></a>Libreria di amministrazione MTS

La libreria di amministrazione MTS fornita con le interfacce di amministrazione COM+ garantisce la compatibilità con le versioni precedenti della libreria di amministrazione di MTS 2.0. La maggior parte del codice di amministrazione di MTS 2.0 esistente continuerà a funzionare con la libreria MTSAdmin fornita. Tuttavia, alcune funzionalità sono state modificate.

Per sfruttare le nuove funzionalità o se si scrive codice di amministrazione per la prima volta, è consigliabile usare la libreria COMAdmin.

Gli elementi seguenti nella libreria di amministrazione MTS corrente vengono modificati dalla libreria di amministrazione di MTS 2.0:

-   **L'interfaccia IRemoteComponentUtil** non è più disponibile.
-   La **raccolta RemoteComponents** non è più disponibile.
-   La proprietà RoleID non è più disponibile. Il nome del ruolo viene ora usato come chiave per questa operazione.
-   Il **metodo ExportPackage** non esporta più un client.exe.
-   La proprietà RemoteComponentInstallPath non è più esposta nella [**raccolta LocalComputer.**](localcomputer.md)
-   La proprietà ApplicationInstallPath non verrà più esposta nella [**raccolta LocalComputer.**](localcomputer.md)
-   Il pacchetto Di sistema è ora denominato Applicazione di sistema.
-   Il pacchetto Utilities è ora denominato COM+ Utilities.
-   La proprietà IsSystem è presente nella raccolta [**Components**](components.md) in MTSAdmin, ma restituirà "NotImpl" se selezionata e non verrà salvata se impostata.
-   La proprietà PackageName non è più supportata dalla [**raccolta Components.**](components.md) Per individuare il nome del pacchetto, è ora necessario ottenere PackageID e quindi trovare il pacchetto corrispondente nella raccolta Packages.
-   Le proprietà seguenti non esistono più nella [**raccolta InterfacesForComponent:**](interfacesforcomponent.md)
    -   **ProxyCLSID**
    -   **ProxyDLL**
    -   **ProxyThreadingModel**
    -   **TypeLibFile**
    -   **TypeLibID**
    -   **TypeLibLangID**
    -   **TypeLibPlatform**
    -   **TypeLibVersion**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione automatica da MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Risultati e problemi della conversione COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversione manuale da MTS](manual-conversion-from-mts.md)
</dt> </dl>

 

 



