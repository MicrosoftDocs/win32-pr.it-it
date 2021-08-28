---
description: Limitazione massima della lunghezza del percorso.
title: Limitazione della lunghezza massima del percorso
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: f57aba8d022e3b193289c8abf884e661797a0cf8585b7537fae19c171250eb12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914761"
---
# <a name="maximum-path-length-limitation"></a>Limitazione della lunghezza massima del percorso

Nell'API Windows (con alcune eccezioni descritte nei paragrafi seguenti), la lunghezza massima per un percorso è **MAX \_ PATH,** definita come 260 caratteri. Un percorso locale è strutturato nell'ordine seguente: lettera di unità, due punti, barra rovesciata, nome di componenti separati da barre rovesciate e un carattere Null di terminazione. Ad esempio, il percorso massimo nell'unità D è "D: \\ *some 256-character path string* &lt; NUL " where " &gt; &lt; NUL " represents the invisible &gt; terminating null character for the current system codepage. I caratteri < > vengono usati qui per maggiore chiarezza visiva e non possono far parte di una stringa di percorso valida.

Ad esempio, è possibile che questa limitazione venga raggiunto se si clona un repository Git con nomi di file lunghi in una cartella con un nome lungo.


> [!Note]  
> Le funzioni di I/O di file nell'API Windows convertono "/" in " " come parte della conversione del nome in un nome di tipo NT, tranne quando si usa il prefisso " ? ", come descritto in dettaglio nelle \\ \\ \\ \\ sezioni seguenti.

L Windows API include molte funzioni che dispongono anche di versioni Unicode per consentire un percorso di lunghezza estesa per una lunghezza totale massima di 32.767 caratteri. Questo tipo di percorso è costituito da componenti separati da barre rovesciate, ognuno fino al valore restituito nel parametro *lpMaximumComponentLength* della funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) (questo valore è in genere di 255 caratteri). Per specificare un percorso di lunghezza estesa, usare il prefisso " \\ \\ ? \\ ". Ad esempio, " \\ \\ ? \\ D: \\ *percorso molto lungo*".

> [!Note]  
> Il percorso massimo di 32.767 caratteri è approssimativo, perché il prefisso " ? " può essere espanso in una stringa più lunga dal sistema in fase di esecuzione e questa espansione si applica alla lunghezza \\ \\ \\ totale.

Il prefisso " \\ \\ ? " può essere usato anche con \\ percorsi costruiti in base alla convenzione di denominazione universale (UNC). Per specificare un percorso di questo tipo tramite UNC, usare " \\ \\ ? \\ Prefisso UNC \\ ". Ad esempio, " \\ \\ ? \\ CONDIVISIONE \\ SERVER \\ UNC", dove "server" è il nome del computer e "condivisione" è il nome della cartella condivisa. Questi prefissi non vengono usati come parte del percorso stesso. Indicano che il percorso deve essere passato al sistema con modifiche minime, ovvero non è possibile usare barre per rappresentare i separatori di percorso o un punto per rappresentare la directory corrente oppure doppi punti per rappresentare la directory padre. Poiché non è possibile usare il prefisso " ? " con un percorso relativo, i percorsi relativi sono sempre limitati a un totale \\ \\ di caratteri MAX \\ **\_ PATH.**

Non è necessario eseguire alcuna normalizzazione Unicode sulle stringhe di percorso e nome file per l'uso da parte delle funzioni API di I/O di file Windows perché il file system considera i nomi di percorso e file come una sequenza opaca di **WCHAR.** Qualsiasi normalizzazione richiesta dall'applicazione deve essere eseguita in questo modo, all'esterno di qualsiasi chiamata alle funzioni api di I/O Windows file correlate.

Quando si usa un'API per creare una directory, il percorso specificato non può essere così lungo che non è possibile aggiungere un nome di file 8.3, ovvero il nome della directory non può superare **MAX \_ PATH** meno 12.

La shell e la file system hanno requisiti diversi. È possibile creare un percorso con l'API Windows che l'interfaccia utente della shell non è in grado di interpretare correttamente.

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>Abilitare percorsi lunghi in Windows 10, versione 1607 e successive

A partire Windows 10 versione 1607, le limitazioni **MAX \_ PATH** sono state rimosse dalle funzioni comuni di file e directory Win32. Tuttavia, è necessario acconsentire esplicitamente al nuovo comportamento.

Per abilitare il nuovo comportamento del percorso lungo, è necessario che siano soddisfatte entrambe le condizioni seguenti:

* La chiave del `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` Registro di sistema deve esistere e deve essere impostata su 1. Il valore della chiave verrà memorizzato nella cache dal sistema (per processo) dopo la prima chiamata a una funzione di directory o file Win32 interessata (vedere di seguito per l'elenco di funzioni). La chiave del Registro di sistema non verrà ricaricata durante la durata del processo. Per consentire a tutte le app nel sistema di riconoscere il valore della chiave, potrebbe essere necessario un riavvio perché alcuni processi potrebbero essere stati avviati prima dell'impostazione della chiave.

È anche possibile copiare questo codice in un file che può impostarlo automaticamente oppure usare il comando di PowerShell da una finestra del terminale con `.reg` privilegi elevati:
# <a name="cmd"></a>[cmd](#tab/cmd)

```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

# <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" `
-Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force

```

---

> [!NOTE]  
> Questa chiave del Registro di sistema può essere controllata anche tramite Criteri di gruppo all'indirizzo `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` .

* Il [manifesto dell'applicazione](../sbscs/application-manifests.md) deve includere anche l'elemento `longPathAware` .

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

Queste sono le funzioni di gestione della directory che non hanno più restrizioni **MAX \_ PATH** se si acconsente esplicitamente al comportamento del percorso lungo: CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.

Queste sono le funzioni di gestione dei file che non hanno più restrizioni **MAX \_ PATH** se si acconsente esplicitamente al comportamento del percorso lungo: CopyFileW, CopyFile2, CopyFileExW, CreateFileW, CreateFile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW, FindFirstStreamW, FindNextStreamW, GetCompressedFileSizeW, GetFinalPathNameByHandleW.
