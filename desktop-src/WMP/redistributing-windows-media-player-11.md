---
title: Ridistribuzione di Windows Media Player 11
description: Ridistribuzione di Windows Media Player 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044488"
---
# <a name="redistributing-windows-media-player-11"></a><span data-ttu-id="fc1fb-103">Ridistribuzione di Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="fc1fb-103">Redistributing Windows Media Player 11</span></span>

<span data-ttu-id="fc1fb-104">È possibile installare Windows Media Player 11 in Windows XP utilizzando uno dei seguenti programmi di installazione, in cui *LocaleID* è un identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-104">You can install Windows Media Player 11 on Windows XP by using one of the following setup programs, where *localeId* is a locale identifier.</span></span>

-   <span data-ttu-id="fc1fb-105">wmp11-windowsxp-x86-*LocaleID*. exe</span><span class="sxs-lookup"><span data-stu-id="fc1fb-105">wmp11-windowsxp-x86-*localeId*.exe</span></span>
-   <span data-ttu-id="fc1fb-106">WMP11-WindowsXP-x64-*LocaleID*. exe</span><span class="sxs-lookup"><span data-stu-id="fc1fb-106">wmp11-windowsxp-x64-*localeId*.exe</span></span>

<span data-ttu-id="fc1fb-107">Di seguito è riportato un esempio di una riga di comando per l'installazione senza interfaccia utente e nessuna richiesta di riavvio o riavvio.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-107">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="fc1fb-108">La tabella seguente illustra i parametri aggiuntivi che è possibile usare con il programma di installazione di Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-108">The following table shows additional parameters that you can use with the Windows Media Player 11 setup program.</span></span>



| <span data-ttu-id="fc1fb-109">Parametro</span><span class="sxs-lookup"><span data-stu-id="fc1fb-109">Parameter</span></span>              | <span data-ttu-id="fc1fb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc1fb-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1fb-111">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="fc1fb-111">/NoMigrate</span></span>             | <span data-ttu-id="fc1fb-112">Impedisci la migrazione della libreria.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-112">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="fc1fb-113">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="fc1fb-113">/NestedRestore</span></span>         | <span data-ttu-id="fc1fb-114">Creare un punto di ripristino del sistema annidato.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-114">Create a nested system restore point.</span></span> <span data-ttu-id="fc1fb-115">Usare questa istruzione se l'applicazione crea un punto di ripristino del sistema per annidare il punto di ripristino di Windows Media Player all'interno del punto di ripristino dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-115">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="fc1fb-116">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="fc1fb-116">/DisallowSystemRestore</span></span> | <span data-ttu-id="fc1fb-117">Impedisce la creazione di un punto di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-117">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="fc1fb-118">Questo flag Disabilita la creazione di un punto di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-118">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="fc1fb-119">Nella maggior parte dei casi non è consigliabile usare questo flag per la ridistribuzione generale del software.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-119">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="fc1fb-120">Questa operazione deve essere utilizzata solo quando è possibile effettuare una scelta esplicita per conto dell'utente finale per non supportare il rollback dei file di Media Player Windows a una versione precedente del lettore.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-120">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="fc1fb-121">Questo flag deve essere usato solo per la distribuzione aziendale o l'installazione OEM (Original Equipment Manufacturer).</span><span class="sxs-lookup"><span data-stu-id="fc1fb-121">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="fc1fb-122">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="fc1fb-122">/DefaultService</span></span>        | <span data-ttu-id="fc1fb-123">Impostare l'archivio online iniziale.</span><span class="sxs-lookup"><span data-stu-id="fc1fb-123">Set the initial online store.</span></span> <span data-ttu-id="fc1fb-124">Per ulteriori informazioni, vedere [impostazione dei parametri della riga di comando per i negozi online](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="fc1fb-124">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="fc1fb-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc1fb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc1fb-126">**Ridistribuzione del software Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="fc1fb-126">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




