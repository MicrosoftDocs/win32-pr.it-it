---
title: Informazioni sul file Memory-Mapped
description: Un file mappato alla memoria (o mapping di file) è il risultato dell'associazione del contenuto di un file a una parte dello spazio degli indirizzi virtuali di un processo. Può essere usato per condividere un file o una memoria tra due o più processi.
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118271"
---
# <a name="memory-mapped-file-information"></a><span data-ttu-id="bec36-104">Informazioni sul file Memory-Mapped</span><span class="sxs-lookup"><span data-stu-id="bec36-104">Memory-Mapped File Information</span></span>

<span data-ttu-id="bec36-105">Un *file mappato alla memoria* (o *mapping di file*) è il risultato dell'associazione del contenuto di un file a una parte dello spazio degli indirizzi virtuali di un processo.</span><span class="sxs-lookup"><span data-stu-id="bec36-105">A *memory-mapped file* (or *file mapping*) is the result of associating a file's contents with a portion of the virtual address space of a process.</span></span> <span data-ttu-id="bec36-106">Può essere usato per condividere un file o una memoria tra due o più processi.</span><span class="sxs-lookup"><span data-stu-id="bec36-106">It can be used to share a file or memory between two or more processes.</span></span>

<span data-ttu-id="bec36-107">La funzione [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) riceve un handle di processo e un puntatore a un indirizzo come input.</span><span class="sxs-lookup"><span data-stu-id="bec36-107">The [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) function receives a process handle and a pointer to an address as input.</span></span> <span data-ttu-id="bec36-108">Se l'indirizzo si trova all'interno di un file mappato alla memoria nello spazio degli indirizzi virtuali del processo, la funzione restituisce il nome del file mappato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="bec36-108">If the address is within a memory-mapped file in the virtual address space of the process, the function returns the name of the memory-mapped file.</span></span> <span data-ttu-id="bec36-109">I nomi di file restituiti da **GetMappedFileName** usano il modulo del dispositivo anziché le lettere di unità.</span><span class="sxs-lookup"><span data-stu-id="bec36-109">The file names returned by **GetMappedFileName** use device form, rather than drive letters.</span></span> <span data-ttu-id="bec36-110">Ad esempio, il nome del file c: \\ WinNT \\ system32 \\ . nls avrà un aspetto simile al seguente nel modulo del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="bec36-110">For example, the file name c:\\winnt\\system32\\ctype.nls would look like this in device form:</span></span>

<span data-ttu-id="bec36-111">\\Device \\ DiscoRigido0 \\ Partition1 \\ WinNT \\ system32 \\ . nls</span><span class="sxs-lookup"><span data-stu-id="bec36-111">\\Device\\Harddisk0\\Partition1\\WINNT\\System32\\ctype.nls</span></span>

<span data-ttu-id="bec36-112">Per ulteriori informazioni sui file mappati alla memoria, vedere [mapping di file](/windows/desktop/Memory/file-mapping).</span><span class="sxs-lookup"><span data-stu-id="bec36-112">For more information about memory-mapped files, see [File Mapping](/windows/desktop/Memory/file-mapping).</span></span> <span data-ttu-id="bec36-113">Per un esempio in cui i nomi di file vengono convertiti in formato dispositivo in lettere di unità, vedere [ottenere un nome di file da un handle di file](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span><span class="sxs-lookup"><span data-stu-id="bec36-113">For an example that converts file names in device form to drive letters, see [Obtaining a File Name From a File Handle](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span></span>

 

 