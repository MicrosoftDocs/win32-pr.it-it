---
title: Registro di sistema di monitoraggio delle Impostazioni
description: Registro di sistema di monitoraggio delle Impostazioni
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player,impostazioni del Registro di sistema per il monitoraggio delle cartelle
- Windows Media Player, impostazioni del Registro di sistema per il monitoraggio delle cartelle file
- Windows Media Player,Registro di sistema
- Registro di sistema, impostazioni di monitoraggio delle cartelle
- Registro di sistema, impostazioni di monitoraggio delle cartelle file
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del Registro di sistema per il monitoraggio delle cartelle
- Impostazioni del Registro di sistema per il monitoraggio delle cartelle file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3e5e99c633c58a68b3579c55d38e6ad5b2415d9faac8d6c3438251c5a83459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748442"
---
# <a name="folder-monitoring-registry-settings"></a>Registro di sistema di monitoraggio delle Impostazioni

Windows Media Player serie 9 o successiva è in grado di monitorare le cartelle file per i nuovi file multimediali digitali. Quando il lettore rileva un nuovo file in una cartella monitorata, aggiunge automaticamente il file alla libreria. Per Windows Media Player da 9 Windows Media Player 11, gli utenti possono modificare l'elenco delle cartelle monitorate  facendo clic su **Monitora** cartelle nella scheda Raccolta della finestra di dialogo Opzioni. Per Windows Media Player 12, un utente può modificare l'elenco delle cartelle [monitorate](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library)seguendo le istruzioni nell'argomento Aggiungere elementi alla libreria Windows Media Player . Per Windows Media Player da 9 a Windows Media Player 11, è possibile aggiungere a livello di codice una cartella da monitorare aggiungendo un valore al Registro di sistema. Per Windows Media Player 12, non è possibile usare il Registro di sistema per aggiungere o rimuovere cartelle da monitorare a livello di codice.

Per Windows Media Player da 9 a Windows Media Player 11, per aggiungere una cartella per il monitoraggio è prima necessario creare o modificare due valori nella chiave del Registro di sistema seguente:

**HKEY \_ CURRENT USER Software Preferenze di Microsoft \_ \\ \\ \\ MediaPlayer \\\\**

I nuovi valori devono essere denominati come indicato di seguito.



| Nome                           | Tipo           | Descrizione                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TrackFoldersDirectories**    | **REG \_ DWORD** | Valore **DWORD** che rappresenta il numero di cartelle da monitorare. Deve corrispondere al numero di **valori TrackFoldersDirectories**_X._                                                                                                                                         |
| **TrackFoldersDirectories**_X_ | **REG \_ SZ**    | Valore stringa che rappresenta il percorso della cartella da monitorare. Ogni cartella da monitorare richiede un valore separato. Il *suffisso X* è un numero intero che deve sempre iniziare da 0 e quindi incrementare di 1. Windows Media Player monitora anche le sottocartelle della cartella specificata. |



 

Ad esempio, per aggiungere la prima cartella da monitorare, aggiungere il valore seguente:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



Creare quindi il valore di conteggio:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



Per aggiungere una seconda cartella da monitorare, aggiungere il valore seguente:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



Incrementare quindi il valore del conteggio:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Registro di Impostazioni**](registry-settings.md)
</dt> </dl>

 

 




