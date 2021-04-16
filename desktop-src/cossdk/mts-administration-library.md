---
description: La libreria di amministrazione MTS fornita con le interfacce di amministrazione COM+ fornisce compatibilità con le versioni precedenti della libreria di amministrazione MTS 2,0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Libreria di amministrazione MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523538"
---
# <a name="mts-administration-library"></a>Libreria di amministrazione MTS

La libreria di amministrazione MTS fornita con le interfacce di amministrazione COM+ fornisce compatibilità con le versioni precedenti della libreria di amministrazione MTS 2,0. La maggior parte del codice di amministrazione MTS 2,0 esistente continuerà a funzionare con la libreria MTSAdmin fornita. Tuttavia, alcune funzionalità sono state modificate.

Per sfruttare i vantaggi delle nuove funzionalità o se si scrive il codice di amministrazione per la prima volta, è necessario usare la libreria COMAdmin.

Gli elementi seguenti nella libreria di amministrazione MTS corrente sono stati modificati dalla libreria di amministrazione MTS 2,0:

-   L'interfaccia **IRemoteComponentUtil** non è più disponibile.
-   La raccolta **RemoteComponents** non è più disponibile.
-   La proprietà RoleID non è più disponibile. il nome del ruolo viene ora usato come chiave per questo oggetto.
-   Il metodo **ExportPackage** non esporta più un client.exe.
-   La proprietà RemoteComponentInstallPath non è più esposta nella raccolta [**LocalComputer**](localcomputer.md) .
-   La proprietà ApplicationInstallPath non verrà più esposta nella raccolta [**LocalComputer**](localcomputer.md) .
-   Il pacchetto di sistema è ora denominato applicazione di sistema.
-   Il pacchetto Utilities è ora denominato utilità COM+.
-   La proprietà IsSynchronized è presente nella raccolta [**Components**](components.md) in MTSAdmin, ma restituirà "NotImpl" quando è selezionata e non verrà salvata se impostata.
-   La proprietà PackageName non è più supportata dalla raccolta [**Components**](components.md) . Per determinare il nome del pacchetto, è ora necessario ottenere il PackageID e quindi trovare il pacchetto corrispondente nella raccolta di pacchetti.
-   Le proprietà seguenti non esistono più nella raccolta [**InterfacesForComponent**](interfacesforcomponent.md) :
    -   **ProxyCLSID**
    -   **ProxyDLL**
    -   **ProxyThreadingModel**
    -   **Filelibreriatipi**
    -   **TypeLibID**
    -   **TypeLibLangID**
    -   **TypeLibPlatform**
    -   **TypeLibVersion**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione automatica da MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Risultati e problemi di conversione COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversione manuale da MTS](manual-conversion-from-mts.md)
</dt> </dl>

 

 



