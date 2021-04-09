---
description: In genere, le informazioni di debug vengono archiviate in un file di simboli separato dall'eseguibile.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: File di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964fbe0ab5f07a6c3d7cfa08b057550e1cc2c74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126054"
---
# <a name="symbol-files"></a><span data-ttu-id="923ec-103">File di simboli</span><span class="sxs-lookup"><span data-stu-id="923ec-103">Symbol Files</span></span>

<span data-ttu-id="923ec-104">In genere, le informazioni di debug vengono archiviate in un file di simboli separato dall'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="923ec-104">Normally, debugging information is stored in a symbol file separate from the executable.</span></span> <span data-ttu-id="923ec-105">L'implementazione di queste informazioni di debug è cambiata negli anni e la documentazione seguente fornirà indicazioni su queste diverse implementazioni.</span><span class="sxs-lookup"><span data-stu-id="923ec-105">The implementation of this debugging information has changed over the years, and the following documentation will provide guidance regarding these various implementations.</span></span>

## <a name="pdb-files"></a><span data-ttu-id="923ec-106">PDB (file)</span><span class="sxs-lookup"><span data-stu-id="923ec-106">PDB files</span></span>

<span data-ttu-id="923ec-107">Tutte le versioni moderne dei compilatori Microsoft archiviano le informazioni di debug su un eseguibile compilato in un file di *database di programma* (con estensione pdb) separato.</span><span class="sxs-lookup"><span data-stu-id="923ec-107">All modern versions of the Microsoft compilers store debugging information about a compiled executable in a separate *program database* (.pdb) file.</span></span> <span data-ttu-id="923ec-108">Questo file viene comunemente definito *PDB*.</span><span class="sxs-lookup"><span data-stu-id="923ec-108">This file is commonly referred to as a *PDB*.</span></span> <span data-ttu-id="923ec-109">I dati vengono archiviati in un file separato dall'eseguibile per limitare le dimensioni del file eseguibile, salvando lo spazio di archiviazione su disco e riducendo il tempo necessario per caricare i dati.</span><span class="sxs-lookup"><span data-stu-id="923ec-109">The data is stored in a separate file from the executable to help limit the size of the executable, saving disk storage space and reducing the time it takes to load the data.</span></span> <span data-ttu-id="923ec-110">Questa metodologia consente inoltre la distribuzione del file eseguibile senza divulgare queste informazioni significative che potrebbero rendere il programma più semplice da decodificare.</span><span class="sxs-lookup"><span data-stu-id="923ec-110">This methodology also allows the executable to be distributed without disclosing this significant information which could make the program easier to reverse engineer.</span></span>

<span data-ttu-id="923ec-111">Per creare un PDB, compilare il file eseguibile con le informazioni di debug in base alle istruzioni per gli strumenti di compilazione.</span><span class="sxs-lookup"><span data-stu-id="923ec-111">To create a PDB, build your executable file with debugging information according to the directions for your build tools.</span></span>

<span data-ttu-id="923ec-112">L'API DbgHelp è in grado di usare pdb per ottenere le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="923ec-112">The DbgHelp API is able to use PDBs to obtain the following information.</span></span>

-   <span data-ttu-id="923ec-113">pubbliche ed esportazioni</span><span class="sxs-lookup"><span data-stu-id="923ec-113">publics and exports</span></span>
-   <span data-ttu-id="923ec-114">simboli globali</span><span class="sxs-lookup"><span data-stu-id="923ec-114">global symbols</span></span>
-   <span data-ttu-id="923ec-115">simboli locali</span><span class="sxs-lookup"><span data-stu-id="923ec-115">local symbols</span></span>
-   <span data-ttu-id="923ec-116">dati di tipo</span><span class="sxs-lookup"><span data-stu-id="923ec-116">type data</span></span>
-   <span data-ttu-id="923ec-117">file di origine</span><span class="sxs-lookup"><span data-stu-id="923ec-117">source files</span></span>
-   <span data-ttu-id="923ec-118">numeri di riga</span><span class="sxs-lookup"><span data-stu-id="923ec-118">line numbers</span></span>

## <a name="dbg-files-and-embedded-debug-information"></a><span data-ttu-id="923ec-119">File DBG e informazioni di debug incorporate</span><span class="sxs-lookup"><span data-stu-id="923ec-119">DBG files and embedded debug information</span></span>

<span data-ttu-id="923ec-120">Le versioni precedenti del set di strumenti Microsoft usavano per incorporare le informazioni di debug nel file eseguibile, tuttavia verrebbero normalmente rimosse in un file separato con estensione dbg.</span><span class="sxs-lookup"><span data-stu-id="923ec-120">Previous versions of the Microsoft toolset used to embed the debugging information in the executable, however it would normally be stripped out into a separate file with a .dbg extension.</span></span> <span data-ttu-id="923ec-121">Questo è comunemente noto come file *dbg* .</span><span class="sxs-lookup"><span data-stu-id="923ec-121">This is commonly known as a *DBG* file.</span></span> <span data-ttu-id="923ec-122">I file DBG utilizzano lo stesso formato di file PE degli eseguibili.</span><span class="sxs-lookup"><span data-stu-id="923ec-122">DBG files use the same PE file format as executables.</span></span>

<span data-ttu-id="923ec-123">Il supporto dell'API DbgHelp per DBGs e informazioni di debug incorporate è limitato e include quanto segue.</span><span class="sxs-lookup"><span data-stu-id="923ec-123">The DbgHelp API support for DBGs and embedded debugging information is limited and includes the following.</span></span>

-   <span data-ttu-id="923ec-124">pubbliche ed esportazioni</span><span class="sxs-lookup"><span data-stu-id="923ec-124">publics and exports</span></span>
-   <span data-ttu-id="923ec-125">simboli globali</span><span class="sxs-lookup"><span data-stu-id="923ec-125">global symbols</span></span>

 

 



