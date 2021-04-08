---
title: Ridistribuzione di Windows Media Player 9 Series
description: Ridistribuzione di Windows Media Player 9 Series
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045257"
---
# <a name="redistributing-windows-media-player-9-series"></a><span data-ttu-id="0c594-103">Ridistribuzione di Windows Media Player 9 Series</span><span class="sxs-lookup"><span data-stu-id="0c594-103">Redistributing Windows Media Player 9 Series</span></span>

<span data-ttu-id="0c594-104">È possibile installare la serie Windows Media Player 9 in Windows XP utilizzando uno dei seguenti programmi di installazione.</span><span class="sxs-lookup"><span data-stu-id="0c594-104">You can install Windows Media Player 9 Series on Windows XP by using one of the following setup programs.</span></span>

-   <span data-ttu-id="0c594-105">MPSetupXP.exe</span><span class="sxs-lookup"><span data-stu-id="0c594-105">MPSetupXP.exe</span></span>
-   <span data-ttu-id="0c594-106">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="0c594-106">MPSetup.exe</span></span>

> [!Note]  
> <span data-ttu-id="0c594-107">MPSetup.exe è un superset del programma di installazione di MPSetupXP.exe.</span><span class="sxs-lookup"><span data-stu-id="0c594-107">MPSetup.exe is a superset of the MPSetupXP.exe setup program.</span></span> <span data-ttu-id="0c594-108">Contiene i file necessari per i sistemi operativi rilasciati prima di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0c594-108">It contains files that are needed by operating systems released before Windows XP.</span></span> <span data-ttu-id="0c594-109">MPSetup.exe è equivalente dal punto di vista funzionale al MPSetupXP.exe quando viene eseguito in Windows XP, ma le dimensioni del file del programma di installazione sono maggiori perché non sono state ottimizzate per l'installazione nei sistemi operativi Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0c594-109">MPSetup.exe is functionally equivalent to MPSetupXP.exe when run on Windows XP, but the setup program file size is larger because it has not been optimized for installation on Windows XP operating systems.</span></span>

 

<span data-ttu-id="0c594-110">È possibile installare la serie Windows Media Player 9 in Windows 98 Second Edition, Windows Millennium Edition o Windows 2000 usando il programma di installazione seguente.</span><span class="sxs-lookup"><span data-stu-id="0c594-110">You can install Windows Media Player 9 Series on Windows 98 Second Edition, Windows Millennium Edition or Windows 2000 by using the following setup program.</span></span>

-   <span data-ttu-id="0c594-111">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="0c594-111">MPSetup.exe</span></span>

<span data-ttu-id="0c594-112">Di seguito è riportato un esempio di una riga di comando per l'installazione senza interfaccia utente e nessuna richiesta di riavvio o riavvio.</span><span class="sxs-lookup"><span data-stu-id="0c594-112">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> <span data-ttu-id="0c594-113">Il parametro/P: \# e specifica che il pacchetto di installazione di windows media Player deve essere memorizzato nella cache durante l'installazione di windows media player.</span><span class="sxs-lookup"><span data-stu-id="0c594-113">The /P:\#e parameter specifies that the Windows Media Player installation package should be cached during Windows Media Player setup.</span></span> <span data-ttu-id="0c594-114">Questo comando viene utilizzato per gestire gli aggiornamenti futuri del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0c594-114">This command is used to handle future upgrades of the operating system.</span></span> <span data-ttu-id="0c594-115">Questo comando deve essere omesso solo dagli amministratori IT aziendali.</span><span class="sxs-lookup"><span data-stu-id="0c594-115">This command should be omitted only by corporate IT administrators.</span></span> <span data-ttu-id="0c594-116">L'unico caso in cui/P: \# e non deve essere incluso nella riga di comando è quando si è proprietari del sistema di destinazione e si sa che il sistema di destinazione non verrà mai aggiornato a un sistema operativo successivo.</span><span class="sxs-lookup"><span data-stu-id="0c594-116">The only case where /P:\#e should not be included on the command line is when you own the target system and know that the target system will never be upgraded to a later operating system.</span></span> <span data-ttu-id="0c594-117">Se ad esempio si installa la serie Windows Media Player 9 in Windows 2000 e il computer potrebbe essere aggiornato a Windows XP, è necessario utilizzare/P: \# e nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="0c594-117">For example, if you are installing Windows Media Player 9 Series on Windows 2000 and the computer may someday be upgraded to Windows XP, you must use /P:\#e on the command line.</span></span> <span data-ttu-id="0c594-118">In caso contrario, dopo l'installazione di Windows XP, i file di Windows Media Player verranno sovrascritti con i file per Windows Media Player per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0c594-118">Otherwise, after the Windows XP installation, the Windows Media Player files will be overwritten with the files for Windows Media Player for Windows XP.</span></span>

 

