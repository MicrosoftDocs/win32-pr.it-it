---
description: Vengono descritti i collegamenti reali e le giunzioni.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Collegamenti reali e giunzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317787"
---
# <a name="hard-links-and-junctions"></a><span data-ttu-id="1b10c-103">Collegamenti reali e giunzioni</span><span class="sxs-lookup"><span data-stu-id="1b10c-103">Hard Links and Junctions</span></span>

<span data-ttu-id="1b10c-104">Nel file system NTFS sono supportati tre tipi di collegamenti file: collegamenti reali, giunzioni e collegamenti simbolici.</span><span class="sxs-lookup"><span data-stu-id="1b10c-104">There are three types of file links supported in the NTFS file system: hard links, junctions, and symbolic links.</span></span> <span data-ttu-id="1b10c-105">Questo argomento è una panoramica dei collegamenti e delle giunzioni reali.</span><span class="sxs-lookup"><span data-stu-id="1b10c-105">This topic is an overview of hard links and junctions.</span></span> <span data-ttu-id="1b10c-106">Per informazioni sui collegamenti simbolici, vedere [creazione di collegamenti simbolici](creating-symbolic-links.md).</span><span class="sxs-lookup"><span data-stu-id="1b10c-106">For information about symbolic links, see [Creating Symbolic Links](creating-symbolic-links.md).</span></span>

## <a name="hard-links"></a><span data-ttu-id="1b10c-107">Collegamenti reali</span><span class="sxs-lookup"><span data-stu-id="1b10c-107">Hard Links</span></span>

<span data-ttu-id="1b10c-108">Un *collegamento fisso* è la rappresentazione file System di un file in base al quale più di un percorso fa riferimento a un singolo file nello stesso volume.</span><span class="sxs-lookup"><span data-stu-id="1b10c-108">A *hard link* is the file system representation of a file by which more than one path references a single file in the same volume.</span></span> <span data-ttu-id="1b10c-109">Per creare un collegamento reale, utilizzare la funzione [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) .</span><span class="sxs-lookup"><span data-stu-id="1b10c-109">To create a hard link, use the [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) function.</span></span> <span data-ttu-id="1b10c-110">Tutte le modifiche apportate al file sono immediatamente visibili alle applicazioni che vi accedono tramite i collegamenti reali che vi fanno riferimento.</span><span class="sxs-lookup"><span data-stu-id="1b10c-110">Any changes to that file are instantly visible to applications that access it through the hard links that reference it.</span></span> <span data-ttu-id="1b10c-111">Le informazioni sulle dimensioni e sugli attributi delle voci di directory vengono tuttavia aggiornate solo per il collegamento attraverso il quale è stata apportata la modifica.</span><span class="sxs-lookup"><span data-stu-id="1b10c-111">However, the directory entry size and attribute information is updated only for the link through which the change was made.</span></span> <span data-ttu-id="1b10c-112">Si noti che gli attributi del file vengono riflessi in tutti i collegamenti reali a tale file e le modifiche apportate agli attributi di tale file vengono propagate a tutti i collegamenti reali.</span><span class="sxs-lookup"><span data-stu-id="1b10c-112">Note that the attributes on the file are reflected in every hard link to that file, and changes to that file's attributes propagate to all the hard links.</span></span> <span data-ttu-id="1b10c-113">Se ad esempio si reimposta l'attributo READONLY su un collegamento reale per eliminare quel particolare collegamento e sono presenti più collegamenti reali al file effettivo, sarà necessario reimpostare il bit di sola lettura sul file da uno dei collegamenti reali rimanenti per riportare il file e tutti i collegamenti reali rimanenti allo stato di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1b10c-113">For example if you reset the READONLY attribute on a hard link to delete that particular hard link, and there are multiple hard links to the actual file, then you will need to reset the READONLY bit on the file from one of the remaining hard links to bring the file and all remaining hard links back to the READONLY state.</span></span>

<span data-ttu-id="1b10c-114">Ad esempio, in un sistema in cui C: e D: sono unità locali e Z: è un'unità di rete mappata a \\ \\ Fred \\ share, i riferimenti seguenti sono consentiti come un collegamento fisso:</span><span class="sxs-lookup"><span data-stu-id="1b10c-114">For example, in a system where C: and D: are local drives and Z: is a network drive mapped to \\\\fred\\share, the following references are permitted as a hard link:</span></span>

