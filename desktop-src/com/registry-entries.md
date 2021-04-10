---
title: Voci del registro di sistema (COM)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 'Altre informazioni su: voci del registro di sistema (COM)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127570"
---
# <a name="registry-entries-com"></a><span data-ttu-id="bf088-103">Voci del registro di sistema (COM)</span><span class="sxs-lookup"><span data-stu-id="bf088-103">Registry Entries (COM)</span></span>

<span data-ttu-id="bf088-104">I valori del registro di sistema nelle chiavi del registro di sistema seguenti controllano gli aspetti della funzionalità di COM:</span><span class="sxs-lookup"><span data-stu-id="bf088-104">Registry values in the following registry keys control aspects of the functionality of COM:</span></span>

-   [<span data-ttu-id="bf088-105">**\_ \_ Classi software del computer locale \\ HKEY \\**</span><span class="sxs-lookup"><span data-stu-id="bf088-105">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**</span></span>](hkey-local-machine-software-classes.md)
-   [<span data-ttu-id="bf088-106">**\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE**</span><span class="sxs-lookup"><span data-stu-id="bf088-106">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Ole**</span></span>](hkey-local-machine-software-microsoft-ole.md)
-   [<span data-ttu-id="bf088-107">**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="bf088-107">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

<span data-ttu-id="bf088-108">A partire da Windows Server 2003, COM usa solo il token di processo corrente per decidere quale hive del registro di sistema accedere, non il token del thread.</span><span class="sxs-lookup"><span data-stu-id="bf088-108">As of Windows Server 2003, COM uses only the current process token to decide which registry hive to access, not the thread token.</span></span> <span data-ttu-id="bf088-109">Se COM non è in grado di accedere all'hive del registro di sistema del profilo utente, accederà a **HKEY \_ Local \_ Machine \\ System** hive.</span><span class="sxs-lookup"><span data-stu-id="bf088-109">If COM is not able to access the user profile registry hive, it will access the **HKEY\_LOCAL\_MACHINE\\System** hive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf088-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf088-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf088-111">Registro</span><span class="sxs-lookup"><span data-stu-id="bf088-111">Registry</span></span>](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