<span data-ttu-id="0c594-119">La tabella seguente illustra i parametri aggiuntivi che è possibile usare con il programma di installazione della serie Windows Media Player 9.</span><span class="sxs-lookup"><span data-stu-id="0c594-119">The following table shows additional parameters that you can use with the Windows Media Player 9 Series setup program.</span></span>



| <span data-ttu-id="0c594-120">Parametro</span><span class="sxs-lookup"><span data-stu-id="0c594-120">Parameter</span></span>              | <span data-ttu-id="0c594-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c594-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c594-122">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="0c594-122">/NoMigrate</span></span>             | <span data-ttu-id="0c594-123">Impedisci la migrazione della libreria.</span><span class="sxs-lookup"><span data-stu-id="0c594-123">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="0c594-124">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="0c594-124">/NestedRestore</span></span>         | <span data-ttu-id="0c594-125">Creare un punto di ripristino del sistema annidato.</span><span class="sxs-lookup"><span data-stu-id="0c594-125">Create a nested system restore point.</span></span> <span data-ttu-id="0c594-126">Usare questa istruzione se l'applicazione crea un punto di ripristino del sistema per annidare il punto di ripristino di Windows Media Player all'interno del punto di ripristino dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c594-126">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0c594-127">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="0c594-127">/DisallowSystemRestore</span></span> | <span data-ttu-id="0c594-128">Impedisce la creazione di un punto di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="0c594-128">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="0c594-129">Questo flag Disabilita la creazione di un punto di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="0c594-129">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="0c594-130">Nella maggior parte dei casi non è consigliabile usare questo flag per la ridistribuzione generale del software.</span><span class="sxs-lookup"><span data-stu-id="0c594-130">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="0c594-131">Questa operazione deve essere utilizzata solo quando è possibile effettuare una scelta esplicita per conto dell'utente finale per non supportare il rollback dei file di Media Player Windows a una versione precedente del lettore.</span><span class="sxs-lookup"><span data-stu-id="0c594-131">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="0c594-132">Questo flag deve essere usato solo per la distribuzione aziendale o l'installazione OEM (Original Equipment Manufacturer).</span><span class="sxs-lookup"><span data-stu-id="0c594-132">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |



 

## <a name="notes"></a><span data-ttu-id="0c594-133">Note</span><span class="sxs-lookup"><span data-stu-id="0c594-133">Notes</span></span>

-   <span data-ttu-id="0c594-134">I parametri della riga di comando distinguono tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0c594-134">The command-line parameters are case-sensitive.</span></span>
-   <span data-ttu-id="0c594-135">Quando si disattiva la richiesta di riavvio, è necessario controllare la chiave del registro di sistema InstallResult e gestire la notifica di riavvio nell'applicazione di installazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="0c594-135">When suppressing the restart prompt, you must check the InstallResult registry key and handle restart notification in the calling setup application.</span></span>
-   <span data-ttu-id="0c594-136">La serie Windows Media Player 9 installa anche il runtime di Windows Media Format, pertanto non è necessario includere il pacchetto di distribuzione di Windows Media Player e il pacchetto di distribuzione di runtime di Windows Media Format nello stesso pacchetto di ridistribuzione software.</span><span class="sxs-lookup"><span data-stu-id="0c594-136">Windows Media Player 9 Series also installs the Windows Media Format runtime, so there is no need to include both the Windows Media Player distribution package and the Windows Media Format runtime distribution package in the same software redistribution package.</span></span> <span data-ttu-id="0c594-137">Se pertanto si includono MPSetup.exe o MPSetupXP.exe nell'installazione di, non è necessario includere WMFdist.exe.</span><span class="sxs-lookup"><span data-stu-id="0c594-137">Therefore, if you include MPSetup.exe or MPSetupXP.exe in your installation, you do not need to include WMFdist.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c594-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c594-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c594-139">**Ridistribuzione del software Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="0c594-139">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




