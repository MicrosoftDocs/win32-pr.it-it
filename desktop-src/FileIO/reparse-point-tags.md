---
description: Ogni reparse point ha un Tag Identifier che consente di distinguere in modo efficiente tra i diversi tipi di punti di analisi, senza dover esaminare i dati definiti dall'utente nel reparse point.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Tag di reparse point
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315928"
---
# <a name="reparse-point-tags"></a><span data-ttu-id="e9d22-103">Tag di reparse point</span><span class="sxs-lookup"><span data-stu-id="e9d22-103">Reparse Point Tags</span></span>

<span data-ttu-id="e9d22-104">Ogni reparse point ha un Tag Identifier che consente di distinguere in modo efficiente tra i diversi tipi di punti di analisi, senza dover esaminare i dati definiti dall'utente nel reparse point.</span><span class="sxs-lookup"><span data-stu-id="e9d22-104">Each reparse point has an identifier tag so that you can efficiently differentiate between the different types of reparse points, without having to examine the user-defined data in the reparse point.</span></span> <span data-ttu-id="e9d22-105">Il sistema usa un set di tag predefiniti e un intervallo di tag riservati per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e9d22-105">The system uses a set of predefined tags and a range of tags reserved for Microsoft.</span></span> <span data-ttu-id="e9d22-106">Se si usa uno dei tag riservati quando si imposta un punto di analisi, l'operazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="e9d22-106">If you use any of the reserved tags when setting a reparse point, the operation fails.</span></span> <span data-ttu-id="e9d22-107">I tag non inclusi in questi intervalli non sono riservati e sono disponibili per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9d22-107">Tags not included in these ranges are not reserved and are available for your application.</span></span>

<span data-ttu-id="e9d22-108">Quando si imposta un reparse point, è necessario contrassegnare i dati da inserire nel punto di analisi.</span><span class="sxs-lookup"><span data-stu-id="e9d22-108">When you set a reparse point, you must tag the data to be placed in the reparse point.</span></span> <span data-ttu-id="e9d22-109">Una volta stabilita la reparse point, una nuova operazione set ha esito negativo se il tag per i nuovi dati non corrisponde al tag per i dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="e9d22-109">After the reparse point has been established, a new set operation fails if the tag for the new data does not match the tag for the existing data.</span></span> <span data-ttu-id="e9d22-110">Se i tag corrispondono, l'operazione di impostazione sovrascrive il reparse point esistente.</span><span class="sxs-lookup"><span data-stu-id="e9d22-110">If the tags match, the set operation overwrites the existing reparse point.</span></span>

<span data-ttu-id="e9d22-111">Per recuperare il tag reparse point, usare la funzione [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) .</span><span class="sxs-lookup"><span data-stu-id="e9d22-111">To retrieve the reparse point tag, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) function.</span></span> <span data-ttu-id="e9d22-112">Se il membro **dwFileAttributes** include l' **attributo \_ file \_ reparse \_ Point** , il membro **dwReserved0** specifica il reparse point.</span><span class="sxs-lookup"><span data-stu-id="e9d22-112">If the **dwFileAttributes** member includes the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute, then the **dwReserved0** member specifies the reparse point.</span></span>

## <a name="tag-contents"></a><span data-ttu-id="e9d22-113">Contenuto del tag</span><span class="sxs-lookup"><span data-stu-id="e9d22-113">Tag Contents</span></span>

<span data-ttu-id="e9d22-114">I tag di reparse vengono archiviati come valori **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e9d22-114">Reparse tags are stored as **DWORD** values.</span></span> <span data-ttu-id="e9d22-115">I bit definiscono determinati attributi, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="e9d22-115">The bits define certain attributes, as shown in the following diagram.</span></span>

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

<span data-ttu-id="e9d22-116">I 16 bit bassi determinano il tipo di reparse point.</span><span class="sxs-lookup"><span data-stu-id="e9d22-116">The low 16 bits determine the kind of reparse point.</span></span> <span data-ttu-id="e9d22-117">I 16 bit alti hanno 12 bit riservati per un uso futuro e 4 bit che indicano attributi specifici dei tag e i dati rappresentati dal punto di analisi.</span><span class="sxs-lookup"><span data-stu-id="e9d22-117">The high 16 bits have 12 bits reserved for future use and 4 bits that denote specific attributes of the tags and the data represented by the reparse point.</span></span> <span data-ttu-id="e9d22-118">Nella tabella seguente vengono descritti questi bit.</span><span class="sxs-lookup"><span data-stu-id="e9d22-118">The following table describes these bits.</span></span>



