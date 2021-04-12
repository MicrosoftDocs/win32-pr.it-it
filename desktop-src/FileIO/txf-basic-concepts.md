---
description: Descrive la coerenza Read Committed, l'isolamento Read committed e i concetti di blocco transazionale in Transactional NTFS.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Concetti di base di TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347821"
---
# <a name="basic-txf-concepts"></a><span data-ttu-id="3ec79-103">Concetti di base di TxF</span><span class="sxs-lookup"><span data-stu-id="3ec79-103">Basic TxF Concepts</span></span>

## <a name="read-isolation"></a><span data-ttu-id="3ec79-104">Isolamento di lettura</span><span class="sxs-lookup"><span data-stu-id="3ec79-104">Read Isolation</span></span>

<span data-ttu-id="3ec79-105">Transactional NTFS (TxF) fornisce la coerenza Read Committed.</span><span class="sxs-lookup"><span data-stu-id="3ec79-105">Transactional NTFS (TxF) provides read-committed consistency.</span></span>

<span data-ttu-id="3ec79-106">Un [*writer transazionale*](glossary.md) fa riferimento a un handle di file transazionale aperto con qualsiasi autorizzazione che non fa parte di un accesso in lettura generico, ma fa parte di un accesso in scrittura generico.</span><span class="sxs-lookup"><span data-stu-id="3ec79-106">A [*transacted writer*](glossary.md) refers to a transacted file handle opened with any permission that is not part of generic read access but is part of generic write access.</span></span> <span data-ttu-id="3ec79-107">Un *writer transazionale* Visualizza la versione più recente di un file che include tutte le modifiche apportate dalla stessa transazione.</span><span class="sxs-lookup"><span data-stu-id="3ec79-107">A *transacted writer* views the most recent version of a file that includes all of the changes by the same transaction.</span></span> <span data-ttu-id="3ec79-108">Può essere presente un solo Writer transazionale per ogni file.</span><span class="sxs-lookup"><span data-stu-id="3ec79-108">There can be only one transacted writer per file.</span></span> <span data-ttu-id="3ec79-109">I writer non sottoposti a transazione sono sempre bloccati da un writer transazionale, anche se il file viene aperto con autorizzazioni di scrittura condivise.</span><span class="sxs-lookup"><span data-stu-id="3ec79-109">Non-transacted writers are always blocked by a transacted writer, even if the file is opened with shared-write permissions.</span></span>

<span data-ttu-id="3ec79-110">Un [*lettore transazionale*](glossary.md) fa riferimento a un handle di file transazionale aperto con qualsiasi autorizzazione che fa parte di un accesso in lettura generico, ma non fa parte dell'accesso in scrittura generico.</span><span class="sxs-lookup"><span data-stu-id="3ec79-110">A [*transacted reader*](glossary.md) refers to a transacted file handle opened with any permission that is a part of generic read access but is not part of generic write access.</span></span> <span data-ttu-id="3ec79-111">Un *lettore transazionale* Visualizza una versione di cui è stato eseguito il commit del file esistente al momento dell'apertura dell'handle di file.</span><span class="sxs-lookup"><span data-stu-id="3ec79-111">A *transacted reader* views a committed version of the file that existed at the time the file handle was opened.</span></span> <span data-ttu-id="3ec79-112">Il lettore transazionale è isolato dagli effetti dei writer transazionali.</span><span class="sxs-lookup"><span data-stu-id="3ec79-112">The transacted reader is isolated from the effects of transacted writers.</span></span> <span data-ttu-id="3ec79-113">Questo fornisce una visualizzazione coerente del file solo per la durata dell'handle di file e blocca i writer non sottoposti a transazione.</span><span class="sxs-lookup"><span data-stu-id="3ec79-113">This provides a consistent view of the file only for the life of the file handle and blocks non-transacted writers.</span></span>

> [!Note]  
> <span data-ttu-id="3ec79-114">Quando un handle è stato aperto per la modifica con la funzione [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) , tutte le aperture successive del file all'interno di tale transazione, se di sola lettura o non vengono convertite dal sistema come writer transazionale a scopo di isolamento e di altra semantica transazionale.</span><span class="sxs-lookup"><span data-stu-id="3ec79-114">When a handle has been opened for modification with the [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) function, all subsequent opens of the file within that transaction whether read-only or not are converted by the system to be a transacted writer for the purposes of isolation and other transactional semantics.</span></span> <span data-ttu-id="3ec79-115">Ciò significa che in seguito, quando un handle viene aperto per l'accesso in sola lettura, l'handle non riceve una visualizzazione del file prima dell'inizio della transazione. riceve la visualizzazione delle transazioni attive del file.</span><span class="sxs-lookup"><span data-stu-id="3ec79-115">This means that subsequently, when a handle is opened for read-only access, the handle does not receive a view of the file prior to the start of the transaction; it receives the active transaction view of the file.</span></span>

 

