---
description: Se l'azione InstallValidate rileva l'installazione di un file in uso, viene visualizzata la finestra di dialogo filesinus e vengono registrate le informazioni seguenti.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Registrazione delle richieste di riavvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530234"
---
# <a name="logging-of-reboot-requests"></a><span data-ttu-id="db7ee-103">Registrazione delle richieste di riavvio</span><span class="sxs-lookup"><span data-stu-id="db7ee-103">Logging of Reboot Requests</span></span>

<span data-ttu-id="db7ee-104">Se l' [azione InstallValidate](installvalidate-action.md) rileva l'installazione di un file in uso, viene visualizzata la [finestra di dialogo filesinus](filesinuse-dialog.md) e vengono registrate le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="db7ee-104">If the [InstallValidate action](installvalidate-action.md) detects the installation of a file in use it displays the [FilesInUse Dialog](filesinuse-dialog.md) and logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

<span data-ttu-id="db7ee-105">Se il programma di installazione rileva che sta per sovrascrivere un file in uso, registra le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="db7ee-105">If the installer detects that it is about to overwrite a file that is in use, it logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

<span data-ttu-id="db7ee-106">Il \[ token del nome file \] può effettivamente contenere un percorso di un file con estensione RBF.</span><span class="sxs-lookup"><span data-stu-id="db7ee-106">The \[filename\] token may actually contain a path to a file with an .rbf extension.</span></span> <span data-ttu-id="db7ee-107">In questo caso il file con estensione RBF è effettivamente il file originale registrato dal messaggio 1603 che è stato rinominato nel file. RBF.</span><span class="sxs-lookup"><span data-stu-id="db7ee-107">In this case the .rbf file is actually the original file logged by the 1603 message which has been renamed to the .rbf file.</span></span> <span data-ttu-id="db7ee-108">Il file in uso viene innanzitutto rinominato con estensione RBF, quindi viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="db7ee-108">The file that's in use is first renamed with an .rbf extension and then deleted.</span></span>

<span data-ttu-id="db7ee-109">Per ottenere ulteriori informazioni sui motivi per cui il programma di installazione tenta di sovrascrivere il file specifico, è possibile utilizzare l'opzione di registrazione dettagliata.</span><span class="sxs-lookup"><span data-stu-id="db7ee-109">To obtain more information about why the installer is attempting to overwrite this particular file, you can use the verbose logging option.</span></span> <span data-ttu-id="db7ee-110">Usare il \_ valore dettagliato INSTALLLOGMODE in una chiamata a [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) o usare l'opzione output dettagliato delle opzioni della [riga di comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="db7ee-110">Use the INSTALLLOGMODE\_VERBOSE value in a call to [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) or use the verbose output option of the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="db7ee-111">Vengono registrate le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="db7ee-111">This logs the following information.</span></span>

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

<span data-ttu-id="db7ee-112">Il log includerà un messaggio come "il file esistente è una versione più bassa" o "file esistente danneggiato (checksum non valido)"</span><span class="sxs-lookup"><span data-stu-id="db7ee-112">The log will include a message such as "Existing file is a lower version" or "Existing file is corrupt (invalid checksum)"</span></span>

 

 