| <span data-ttu-id="e9d22-119">bit</span><span class="sxs-lookup"><span data-stu-id="e9d22-119">Bit</span></span> | <span data-ttu-id="e9d22-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9d22-120">Description</span></span>                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d22-121">M</span><span class="sxs-lookup"><span data-stu-id="e9d22-121">M</span></span>   | <span data-ttu-id="e9d22-122">Microsoft bit.</span><span class="sxs-lookup"><span data-stu-id="e9d22-122">Microsoft bit.</span></span> <span data-ttu-id="e9d22-123">Se questo bit è impostato, il tag è di proprietà di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e9d22-123">If this bit is set, the tag is owned by Microsoft.</span></span> <span data-ttu-id="e9d22-124">Tutti gli altri tag devono usare zero per questo bit.</span><span class="sxs-lookup"><span data-stu-id="e9d22-124">All other tags must use zero for this bit.</span></span> |
| <span data-ttu-id="e9d22-125">R</span><span class="sxs-lookup"><span data-stu-id="e9d22-125">R</span></span>   | <span data-ttu-id="e9d22-126">Riservati deve essere zero per tutti i tag non Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e9d22-126">Reserved; must be zero for all non-Microsoft tags.</span></span>                                                           |
| <span data-ttu-id="e9d22-127">N</span><span class="sxs-lookup"><span data-stu-id="e9d22-127">N</span></span>   | <span data-ttu-id="e9d22-128">Nome surrogato bit.</span><span class="sxs-lookup"><span data-stu-id="e9d22-128">Name surrogate bit.</span></span> <span data-ttu-id="e9d22-129">Se questo bit è impostato, il file o la directory rappresenta un'altra entità denominata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e9d22-129">If this bit is set, the file or directory represents another named entity in the system.</span></span> |



 

<span data-ttu-id="e9d22-130">Sono disponibili le macro seguenti per semplificare il test dei tag:</span><span class="sxs-lookup"><span data-stu-id="e9d22-130">The following macros exist to assist in testing tags:</span></span>

