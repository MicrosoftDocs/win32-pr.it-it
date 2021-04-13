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
# <a name="folder-monitoring-registry-settings"></a><span data-ttu-id="d8b28-111">Impostazioni del registro di sistema di monitoraggio cartella</span><span class="sxs-lookup"><span data-stu-id="d8b28-111">Folder Monitoring Registry Settings</span></span>

<span data-ttu-id="d8b28-112">Windows Media Player 9 Series o versioni successive è in grado di monitorare le cartelle di file per i nuovi file multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="d8b28-112">Windows Media Player 9 Series or later can monitor file folders for new digital media files.</span></span> <span data-ttu-id="d8b28-113">Quando il giocatore rileva un nuovo file in una cartella monitorata, aggiunge automaticamente il file alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d8b28-113">When the Player detects a new file in a monitored folder, it automatically adds the file to the library.</span></span> <span data-ttu-id="d8b28-114">Per Windows Media Player 9 tramite Windows Media Player 11, gli utenti possono modificare l'elenco delle cartelle monitorate facendo clic su **monitora cartelle** nella scheda Libreria della finestra di dialogo **Opzioni** .</span><span class="sxs-lookup"><span data-stu-id="d8b28-114">For Windows Media Player 9 through Windows Media Player 11, users can change the list of monitored folders by clicking **Monitor Folders** on the library tab of the **Options** dialog box.</span></span> <span data-ttu-id="d8b28-115">Per Windows Media Player 12, un utente può modificare l'elenco delle cartelle monitorate seguendo le istruzioni riportate nell'argomento [aggiungere elementi alla raccolta di Media Player di Windows](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span><span class="sxs-lookup"><span data-stu-id="d8b28-115">For Windows Media Player 12, a user can change the list of monitored folders by following the instructions in the topic [Add items to the Windows Media Player Library](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span></span> <span data-ttu-id="d8b28-116">Per Windows Media Player 9 tramite Windows Media Player 11, è possibile aggiungere a livello di codice una cartella da monitorare aggiungendo un valore al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d8b28-116">For Windows Media Player 9 through Windows Media Player 11, you can programmatically add a folder to be monitored by adding a value to the registry.</span></span> <span data-ttu-id="d8b28-117">Per Windows Media Player 12, non è possibile utilizzare il registro di sistema per aggiungere o rimuovere cartelle da monitorare a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="d8b28-117">For Windows Media Player 12, you cannot use the registry to programmatically add or remove folders to be monitored.</span></span>

<span data-ttu-id="d8b28-118">Per Windows Media Player 9 tramite Windows Media Player 11, per aggiungere una cartella per il monitoraggio, è necessario innanzitutto creare o modificare due valori nella seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="d8b28-118">For Windows Media Player 9 through Windows Media Player 11, to add a folder for monitoring you must first create or modify two values in the following registry key:</span></span>

<span data-ttu-id="d8b28-119">**HKEY \_ \_ software utente \\ corrente \\ \\ Preferenze Microsoft MediaPlayer \\\\**</span><span class="sxs-lookup"><span data-stu-id="d8b28-119">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Preferences\\**</span></span>

<span data-ttu-id="d8b28-120">I nuovi valori devono essere denominati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d8b28-120">The new values must be named as follows.</span></span>



| <span data-ttu-id="d8b28-121">Nome</span><span class="sxs-lookup"><span data-stu-id="d8b28-121">Name</span></span>                           | <span data-ttu-id="d8b28-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="d8b28-122">Type</span></span>           | <span data-ttu-id="d8b28-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8b28-123">Description</span></span>                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b28-124">**TrackFoldersDirectories**</span><span class="sxs-lookup"><span data-stu-id="d8b28-124">**TrackFoldersDirectories**</span></span>    | <span data-ttu-id="d8b28-125">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8b28-125">**REG\_DWORD**</span></span> | <span data-ttu-id="d8b28-126">Valore **DWORD** che rappresenta il numero di cartelle da monitorare.</span><span class="sxs-lookup"><span data-stu-id="d8b28-126">A **DWORD** value that represents the count of folders to monitor.</span></span> <span data-ttu-id="d8b28-127">Deve corrispondere al conteggio dei valori \**TrackFoldersDirectories \* \* \* X* .</span><span class="sxs-lookup"><span data-stu-id="d8b28-127">This must match the count of \**TrackFoldersDirectories\*\*\*X* values.</span></span>                                                                                                                                         |
| <span data-ttu-id="d8b28-128">\**TrackFoldersDirectories \* \* \* X*</span><span class="sxs-lookup"><span data-stu-id="d8b28-128">\**TrackFoldersDirectories\*\*\*X*</span></span> | <span data-ttu-id="d8b28-129">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="d8b28-129">**REG\_SZ**</span></span>    | <span data-ttu-id="d8b28-130">Valore stringa che rappresenta il percorso della cartella da monitorare.</span><span class="sxs-lookup"><span data-stu-id="d8b28-130">A string value that represents the path of the folder to monitor.</span></span> <span data-ttu-id="d8b28-131">Ogni cartella da monitorare richiede un valore distinto.</span><span class="sxs-lookup"><span data-stu-id="d8b28-131">Each folder to monitor requires a separate value.</span></span> <span data-ttu-id="d8b28-132">Il suffisso *X* è un numero intero che deve sempre iniziare da 0 e quindi incrementare di 1.</span><span class="sxs-lookup"><span data-stu-id="d8b28-132">The suffix *X* is an integer that should always begin at 0 and then increment by 1.</span></span> <span data-ttu-id="d8b28-133">Windows Media Player monitora inoltre le sottocartelle della cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="d8b28-133">Windows Media Player also monitors subfolders of the specified folder.</span></span> |



 

<span data-ttu-id="d8b28-134">Ad esempio, per aggiungere la prima cartella da monitorare, aggiungere il valore seguente:</span><span class="sxs-lookup"><span data-stu-id="d8b28-134">For example, to add the first folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



<span data-ttu-id="d8b28-135">Quindi, creare il valore del conteggio:</span><span class="sxs-lookup"><span data-stu-id="d8b28-135">Then, create the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



<span data-ttu-id="d8b28-136">Per aggiungere una seconda cartella da monitorare, aggiungere il valore seguente:</span><span class="sxs-lookup"><span data-stu-id="d8b28-136">To add a second folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



<span data-ttu-id="d8b28-137">Quindi, incrementare il valore del conteggio:</span><span class="sxs-lookup"><span data-stu-id="d8b28-137">Then, increment the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a><span data-ttu-id="d8b28-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8b28-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8b28-139">**Impostazioni del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="d8b28-139">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




