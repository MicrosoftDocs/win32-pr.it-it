---
description: Come ottenere maggiore spazio libero su disco dopo il superamento della quota di quote.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Amministrazione a livello di utente di quote disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316761"
---
# <a name="user-level-administration-of-disk-quotas"></a><span data-ttu-id="18b3e-103">Amministrazione a livello di utente di quote disco</span><span class="sxs-lookup"><span data-stu-id="18b3e-103">User-level Administration of Disk Quotas</span></span>

<span data-ttu-id="18b3e-104">Le quote disco sono trasparenti per l'utente.</span><span class="sxs-lookup"><span data-stu-id="18b3e-104">Disk quotas are transparent to the user.</span></span> <span data-ttu-id="18b3e-105">Quando un utente chiede la quantità di spazio disponibile su un disco, il sistema segnala solo la quota disponibile disponibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="18b3e-105">When a user asks how much space is free on a disk, the system reports only the available quota allowance the user has available.</span></span> <span data-ttu-id="18b3e-106">Se l'utente supera questo limite, il sistema restituisce l' **errore \_ \_ completo del disco di errore** , come per indicare che il disco è pieno.</span><span class="sxs-lookup"><span data-stu-id="18b3e-106">If the user exceeds this allowance, the system returns the **ERROR\_DISK\_FULL** error, just as it would to indicate that the disk was full.</span></span>

<span data-ttu-id="18b3e-107">Per ottenere maggiore spazio su disco dopo il superamento della quota di quote, l'utente deve eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="18b3e-107">To obtain more free disk space after exceeding the quota allowance, the user must do one of the following:</span></span>

-   <span data-ttu-id="18b3e-108">Eliminare alcuni file.</span><span class="sxs-lookup"><span data-stu-id="18b3e-108">Delete some files.</span></span>
-   <span data-ttu-id="18b3e-109">Chiedere a un altro utente di ottenere la proprietà di alcuni file.</span><span class="sxs-lookup"><span data-stu-id="18b3e-109">Have another user claim ownership of some files.</span></span>
-   <span data-ttu-id="18b3e-110">Chiedere all'amministratore di aumentare la quota di quote.</span><span class="sxs-lookup"><span data-stu-id="18b3e-110">Have the administrator increase the quota allowance.</span></span>

<span data-ttu-id="18b3e-111">I programmi che devono recuperare la quantità effettiva di spazio libero su disco possono chiamare la funzione [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) ed esaminare il parametro *TotalNumberOfFreeBytes* .</span><span class="sxs-lookup"><span data-stu-id="18b3e-111">Programs that need to retrieve the actual amount of free disk space can call the [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) function and look at the *TotalNumberOfFreeBytes* parameter.</span></span>

 

 



