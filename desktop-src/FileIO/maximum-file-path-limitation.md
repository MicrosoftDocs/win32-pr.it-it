---
description: Limite massimo di lunghezza del percorso.
title: Limite lunghezza massima percorso
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: 995cd6d973a5bab02deae3068e39e8e3f3d51f40
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "104234539"
---
# <a name="maximum-path-length-limitation"></a>Limite lunghezza massima percorso

Nell'API Windows (con alcune eccezioni descritte nei paragrafi seguenti), la lunghezza massima di un percorso è il **\_ percorso** massimo, che è definito come 260 caratteri. Un percorso locale è strutturato nell'ordine seguente: lettera di unità, due punti, barra rovesciata, componenti nome separati da barre rovesciate e un carattere null di terminazione. Ad esempio, il percorso massimo sull'unità D è "D: \\ *some stringa di percorso di 256 caratteri* &lt; NUL &gt; ", dove " &lt; NUL &gt; " rappresenta il carattere null di terminazione invisibile per la tabella codici di sistema corrente. I caratteri < > vengono usati qui per la chiarezza visiva e non possono far parte di una stringa di percorso valida.

È possibile, ad esempio, raggiungere questa limitazione se si clona un repository git con nomi di file lunghi in una cartella a cui è associato un nome lungo.


> [!Note]  
> Le funzioni di i/O dei file nell'API Windows convertono "/" in " \\ " come parte della conversione del nome in un nome di tipo NT, tranne quando si usa il \\ \\ prefisso "? \\ ", come descritto nelle sezioni seguenti.

L'API Windows dispone di molte funzioni che dispongono anche di versioni Unicode per consentire un percorso di lunghezza estesa per un percorso di lunghezza totale massimo di 32.767 caratteri. Questo tipo di percorso è costituito da componenti separati da barre rovesciate, ciascuno fino al valore restituito nel parametro *lpMaximumComponentLength* della funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) (questo valore è in genere di 255 caratteri). Per specificare un percorso di lunghezza estesa, usare il \\ \\ prefisso "? \\ ". Ad esempio, " \\ \\ ? \\ D: \\ *percorso molto lungo*".

> [!Note]  
> Il percorso massimo di 32.767 caratteri è approssimativo, perché il \\ \\ prefisso "? \\ " può essere espanso a una stringa più lunga dal sistema in fase di esecuzione e questa espansione viene applicata alla lunghezza totale.

Il \\ \\ prefisso "? \\ " può essere utilizzato anche con i percorsi costruiti in base alla convenzione UNC (Universal Naming Convention). Per specificare tale percorso utilizzando UNC, utilizzare il valore " \\ \\ ? \\ \\Prefisso UNC ". Ad esempio, " \\ \\ ? \\ \\Condivisione server UNC \\ ", dove" Server "è il nome del computer e" Share "è il nome della cartella condivisa. Questi prefissi non vengono usati come parte del percorso. Indica che il percorso deve essere passato al sistema con una modifica minima, il che significa che non è possibile usare le barre per rappresentare i separatori di percorso o un punto per rappresentare la directory corrente o i punti doppi per rappresentare la directory padre. Poiché non è possibile usare il \\ \\ prefisso "? \\ " con un percorso relativo, i percorsi relativi sono sempre limitati a un totale di caratteri di **\_ percorso massimi** .

Non è necessario eseguire alcuna normalizzazione Unicode per le stringhe di percorso e nome file per l'uso da parte delle funzioni API di I/O dei file di Windows, perché il file system considera i nomi di percorso e file come una sequenza opaca di **WCHAR** s. Qualsiasi normalizzazione necessaria per l'applicazione deve essere eseguita tenendo presente questo aspetto, esterno alle chiamate alle funzioni API I/O dei file di Windows correlate.

Quando si usa un'API per creare una directory, il percorso specificato non può essere così lungo che non è possibile aggiungere un nome file 8,3 (ovvero, il nome della directory non può superare il **\_ percorso massimo** meno 12).

La shell e la file system hanno requisiti diversi. È possibile creare un percorso con l'API Windows che l'interfaccia utente della shell non è in grado di interpretare correttamente.

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>Abilita percorsi lunghi in Windows 10, versione 1607 e successive

A partire da Windows 10, versione 1607, le limitazioni del **\_ percorso massimo** sono state rimosse dalle funzioni comuni di file e directory Win32. Tuttavia, è necessario acconsentire esplicitamente al nuovo comportamento.

Per abilitare il nuovo comportamento del percorso lungo, è necessario che siano soddisfatte entrambe le condizioni seguenti:

* La chiave del registro `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` di sistema deve esistere e deve essere impostata su 1. Il valore della chiave verrà memorizzato nella cache dal sistema (per processo) dopo la prima chiamata a una funzione di directory o a un file Win32 interessato (vedere di seguito per l'elenco di funzioni). La chiave del registro di sistema non verrà ricaricata durante il ciclo di vita del processo. Affinché tutte le app del sistema riconoscano il valore della chiave, potrebbe essere necessario riavviare il sistema perché alcuni processi potrebbero essere stati avviati prima dell'impostazione della chiave.

È anche possibile copiare questo codice in un `.reg` file che può essere impostato per l'utente:
```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

    > [!NOTE]  
    > This registry key can also be controlled via Group Policy at `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths`.

* Il [manifesto dell'applicazione](../sbscs/application-manifests.md) deve includere anche l' `longPathAware` elemento.

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

Queste sono le funzioni di gestione della directory che non hanno più restrizioni di **\_ percorso massime** se si sceglie il comportamento di percorso lungo: CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.

Queste sono le funzioni di gestione dei file che non hanno più restrizioni del **\_ percorso massimo** se si sceglie il comportamento del percorso lungo: CopyFileW, CopyFile2, CopyFileExW, CreateFileW, CreateFile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW, FindFirstStreamW, FindNextStreamW, GetCompressedFileSizeW, GetFinalPathNameByHandleW.