<span data-ttu-id="3ec79-116">Un handle di file non transazionale non Visualizza le modifiche apportate all'interno di una transazione fino a quando non viene eseguito il commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="3ec79-116">A non-transacted file handle does not see any changes made within a transaction until the transaction is committed.</span></span> <span data-ttu-id="3ec79-117">L'handle di file non transazionale riceve una visualizzazione isolata che è simile a un lettore sottoposto a transazione, ma a differenza di un reader transazionale, riceve l'aggiornamento del file quando un writer transazionale esegue il commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="3ec79-117">The non-transacted file handle receives an isolated view that is similar to a transacted reader, but unlike a transacted reader, it receives the file update when a transacted writer commits the transaction.</span></span>

## <a name="isolation-levels"></a><span data-ttu-id="3ec79-118">Livelli di isolamento</span><span class="sxs-lookup"><span data-stu-id="3ec79-118">Isolation Levels</span></span>

<span data-ttu-id="3ec79-119">TxF fornisce un isolamento Read Committed.</span><span class="sxs-lookup"><span data-stu-id="3ec79-119">TxF provides read-committed isolation.</span></span> <span data-ttu-id="3ec79-120">Questo significa che gli aggiornamenti dei file non vengono visualizzati all'esterno della transazione.</span><span class="sxs-lookup"><span data-stu-id="3ec79-120">This means that file updates are not seen outside the transaction.</span></span> <span data-ttu-id="3ec79-121">Inoltre, se un file viene aperto più volte durante la lettura dei file all'interno della transazione, è possibile che vengano visualizzati risultati diversi a ogni apertura successiva.</span><span class="sxs-lookup"><span data-stu-id="3ec79-121">In addition, if a file is opened more than once while reading files within the transaction, you may see different results with each subsequent opening.</span></span> <span data-ttu-id="3ec79-122">I file che erano disponibili la prima volta che si accedevano potrebbero non essere disponibili, perché sono stati eliminati, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="3ec79-122">Files that were available the first time you accessed them may not be available (because they were deleted), or vice versa.</span></span>

## <a name="transactional-locking"></a><span data-ttu-id="3ec79-123">Blocco transazionale</span><span class="sxs-lookup"><span data-stu-id="3ec79-123">Transactional Locking</span></span>

<span data-ttu-id="3ec79-124">La creazione di un writer transazionale in un file blocca il file in modo *transazionale* .</span><span class="sxs-lookup"><span data-stu-id="3ec79-124">Creating a transacted writer on a file *transactionally locks* the file.</span></span> <span data-ttu-id="3ec79-125">Dopo che un file è stato bloccato da una transazione, altre file system operazioni esterne alla transazione di blocco che tentano di modificare il file bloccato a livello transazionale avranno esito negativo con **\_ \_ violazione della condivisione degli errori** o **\_ \_ conflitti transazionali**.</span><span class="sxs-lookup"><span data-stu-id="3ec79-125">After a file is locked by a transaction, other file system operations external to the locking transaction that try to modify the transactionally locked file will fail with either **ERROR\_SHARING\_VIOLATION** or **ERROR\_TRANSACTIONAL\_CONFLICT**.</span></span>

<span data-ttu-id="3ec79-126">Nella tabella seguente viene riepilogato il blocco transazionale.</span><span class="sxs-lookup"><span data-stu-id="3ec79-126">The following table summarizes transactional locking.</span></span>



<span data-ttu-id="3ec79-127">File attualmente aperto da</span><span class="sxs-lookup"><span data-stu-id="3ec79-127">File currently opened by</span></span>

<span data-ttu-id="3ec79-128">File aperto tentato da</span><span class="sxs-lookup"><span data-stu-id="3ec79-128">File open attempted by</span></span>

<span data-ttu-id="3ec79-129">Con transazione eseguita</span><span class="sxs-lookup"><span data-stu-id="3ec79-129">Transacted</span></span>

<span data-ttu-id="3ec79-130">Non transazionale</span><span class="sxs-lookup"><span data-stu-id="3ec79-130">Non-Transacted</span></span>

<span data-ttu-id="3ec79-131">Lettore</span><span class="sxs-lookup"><span data-stu-id="3ec79-131">Reader</span></span>

<span data-ttu-id="3ec79-132">Reader/Writer</span><span class="sxs-lookup"><span data-stu-id="3ec79-132">Reader/Writer</span></span>