-   [<span data-ttu-id="e9d22-131">**IsReparseTagMicrosoft**</span><span class="sxs-lookup"><span data-stu-id="e9d22-131">**IsReparseTagMicrosoft**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [<span data-ttu-id="e9d22-132">**IsReparseTagNameSurrogate**</span><span class="sxs-lookup"><span data-stu-id="e9d22-132">**IsReparseTagNameSurrogate**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

<span data-ttu-id="e9d22-133">Ogni macro restituisce un valore diverso da zero se il bit associato è impostato.</span><span class="sxs-lookup"><span data-stu-id="e9d22-133">Each macro returns a nonzero value if the associated bit is set.</span></span>

<span data-ttu-id="e9d22-134">Di seguito sono riportati i valori di tag di reparse predefiniti di Microsoft; sono definiti in WinNT. h:</span><span class="sxs-lookup"><span data-stu-id="e9d22-134">The following are Microsoft's predefined reparse tag values; they are defined in WinNT.h:</span></span>

-   <span data-ttu-id="e9d22-135">**IO_REPARSE_TAG_AF_UNIX**</span><span class="sxs-lookup"><span data-stu-id="e9d22-135">**IO_REPARSE_TAG_AF_UNIX**</span></span>
-   <span data-ttu-id="e9d22-136">**IO_REPARSE_TAG_APPEXECLINK**</span><span class="sxs-lookup"><span data-stu-id="e9d22-136">**IO_REPARSE_TAG_APPEXECLINK**</span></span>
-   <span data-ttu-id="e9d22-137">**IO_REPARSE_TAG_CLOUD**</span><span class="sxs-lookup"><span data-stu-id="e9d22-137">**IO_REPARSE_TAG_CLOUD**</span></span>
-   <span data-ttu-id="e9d22-138">**IO_REPARSE_TAG_CLOUD_1**</span><span class="sxs-lookup"><span data-stu-id="e9d22-138">**IO_REPARSE_TAG_CLOUD_1**</span></span>
-   <span data-ttu-id="e9d22-139">**IO_REPARSE_TAG_CLOUD_2**</span><span class="sxs-lookup"><span data-stu-id="e9d22-139">**IO_REPARSE_TAG_CLOUD_2**</span></span>
-   <span data-ttu-id="e9d22-140">**IO_REPARSE_TAG_CLOUD_3**</span><span class="sxs-lookup"><span data-stu-id="e9d22-140">**IO_REPARSE_TAG_CLOUD_3**</span></span>
-   <span data-ttu-id="e9d22-141">**IO_REPARSE_TAG_CLOUD_4**</span><span class="sxs-lookup"><span data-stu-id="e9d22-141">**IO_REPARSE_TAG_CLOUD_4**</span></span>
-   <span data-ttu-id="e9d22-142">**IO_REPARSE_TAG_CLOUD_5**</span><span class="sxs-lookup"><span data-stu-id="e9d22-142">**IO_REPARSE_TAG_CLOUD_5**</span></span>
-   <span data-ttu-id="e9d22-143">**IO_REPARSE_TAG_CLOUD_6**</span><span class="sxs-lookup"><span data-stu-id="e9d22-143">**IO_REPARSE_TAG_CLOUD_6**</span></span>
-   <span data-ttu-id="e9d22-144">**IO_REPARSE_TAG_CLOUD_7**</span><span class="sxs-lookup"><span data-stu-id="e9d22-144">**IO_REPARSE_TAG_CLOUD_7**</span></span>
-   <span data-ttu-id="e9d22-145">**IO_REPARSE_TAG_CLOUD_8**</span><span class="sxs-lookup"><span data-stu-id="e9d22-145">**IO_REPARSE_TAG_CLOUD_8**</span></span>
-   <span data-ttu-id="e9d22-146">**IO_REPARSE_TAG_CLOUD_9**</span><span class="sxs-lookup"><span data-stu-id="e9d22-146">**IO_REPARSE_TAG_CLOUD_9**</span></span>
-   <span data-ttu-id="e9d22-147">**IO_REPARSE_TAG_CLOUD_A**</span><span class="sxs-lookup"><span data-stu-id="e9d22-147">**IO_REPARSE_TAG_CLOUD_A**</span></span>
-   <span data-ttu-id="e9d22-148">**IO_REPARSE_TAG_CLOUD_B**</span><span class="sxs-lookup"><span data-stu-id="e9d22-148">**IO_REPARSE_TAG_CLOUD_B**</span></span>
-   <span data-ttu-id="e9d22-149">**IO_REPARSE_TAG_CLOUD_C**</span><span class="sxs-lookup"><span data-stu-id="e9d22-149">**IO_REPARSE_TAG_CLOUD_C**</span></span>
-   <span data-ttu-id="e9d22-150">**IO_REPARSE_TAG_CLOUD_D**</span><span class="sxs-lookup"><span data-stu-id="e9d22-150">**IO_REPARSE_TAG_CLOUD_D**</span></span>
-   <span data-ttu-id="e9d22-151">**IO_REPARSE_TAG_CLOUD_E**</span><span class="sxs-lookup"><span data-stu-id="e9d22-151">**IO_REPARSE_TAG_CLOUD_E**</span></span>
-   <span data-ttu-id="e9d22-152">**IO_REPARSE_TAG_CLOUD_F**</span><span class="sxs-lookup"><span data-stu-id="e9d22-152">**IO_REPARSE_TAG_CLOUD_F**</span></span>
-   <span data-ttu-id="e9d22-153">**IO_REPARSE_TAG_CLOUD_MASK**</span><span class="sxs-lookup"><span data-stu-id="e9d22-153">**IO_REPARSE_TAG_CLOUD_MASK**</span></span>
-   <span data-ttu-id="e9d22-154">**IO_REPARSE_TAG_CSV**</span><span class="sxs-lookup"><span data-stu-id="e9d22-154">**IO_REPARSE_TAG_CSV**</span></span>
-   <span data-ttu-id="e9d22-155">**IO_REPARSE_TAG_DEDUP**</span><span class="sxs-lookup"><span data-stu-id="e9d22-155">**IO_REPARSE_TAG_DEDUP**</span></span>
-   <span data-ttu-id="e9d22-156">**IO_REPARSE_TAG_DFS**</span><span class="sxs-lookup"><span data-stu-id="e9d22-156">**IO_REPARSE_TAG_DFS**</span></span>
-   <span data-ttu-id="e9d22-157">**IO_REPARSE_TAG_DFSR**</span><span class="sxs-lookup"><span data-stu-id="e9d22-157">**IO_REPARSE_TAG_DFSR**</span></span>
-   <span data-ttu-id="e9d22-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span><span class="sxs-lookup"><span data-stu-id="e9d22-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span></span>
-   <span data-ttu-id="e9d22-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span><span class="sxs-lookup"><span data-stu-id="e9d22-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span></span>
-   <span data-ttu-id="e9d22-160">**IO_REPARSE_TAG_HSM**</span><span class="sxs-lookup"><span data-stu-id="e9d22-160">**IO_REPARSE_TAG_HSM**</span></span>
-   <span data-ttu-id="e9d22-161">**IO_REPARSE_TAG_HSM2**</span><span class="sxs-lookup"><span data-stu-id="e9d22-161">**IO_REPARSE_TAG_HSM2**</span></span>
-   <span data-ttu-id="e9d22-162">**IO_REPARSE_TAG_MOUNT_POINT**</span><span class="sxs-lookup"><span data-stu-id="e9d22-162">**IO_REPARSE_TAG_MOUNT_POINT**</span></span>
-   <span data-ttu-id="e9d22-163">**IO_REPARSE_TAG_NFS**</span><span class="sxs-lookup"><span data-stu-id="e9d22-163">**IO_REPARSE_TAG_NFS**</span></span>
-   <span data-ttu-id="e9d22-164">**IO_REPARSE_TAG_ONEDRIVE**</span><span class="sxs-lookup"><span data-stu-id="e9d22-164">**IO_REPARSE_TAG_ONEDRIVE**</span></span>
-   <span data-ttu-id="e9d22-165">**IO_REPARSE_TAG_PROJFS**</span><span class="sxs-lookup"><span data-stu-id="e9d22-165">**IO_REPARSE_TAG_PROJFS**</span></span>
-   <span data-ttu-id="e9d22-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="e9d22-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span></span>
-   <span data-ttu-id="e9d22-167">**IO_REPARSE_TAG_SIS**</span><span class="sxs-lookup"><span data-stu-id="e9d22-167">**IO_REPARSE_TAG_SIS**</span></span>
-   <span data-ttu-id="e9d22-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span><span class="sxs-lookup"><span data-stu-id="e9d22-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span></span>
-   <span data-ttu-id="e9d22-169">**IO_REPARSE_TAG_SYMLINK**</span><span class="sxs-lookup"><span data-stu-id="e9d22-169">**IO_REPARSE_TAG_SYMLINK**</span></span>
-   <span data-ttu-id="e9d22-170">**IO_REPARSE_TAG_UNHANDLED**</span><span class="sxs-lookup"><span data-stu-id="e9d22-170">**IO_REPARSE_TAG_UNHANDLED**</span></span>
-   <span data-ttu-id="e9d22-171">**IO_REPARSE_TAG_WCI**</span><span class="sxs-lookup"><span data-stu-id="e9d22-171">**IO_REPARSE_TAG_WCI**</span></span>
-   <span data-ttu-id="e9d22-172">**IO_REPARSE_TAG_WCI_1**</span><span class="sxs-lookup"><span data-stu-id="e9d22-172">**IO_REPARSE_TAG_WCI_1**</span></span>
-   <span data-ttu-id="e9d22-173">**IO_REPARSE_TAG_WCI_LINK**</span><span class="sxs-lookup"><span data-stu-id="e9d22-173">**IO_REPARSE_TAG_WCI_LINK**</span></span>
-   <span data-ttu-id="e9d22-174">**IO_REPARSE_TAG_WCI_LINK_1**</span><span class="sxs-lookup"><span data-stu-id="e9d22-174">**IO_REPARSE_TAG_WCI_LINK_1**</span></span>
-   <span data-ttu-id="e9d22-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="e9d22-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span></span>
-   <span data-ttu-id="e9d22-176">**IO_REPARSE_TAG_WIM**</span><span class="sxs-lookup"><span data-stu-id="e9d22-176">**IO_REPARSE_TAG_WIM**</span></span>
-   <span data-ttu-id="e9d22-177">**IO_REPARSE_TAG_WOF**</span><span class="sxs-lookup"><span data-stu-id="e9d22-177">**IO_REPARSE_TAG_WOF**</span></span>

<span data-ttu-id="e9d22-178">Per garantire l'univocità dei tag, Microsoft fornisce un meccanismo per distribuire i nuovi tag.</span><span class="sxs-lookup"><span data-stu-id="e9d22-178">To ensure uniqueness of tags, Microsoft provides a mechanism to distribute new tags.</span></span> <span data-ttu-id="e9d22-179">Per ulteriori informazioni, vedere il [Kit Installable File System (IFS)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span><span class="sxs-lookup"><span data-stu-id="e9d22-179">For more information, see the [Installable File System (IFS) Kit](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span></span>

 

 



