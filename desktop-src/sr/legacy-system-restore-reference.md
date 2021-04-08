---
title: Riferimento ripristino configurazione di sistema legacy
description: Questa documentazione descrive i dettagli di implementazione del repository usati da una versione legacy di ripristino configurazione di sistema. Non si applica all'implementazione di ripristino configurazione di sistema in Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855458"
---
# <a name="legacy-system-restore-reference"></a><span data-ttu-id="90721-104">Riferimento ripristino configurazione di sistema legacy</span><span class="sxs-lookup"><span data-stu-id="90721-104">Legacy System Restore Reference</span></span>

<span data-ttu-id="90721-105">\[Queste informazioni si applicano solo a Windows XP con Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="90721-105">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="90721-106">Questa documentazione descrive i dettagli di implementazione del repository usati da una versione legacy di ripristino configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="90721-106">This documentation describes implementation details of the repository used by a legacy version of System Restore.</span></span> <span data-ttu-id="90721-107">Non si applica all'implementazione di ripristino configurazione di sistema in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="90721-107">It does not apply to the implementation of System Restore on Windows Vista.</span></span>

## <a name="system-restore-repository-structure"></a><span data-ttu-id="90721-108">Struttura del repository di ripristino del sistema</span><span class="sxs-lookup"><span data-stu-id="90721-108">System Restore Repository Structure</span></span>

<span data-ttu-id="90721-109">Windows XP con SP2 contiene un repository per ripristino configurazione di sistema nella cartella seguente:% SYSTEMDRIVE% \\ System Volume Information.</span><span class="sxs-lookup"><span data-stu-id="90721-109">Windows XP with SP2 contains a repository for System Restore in the following folder: %SYSTEMDRIVE%\\System Volume Information.</span></span> <span data-ttu-id="90721-110">Questo repository contiene informazioni per i punti di ripristino, che sono essenzialmente uno snapshot del sistema in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="90721-110">This repository contains information for restore points, which are essentially a snapshot of the system at a moment in time.</span></span>

<span data-ttu-id="90721-111">Il repository è strutturato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="90721-111">The repository is structured as follows:</span></span>

<span data-ttu-id="90721-112">**System Volume Information**    \*\* \_ Restore {*GUID*}\*\*       **RP1**       **RP2**       **RP *n*-1**       **RP \* n** \*     \*\* \_ Restore {*GUID*}\*\*       **RP1**       **RP2**       **RP *n*-1**       **RP \* n**\*</span><span class="sxs-lookup"><span data-stu-id="90721-112">**System Volume Information**    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*</span></span>

<span data-ttu-id="90721-113">Per determinare quale \_ cartella di ripristino {*GUID*} usare, leggere il **GUID** specificato nel file seguente: SYSTEMROOT% \\ system32 \\ Restore \\MachineGUID.txt.</span><span class="sxs-lookup"><span data-stu-id="90721-113">To determine which \_restore{*GUID*} folder to use, read the **GUID** specified in the following file: SYSTEMROOT%\\System32\\Restore\\MachineGUID.txt.</span></span>

<span data-ttu-id="90721-114">All'interno di ogni \_ cartella Restore {*GUID*}, il \_ file driver. cfg contiene informazioni provenienti da una struttura di **\_ \_ configurazione persistente SR** definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="90721-114">Within each \_restore{*GUID*} folder, the \_driver.cfg file contains information from a **SR\_PERSISTENT\_CONFIG** structure defined as follows:</span></span>

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a><span data-ttu-id="90721-115">File contenuti in ogni cartella RP *n*</span><span class="sxs-lookup"><span data-stu-id="90721-115">Files Contained in Each RP *n* Folder</span></span>

<span data-ttu-id="90721-116">Ogni cartella RP *n* contiene una cartella snapshot che contiene gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="90721-116">Each RP *n* folder contains a Snapshot folder that contains the following:</span></span>

-   <span data-ttu-id="90721-117">Uno snapshot degli hive del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="90721-117">A snapshot of the registry hives</span></span>
-   <span data-ttu-id="90721-118">Una cartella del repository che contiene uno snapshot del repository WMI</span><span class="sxs-lookup"><span data-stu-id="90721-118">A Repository folder that contains a snapshot of the WMI repository</span></span>
-   <span data-ttu-id="90721-119">Snapshot del database COM+</span><span class="sxs-lookup"><span data-stu-id="90721-119">A snapshot of the COM+ database</span></span>
-   <span data-ttu-id="90721-120">Uno snapshot del database IIS</span><span class="sxs-lookup"><span data-stu-id="90721-120">A snapshot of the IIS database</span></span>

<span data-ttu-id="90721-121">Ogni cartella RP *n* contiene un file RP. log che contiene informazioni generali sul punto di ripristino dalla struttura [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) .</span><span class="sxs-lookup"><span data-stu-id="90721-121">Each RP *n* folder contains an RP.log file that contains general information about the restore point from the [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) structure.</span></span>

<span data-ttu-id="90721-122">Ogni cartella RP *n* può contenere file usati per tenere traccia delle modifiche per un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="90721-122">Each RP *n* folder may contain files used to track changes for a restore point.</span></span> <span data-ttu-id="90721-123">Il primo file è denominato Change. log, il file successivo è denominato Change. log. 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="90721-123">The first file is named change.log, the next file is named change.log.1, and so on.</span></span> <span data-ttu-id="90721-124">Ogni file di log delle modifiche contiene le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="90721-124">Each change log file contains the following structures:</span></span>

-   [<span data-ttu-id="90721-125">**MODIFICARE \_ l' \_ intestazione del log**</span><span class="sxs-lookup"><span data-stu-id="90721-125">**CHANGE\_LOG\_HEADER**</span></span>](change-log-header.md)
-   <span data-ttu-id="90721-126">[**Modifica \_ di \_Voce di log**](change-log-entry.md)1</span><span class="sxs-lookup"><span data-stu-id="90721-126">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)1</span></span>
-   <span data-ttu-id="90721-127">[**Modifica \_ di \_Voce di log**](change-log-entry.md)2</span><span class="sxs-lookup"><span data-stu-id="90721-127">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)2</span></span>
-   <span data-ttu-id="90721-128">...</span><span class="sxs-lookup"><span data-stu-id="90721-128">...</span></span>
-   <span data-ttu-id="90721-129">[**Modifica \_ di \_Voce di log**](change-log-entry.md)*n*</span><span class="sxs-lookup"><span data-stu-id="90721-129">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)*n*</span></span>

## <a name="related-topics"></a><span data-ttu-id="90721-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90721-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90721-131">Strutture di ripristino del sistema legacy</span><span class="sxs-lookup"><span data-stu-id="90721-131">Legacy System Restore Structures</span></span>](legacy-system-restore-structures.md)
</dt> </dl>

 

 




