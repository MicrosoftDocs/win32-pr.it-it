---
description: Oltre a essere accessibile tramite l'interfaccia IVssBackupComponents tramite l'oggetto dispositivo della copia, un richiedente può rendere disponibile una copia shadow per altri processi come dispositivo montato in sola lettura.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Esposizione ed emersione di volumi copiati Shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318583"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a><span data-ttu-id="04040-103">Esposizione ed emersione di volumi copiati Shadow</span><span class="sxs-lookup"><span data-stu-id="04040-103">Exposing and Surfacing Shadow Copied Volumes</span></span>

<span data-ttu-id="04040-104">Oltre a essere accessibile tramite l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) tramite l' [*oggetto dispositivo*](vssgloss-d.md)della copia, un richiedente può rendere disponibile una copia shadow per altri processi come dispositivo montato in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="04040-104">In addition to being accessed through the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface by means of its copy's [*device object*](vssgloss-d.md), a requester can make a shadow copy available to other processes as a mounted read-only device.</span></span>

<span data-ttu-id="04040-105">Questo processo è noto come [*esposizione di una copia shadow*](vssgloss-e.md)e viene eseguito usando il metodo [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) .</span><span class="sxs-lookup"><span data-stu-id="04040-105">This process is known as [*exposing a shadow copy*](vssgloss-e.md), and is performed using the [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) method.</span></span>

<span data-ttu-id="04040-106">Una copia shadow può essere esposta come volume locale, a cui è stata assegnata una lettera di unità o associata a una cartella montata, oppure come condivisione file.</span><span class="sxs-lookup"><span data-stu-id="04040-106">A shadow copy can be exposed as a local volume—assigned a drive letter or associated with a mounted folder—or as a file share.</span></span>

<span data-ttu-id="04040-107">Per illustrare, si consideri una copia shadow costituita da un volume nel exposedSys di sistema montato in F: \\ sulla cui radice sono le directory dirOne e dirTwo e il file FileOne.</span><span class="sxs-lookup"><span data-stu-id="04040-107">To illustrate, consider a shadow copy made of a volume on the system exposedSys mounted at F:\\ on whose root are the directories dirOne and dirTwo, and the file FileOne.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="04040-108">Esposizione locale di una copia shadow</span><span class="sxs-lookup"><span data-stu-id="04040-108">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="04040-109">Quando viene montata come volume locale, la radice della copia shadow è sempre visibile nel punto di montaggio (lettera di unità o cartella montata) e tutti i file copiati dall'ombreggiatura sono visibili.</span><span class="sxs-lookup"><span data-stu-id="04040-109">When mounted as a local volume, the shadow copy's root is always visible at the mount point (drive letter or mounted folder) and all the shadow-copied files are visible.</span></span>

<span data-ttu-id="04040-110">Se la copia shadow è stata esposta localmente tramite la cartella montata C: \\ ShadowOfF, si troveranno tutti i file presenti sul disco montati a F: \\ al momento della copia shadow disponibile in c: \\ ShadowOfF.</span><span class="sxs-lookup"><span data-stu-id="04040-110">If the shadow copy was locally exposed through the mounted folder C:\\ShadowOfF, you would find all files present on disk mounted at F:\\ at the time of the shadow copy available under C:\\ShadowOfF.</span></span> <span data-ttu-id="04040-111">L'analisi di C: \\ ShadowOfF potrebbe rivelare due directory, dirOne e dirTwo, e un file, FileOne, in c: \\ ShadowOfF.</span><span class="sxs-lookup"><span data-stu-id="04040-111">Examining C:\\ShadowOfF would reveal two directories, dirOne and dirTwo, and one file, fileOne, under C:\\ShadowOfF.</span></span>

<span data-ttu-id="04040-112">Una chiamata a esporre localmente la copia shadow potrebbe essere:</span><span class="sxs-lookup"><span data-stu-id="04040-112">A call to locally expose the shadow copy might be:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="04040-113">Se la copia shadow è stata esposta correttamente localmente, *wszExposed* deve contenere la stringa di caratteri wide "C: \\ ShadowOfF".</span><span class="sxs-lookup"><span data-stu-id="04040-113">If the shadow copy was successfully exposed locally, *wszExposed* should contain the wide character string "C:\\ShadowOfF."</span></span>

