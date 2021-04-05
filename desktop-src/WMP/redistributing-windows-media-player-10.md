---
title: Ridistribuzione di Windows Media Player 10
description: Ridistribuzione di Windows Media Player 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707909"
---
# <a name="redistributing-windows-media-player-10"></a><span data-ttu-id="f6063-103">Ridistribuzione di Windows Media Player 10</span><span class="sxs-lookup"><span data-stu-id="f6063-103">Redistributing Windows Media Player 10</span></span>

<span data-ttu-id="f6063-104">È possibile installare Windows Media Player 10 in Windows XP utilizzando il seguente programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="f6063-104">You can install Windows Media Player 10 on Windows XP by using the following setup program.</span></span>

-   <span data-ttu-id="f6063-105">MP10Setup.exe</span><span class="sxs-lookup"><span data-stu-id="f6063-105">MP10Setup.exe</span></span>

<span data-ttu-id="f6063-106">Di seguito è riportato un esempio di una riga di comando per l'installazione senza interfaccia utente e nessuna richiesta di riavvio o riavvio.</span><span class="sxs-lookup"><span data-stu-id="f6063-106">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="f6063-107">La tabella seguente illustra i parametri aggiuntivi che è possibile usare con il programma di installazione di Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="f6063-107">The following table shows additional parameters that you can use with the Windows Media Player 10 setup program.</span></span>



| <span data-ttu-id="f6063-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="f6063-108">Parameter</span></span>              | <span data-ttu-id="f6063-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6063-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6063-110">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="f6063-110">/NoMigrate</span></span>             | <span data-ttu-id="f6063-111">Impedisci la migrazione della libreria.</span><span class="sxs-lookup"><span data-stu-id="f6063-111">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f6063-112">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="f6063-112">/NestedRestore</span></span>         | <span data-ttu-id="f6063-113">Creare un punto di ripristino del sistema annidato.</span><span class="sxs-lookup"><span data-stu-id="f6063-113">Create a nested system restore point.</span></span> <span data-ttu-id="f6063-114">Usare questa istruzione se l'applicazione crea un punto di ripristino del sistema per annidare il punto di ripristino di Windows Media Player all'interno del punto di ripristino dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6063-114">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f6063-115">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="f6063-115">/DisallowSystemRestore</span></span> | <span data-ttu-id="f6063-116">Impedisce la creazione di un punto di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="f6063-116">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="f6063-117">Questo flag Disabilita la creazione di un punto di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="f6063-117">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="f6063-118">Nella maggior parte dei casi non è consigliabile usare questo flag per la ridistribuzione generale del software.</span><span class="sxs-lookup"><span data-stu-id="f6063-118">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="f6063-119">Questa operazione deve essere utilizzata solo quando è possibile effettuare una scelta esplicita per conto dell'utente finale per non supportare il rollback dei file di Media Player Windows a una versione precedente del lettore.</span><span class="sxs-lookup"><span data-stu-id="f6063-119">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="f6063-120">Questo flag deve essere usato solo per la distribuzione aziendale o l'installazione OEM (Original Equipment Manufacturer).</span><span class="sxs-lookup"><span data-stu-id="f6063-120">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="f6063-121">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="f6063-121">/DefaultService</span></span>        | <span data-ttu-id="f6063-122">Impostare l'archivio online iniziale.</span><span class="sxs-lookup"><span data-stu-id="f6063-122">Set the initial online store.</span></span> <span data-ttu-id="f6063-123">Per ulteriori informazioni, vedere [impostazione dei parametri della riga di comando per i negozi online](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="f6063-123">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="f6063-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6063-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6063-125">**Ridistribuzione del software Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="f6063-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> <dt>

[<span data-ttu-id="f6063-126">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="f6063-126">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




