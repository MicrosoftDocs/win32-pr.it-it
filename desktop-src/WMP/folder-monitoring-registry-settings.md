---
title: Impostazioni del registro di sistema di monitoraggio cartella
description: Impostazioni del registro di sistema di monitoraggio cartella
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player, impostazioni del registro di sistema di monitoraggio cartelle
- Windows Media Player, monitoraggio cartella file impostazioni registro di sistema
- Windows Media Player, registro di sistema
- Registro di sistema, impostazioni di monitoraggio cartella
- Registro di sistema, impostazioni di monitoraggio cartella file
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema di monitoraggio cartella
- impostazioni del registro di sistema monitoraggio cartella file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399837"
---
# <a name="folder-monitoring-registry-settings"></a>Impostazioni del registro di sistema di monitoraggio cartella

Windows Media Player 9 Series o versioni successive è in grado di monitorare le cartelle di file per i nuovi file multimediali digitali. Quando il giocatore rileva un nuovo file in una cartella monitorata, aggiunge automaticamente il file alla raccolta. Per Windows Media Player 9 tramite Windows Media Player 11, gli utenti possono modificare l'elenco delle cartelle monitorate facendo clic su **monitora cartelle** nella scheda Libreria della finestra di dialogo **Opzioni** . Per Windows Media Player 12, un utente può modificare l'elenco delle cartelle monitorate seguendo le istruzioni riportate nell'argomento [aggiungere elementi alla raccolta di Media Player di Windows](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library). Per Windows Media Player 9 tramite Windows Media Player 11, è possibile aggiungere a livello di codice una cartella da monitorare aggiungendo un valore al registro di sistema. Per Windows Media Player 12, non è possibile utilizzare il registro di sistema per aggiungere o rimuovere cartelle da monitorare a livello di codice.

Per Windows Media Player 9 tramite Windows Media Player 11, per aggiungere una cartella per il monitoraggio, è necessario innanzitutto creare o modificare due valori nella seguente chiave del registro di sistema:

**HKEY \_ \_ software utente \\ corrente \\ \\ Preferenze Microsoft MediaPlayer \\\\**

I nuovi valori devono essere denominati come indicato di seguito.



| Nome                           | Tipo           | Descrizione                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TrackFoldersDirectories**    | **REG \_ DWORD** | Valore **DWORD** che rappresenta il numero di cartelle da monitorare. Deve corrispondere al conteggio dei valori **TrackFoldersDirectories * * * X* .                                                                                                                                         |
| **TrackFoldersDirectories * * * X* | **REG \_ SZ**    | Valore stringa che rappresenta il percorso della cartella da monitorare. Ogni cartella da monitorare richiede un valore distinto. Il suffisso *X* è un numero intero che deve sempre iniziare da 0 e quindi incrementare di 1. Windows Media Player monitora inoltre le sottocartelle della cartella specificata. |



 

Ad esempio, per aggiungere la prima cartella da monitorare, aggiungere il valore seguente:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



Quindi, creare il valore del conteggio:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



Per aggiungere una seconda cartella da monitorare, aggiungere il valore seguente:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



Quindi, incrementare il valore del conteggio:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del registro di sistema**](registry-settings.md)
</dt> </dl>

 

 




