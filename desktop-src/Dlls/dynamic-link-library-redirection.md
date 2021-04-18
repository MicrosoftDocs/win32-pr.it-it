---
description: Le applicazioni possono dipendere da una versione specifica di una DLL condivisa e iniziare a non riuscire se un'altra applicazione viene installata con una versione più recente o precedente della stessa DLL.
ms.assetid: 3b426b6c-1ad5-43b9-81ea-5e6d3c6588c8
title: Reindirizzamento libreria Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b575d566231058cca13c10a067a3c2e20078073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308922"
---
# <a name="dynamic-link-library-redirection"></a>Reindirizzamento libreria Dynamic-Link

Le applicazioni possono dipendere da una versione specifica di una DLL condivisa e iniziare a non riuscire se un'altra applicazione viene installata con una versione più recente o precedente della stessa DLL. Esistono due modi per assicurarsi che l'applicazione usi la DLL corretta: reindirizzamento DLL e componenti affiancati. Gli sviluppatori e gli amministratori devono utilizzare il reindirizzamento DLL per le applicazioni esistenti, perché non richiede alcuna modifica all'applicazione. Se si crea una nuova applicazione o si aggiorna un'applicazione e si vuole isolare l'applicazione da potenziali problemi, creare un [componente affiancato](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Per abilitare il reindirizzamento DLL a livello di computer, è necessario creare una nuova chiave del registro di sistema. Creare una nuova chiave DWORD denominata **DevOverrideEnable** in **HKLM\Software\Microsoft\Windows NT\CurrentVersion\Image opzioni di esecuzione file** e impostarla su 1. Al termine di questa operazione, è necessario riavviare il computer per visualizzare gli effetti.

Per usare il reindirizzamento DLL, creare un *file di reindirizzamento* per l'applicazione. Il nome del file di reindirizzamento deve essere il seguente: *\_ nome dell'app*. local. Se ad esempio il nome dell'applicazione è Editor.exe, il file di reindirizzamento deve essere denominato Editor.exe. local. È necessario installare il file. local nella directory dell'applicazione. È necessario installare anche le dll nella directory dell'applicazione.

Il contenuto di un file di reindirizzamento viene ignorato, ma la sua presenza fa in modo che Windows verifichi prima di tutto la directory dell'applicazione ogni volta che viene caricata una DLL, indipendentemente dal percorso specificato per [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Se la DLL non viene trovata nella directory dell'applicazione, queste funzioni usano il consueto ordine di ricerca. Ad esempio, se l'applicazione c: \\ myapp \\myapp.exe chiama **LoadLibrary** usando il percorso seguente:

c: \\ Programmi file \\ comuni del \\ sistema \\mydll.dll

Se sono presenti sia c: \\ myapp \\myapp.exe. local che c: \\ MyApp \\mydll.dll, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) carica ilmydll.dll c: \\ MyApp \\ . In caso contrario, **LoadLibrary** carica i file comuni del sistema di file c: \\ Program \\ \\ \\mydll.dll.

In alternativa, se esiste una directory denominata c: \\ myapp \\myapp.exe. local e contiene mydll.dll, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) carica c: \\ MyApp \\myapp.exe. local \\mydll.dll.

Se l'applicazione dispone di un manifesto, i file. local verranno ignorati.

Se si usa il reindirizzamento DLL e l'applicazione non ha accesso a tutte le unità e directory nell'ordine di ricerca, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) interrompe la ricerca non appena l'accesso viene negato. Se non si usa il reindirizzamento DLL, **LoadLibrary** ignora le directory a cui non può accedere e quindi continua la ricerca.

È consigliabile installare le DLL dell'applicazione nella stessa directory che contiene l'applicazione, anche se non si usa il reindirizzamento DLL. In questo modo si garantisce che l'installazione dell'applicazione non sovrascriva le altre copie della DLL e provochi l'esito negativo di altre applicazioni. Inoltre, se si segue questa procedura consigliata, le altre applicazioni non sovrascrivono la copia della DLL e impediscono l'esecuzione dell'applicazione.

 

 