<span data-ttu-id="04040-114">In seguito, la copia shadow può essere non esposta chiamando [**IVssBackupComponentsEx2:: UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="04040-114">The shadow copy can later be unexposed by calling [**IVssBackupComponentsEx2::UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span></span>

<span data-ttu-id="04040-115">Solo le copie shadow persistenti, ovvero le copie shadow create con il rollback dell' \_ app VSS CTX \_ NAS \_ o VSS \_ ctx, \_ \_ possono essere esposte localmente.</span><span class="sxs-lookup"><span data-stu-id="04040-115">Only persistent shadow copies—that is, shadow copies created with either VSS\_CTX\_NAS\_ROLLBACK or VSS\_CTX\_APP\_ROLLBACK—can be exposed locally.</span></span>

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a><span data-ttu-id="04040-116">Esposizione di una copia shadow come condivisione remota</span><span class="sxs-lookup"><span data-stu-id="04040-116">Exposing a Shadow Copy as a Remote Share</span></span>

<span data-ttu-id="04040-117">In alternativa, è possibile scegliere di rendere la copia shadow del disco montata in F: \\ disponibile come condivisione file remota ed esporre solo i dati in dirTwo come condivisione file dirTwoOfF.</span><span class="sxs-lookup"><span data-stu-id="04040-117">Alternatively, you could choose to make the shadow copy of the disk mounted at F:\\ available as a remote file share, and expose only data under dirTwo as the file share dirTwoOfF.</span></span>

<span data-ttu-id="04040-118">In questo caso, i sistemi possono accedere alla copia shadow dei file in F: \\ dirTwo eseguendo il mapping di \\ \\ exposedSys \\ dirTwoOfF come unità di rete.</span><span class="sxs-lookup"><span data-stu-id="04040-118">In this case, systems could access the shadow copy of files under F:\\dirTwo by mapping \\\\exposedSys\\dirTwoOfF as a network drive.</span></span>

<span data-ttu-id="04040-119">Una chiamata a implement Remote esponendo la copia shadow come condivisione potrebbe essere la seguente:</span><span class="sxs-lookup"><span data-stu-id="04040-119">A call to implement remote exposing the shadow copy as a share might be the following:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="04040-120">Se la copia shadow è stata esposta in remoto, *wszExposed* deve contenere la stringa di caratteri wide "dirTwoOfF".</span><span class="sxs-lookup"><span data-stu-id="04040-120">If the shadow copy was successfully exposed remotely, *wszExposed* should contain the wide character string "dirTwoOfF."</span></span>

<span data-ttu-id="04040-121">Qualsiasi sistema che attualmente sta eseguendo il mapping della condivisione di rete di dirTwoOfF potrebbe disconnettersi, così come potrebbe disconnettersi da qualsiasi condivisione ordinaria.</span><span class="sxs-lookup"><span data-stu-id="04040-121">Any system currently mapping the network share of dirTwoOfF could disconnect from it, just as it might disconnect from any ordinary share.</span></span>

## <a name="surfacing-a-shadow-copy"></a><span data-ttu-id="04040-122">Emersione di una copia shadow</span><span class="sxs-lookup"><span data-stu-id="04040-122">Surfacing a Shadow Copy</span></span>

<span data-ttu-id="04040-123">Una [*copia shadow di superficie*](vssgloss-s.md) è una copia in cui la copia shadow è nota allo spazio dei nomi del gestore di montaggio di un sistema.</span><span class="sxs-lookup"><span data-stu-id="04040-123">A [*surfaced shadow copy*](vssgloss-s.md) is one in which the shadow copy is known to a system's Mount Manager namespace.</span></span>

<span data-ttu-id="04040-124">Ciò significa che è possibile individuare tali copie shadow in modo analogo a qualsiasi altro volume disponibile ma non ancora montato, ad esempio usando **FindFirstVolume** e **FindNextVolume**.</span><span class="sxs-lookup"><span data-stu-id="04040-124">This means that you can locate such shadow copies just as you would locate any other available but not-yet-mounted volume—by using **FindFirstVolume** and **FindNextVolume**, for example.</span></span>

<span data-ttu-id="04040-125">Ovviamente, le copie shadow esposte sono anche copie shadow di superficie.</span><span class="sxs-lookup"><span data-stu-id="04040-125">Clearly, then, exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="04040-126">Tuttavia, il contrario non è necessariamente vero.</span><span class="sxs-lookup"><span data-stu-id="04040-126">However, the reverse is not necessarily true.</span></span>

<span data-ttu-id="04040-127">Se una copia shadow esposta localmente è stata smontata o un sistema ha scelto di disconnettere una copia shadow esposta in modalità remota, la copia shadow non verrà più esposta.</span><span class="sxs-lookup"><span data-stu-id="04040-127">If a locally exposed shadow copy was dismounted, or a system chose to disconnect a remotely exposed shadow copy, that shadow copy would no longer be exposed.</span></span> <span data-ttu-id="04040-128">Tuttavia, finché la copia shadow viene mantenute, i volumi verrebbero esposti.</span><span class="sxs-lookup"><span data-stu-id="04040-128">However, as long as the shadow copy persisted, the volumes would be surfaced.</span></span> <span data-ttu-id="04040-129">Ciò significa che possono essere montati come qualsiasi altro volume di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="04040-129">This means they could be mounted like any other read-only volume.</span></span>

 

 



