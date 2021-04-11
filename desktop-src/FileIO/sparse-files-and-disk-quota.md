---
description: Un file sparse influiscono sulle quote utente in base alle dimensioni nominali del file, non alla quantità effettiva di spazio su disco allocata.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: File sparse e quote disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129758"
---
# <a name="sparse-files-and-disk-quotas"></a><span data-ttu-id="b8f4e-103">File sparse e quote disco</span><span class="sxs-lookup"><span data-stu-id="b8f4e-103">Sparse Files and Disk Quotas</span></span>

<span data-ttu-id="b8f4e-104">Un file sparse influiscono sulle quote utente in base alle dimensioni nominali del file, non alla quantità effettiva di spazio su disco allocata.</span><span class="sxs-lookup"><span data-stu-id="b8f4e-104">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span> <span data-ttu-id="b8f4e-105">Ovvero la creazione di un file di 50 MB con tutti i byte zero utilizza 50 MB della quota di tale utente.</span><span class="sxs-lookup"><span data-stu-id="b8f4e-105">That is, creating a 50-MB file with all zero bytes consumes 50 MB of that user's quota.</span></span> <span data-ttu-id="b8f4e-106">Ciò significa che quando l'utente scrive i dati nel file sparse, non è necessario preoccuparsi del superamento del limite di quota hardware perché è già stato addebitato per lo spazio.</span><span class="sxs-lookup"><span data-stu-id="b8f4e-106">This means that as the user writes data to the sparse file, he need not worry about exceeding his hard quota limit, because he has already been charged for the space.</span></span> <span data-ttu-id="b8f4e-107">Gli amministratori di sistema non devono contare sulle dimensioni di un file sparse che rimane ridotto.</span><span class="sxs-lookup"><span data-stu-id="b8f4e-107">System administrators should not count on the size of a sparse file remaining small.</span></span> <span data-ttu-id="b8f4e-108">Non devono quindi concedere ai propri utenti limiti di quota rigidi che superano lo spazio fisico disponibile, nonostante l'uso di file sparse.</span><span class="sxs-lookup"><span data-stu-id="b8f4e-108">Therefore they should not grant their users hard quota limits that exceed the physical space available, despite the use of sparse files.</span></span>

 

 