<span data-ttu-id="3ec79-133">Lettore</span><span class="sxs-lookup"><span data-stu-id="3ec79-133">Reader</span></span>

<span data-ttu-id="3ec79-134">Reader/Writer</span><span class="sxs-lookup"><span data-stu-id="3ec79-134">Reader/Writer</span></span>

<span data-ttu-id="3ec79-135">Lettore sottoposto a transazione</span><span class="sxs-lookup"><span data-stu-id="3ec79-135">Transacted Reader</span></span>

<span data-ttu-id="3ec79-136">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-136">Yes</span></span>

<span data-ttu-id="3ec79-137">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-137">Yes</span></span>

<span data-ttu-id="3ec79-138">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-138">Yes</span></span>

<span data-ttu-id="3ec79-139">No2</span><span class="sxs-lookup"><span data-stu-id="3ec79-139">No2</span></span>

<span data-ttu-id="3ec79-140">Lettura/scrittura transazionale</span><span class="sxs-lookup"><span data-stu-id="3ec79-140">Transacted Reader/Writer</span></span>

<span data-ttu-id="3ec79-141">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-141">Yes</span></span>

<span data-ttu-id="3ec79-142">No2</span><span class="sxs-lookup"><span data-stu-id="3ec79-142">No2</span></span>

<span data-ttu-id="3ec79-143">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-143">Yes</span></span>

<span data-ttu-id="3ec79-144">No2</span><span class="sxs-lookup"><span data-stu-id="3ec79-144">No2</span></span>

<span data-ttu-id="3ec79-145">Lettore non sottoposto a transazione</span><span class="sxs-lookup"><span data-stu-id="3ec79-145">Non-Transacted Reader</span></span>

<span data-ttu-id="3ec79-146">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-146">Yes</span></span>

<span data-ttu-id="3ec79-147">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-147">Yes</span></span>

<span data-ttu-id="3ec79-148">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-148">Yes</span></span>

<span data-ttu-id="3ec79-149">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-149">Yes</span></span>

<span data-ttu-id="3ec79-150">Lettura/scrittura non in transazioni</span><span class="sxs-lookup"><span data-stu-id="3ec79-150">Non-Transacted Reader/Writer</span></span>

<span data-ttu-id="3ec79-151">No1</span><span class="sxs-lookup"><span data-stu-id="3ec79-151">No1</span></span>

<span data-ttu-id="3ec79-152">No1</span><span class="sxs-lookup"><span data-stu-id="3ec79-152">No1</span></span>

<span data-ttu-id="3ec79-153">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-153">Yes</span></span>

<span data-ttu-id="3ec79-154">Sì</span><span class="sxs-lookup"><span data-stu-id="3ec79-154">Yes</span></span>

1. <span data-ttu-id="3ec79-155">Esito negativo con **errore di \_ transazione \_ transazionale**</span><span class="sxs-lookup"><span data-stu-id="3ec79-155">Fails with **ERROR\_TRANSACTIONAL\_CONFLICT**</span></span><br/> <span data-ttu-id="3ec79-156">2. esito negativo con **\_ \_ violazione della condivisione degli errori**</span><span class="sxs-lookup"><span data-stu-id="3ec79-156">2. Fails with **ERROR\_SHARING\_VIOLATION**</span></span><br/>



 

<span data-ttu-id="3ec79-157">Se si apre un flusso denominato per una modifica che utilizza una transazione, è necessario bloccare l'intero file.</span><span class="sxs-lookup"><span data-stu-id="3ec79-157">If you open a named stream for a modification that is using a transaction, the entire file is required to be locked.</span></span>

<span data-ttu-id="3ec79-158">Oltre al blocco transazionale, vengono applicate le normali regole di condivisione file NTFS.</span><span class="sxs-lookup"><span data-stu-id="3ec79-158">In addition to transactional locking, typical NTFS file-sharing rules apply.</span></span>

<span data-ttu-id="3ec79-159">In parallelo è necessario considerare le due modalità di condivisione file seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ec79-159">You need to consider the following two file sharing modes in parallel:</span></span>

-   <span data-ttu-id="3ec79-160">Modalità di blocco transazionale.</span><span class="sxs-lookup"><span data-stu-id="3ec79-160">The transactional locking mode.</span></span>
-   <span data-ttu-id="3ec79-161">Modalità di condivisione file normali.</span><span class="sxs-lookup"><span data-stu-id="3ec79-161">Normal file-sharing modes.</span></span>

<span data-ttu-id="3ec79-162">Qualunque sia la modalità più restrittiva è quella che si applica.</span><span class="sxs-lookup"><span data-stu-id="3ec79-162">Whichever mode is more restrictive is the one that applies.</span></span>

 

 