-   <span data-ttu-id="1b10c-115">C: \\ dira \\ethel.txt collegato a c: \\ dirB \\ DIRC \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="1b10c-115">C:\\dira\\ethel.txt linked to C:\\dirb\\dirc\\lucy.txt</span></span>
-   <span data-ttu-id="1b10c-116">D: \\ dir1 \\tinker.txt a d: \\ dir2 \\ DirX \\bell.txt</span><span class="sxs-lookup"><span data-stu-id="1b10c-116">D:\\dir1\\tinker.txt to D:\\dir2\\dirx\\bell.txt</span></span>
-   <span data-ttu-id="1b10c-117">C: \\ diry \\ Bob. bak collegato a c: \\ dir2 \\mina.txt</span><span class="sxs-lookup"><span data-stu-id="1b10c-117">C:\\diry\\bob.bak linked to C:\\dir2\\mina.txt</span></span>

<span data-ttu-id="1b10c-118">Gli elementi seguenti non sono:</span><span class="sxs-lookup"><span data-stu-id="1b10c-118">The following are not:</span></span>

-   <span data-ttu-id="1b10c-119">C: \\ dira collegato a c: \\ dirB</span><span class="sxs-lookup"><span data-stu-id="1b10c-119">C:\\dira linked to C:\\dirb</span></span>
-   <span data-ttu-id="1b10c-120">C: \\ dira \\ethel.txt collegato a D: \\ dirB \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="1b10c-120">C:\\dira\\ethel.txt linked to D:\\dirb\\lucy.txt</span></span>
-   <span data-ttu-id="1b10c-121">C: \\ dira \\ethel.txt collegato alla Z: \\ dirB \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="1b10c-121">C:\\dira\\ethel.txt linked to Z:\\dirb\\lucy.txt</span></span>

<span data-ttu-id="1b10c-122">Per eliminare un collegamento reale, utilizzare la funzione [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) .</span><span class="sxs-lookup"><span data-stu-id="1b10c-122">To delete a hard link, use the [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function.</span></span> <span data-ttu-id="1b10c-123">È possibile eliminare i collegamenti reali in qualsiasi ordine indipendentemente dall'ordine in cui vengono creati.</span><span class="sxs-lookup"><span data-stu-id="1b10c-123">You can delete hard links in any order regardless of the order in which they are created.</span></span>

## <a name="junctions"></a><span data-ttu-id="1b10c-124">Giunzioni</span><span class="sxs-lookup"><span data-stu-id="1b10c-124">Junctions</span></span>

<span data-ttu-id="1b10c-125">Una *giunzione* (anche denominata *collegamento flessibile*) differisce da un collegamento reale in quanto gli oggetti di archiviazione a cui fa riferimento sono directory separate e una giunzione può collegare le directory che si trovano in volumi locali diversi nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="1b10c-125">A *junction* (also called a *soft link*) differs from a hard link in that the storage objects it references are separate directories, and a junction can link directories located on different local volumes on the same computer.</span></span> <span data-ttu-id="1b10c-126">In caso contrario, le giunzioni operano in modo identico ai collegamenti reali.</span><span class="sxs-lookup"><span data-stu-id="1b10c-126">Otherwise, junctions operate identically to hard links.</span></span> <span data-ttu-id="1b10c-127">Le giunzioni vengono implementate tramite [reparse point](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="1b10c-127">Junctions are implemented through [reparse points](reparse-points.md).</span></span>

<span data-ttu-id="1b10c-128">Supponendo le stesse condizioni nella sezione dei collegamenti reali, i riferimenti seguenti sono consentiti come giunzioni:</span><span class="sxs-lookup"><span data-stu-id="1b10c-128">Assuming the same conditions in the Hard Links section, the following references are permitted as junctions:</span></span>

-   <span data-ttu-id="1b10c-129">C: \\ dira collegato a c: \\ dirB \\ DIRC</span><span class="sxs-lookup"><span data-stu-id="1b10c-129">C:\\dira linked to C:\\dirb\\dirc</span></span>
-   <span data-ttu-id="1b10c-130">C: \\ DirX collegato a D: \\ diry</span><span class="sxs-lookup"><span data-stu-id="1b10c-130">C:\\dirx linked to D:\\diry</span></span>

<span data-ttu-id="1b10c-131">Gli elementi seguenti non sono:</span><span class="sxs-lookup"><span data-stu-id="1b10c-131">The following are not:</span></span>

-   <span data-ttu-id="1b10c-132">C: \\ dira \\one.txt collegato a c: \\ dirB \\two.txt</span><span class="sxs-lookup"><span data-stu-id="1b10c-132">C:\\dira\\one.txt linked to C:\\dirb\\two.txt</span></span>
-   <span data-ttu-id="1b10c-133">C: \\ dir1 collegato a Z: \\ dir2</span><span class="sxs-lookup"><span data-stu-id="1b10c-133">C:\\dir1 linked to Z:\\dir2</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b10c-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b10c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b10c-135">Creazione di collegamenti simbolici</span><span class="sxs-lookup"><span data-stu-id="1b10c-135">Creating Symbolic Links</span></span>](creating-symbolic-links.md)
</dt> </dl>

 

 



