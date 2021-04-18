---
title: Oggetto ripristinatore backup
description: Oggetto ripristinatore backup
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Media Format SDK, oggetti del ripristino di backup
- ASF (Advanced Systems Format), oggetti del ripristino di backup
- ASF (formato avanzato dei sistemi), oggetti del ripristino di backup
- oggetti, backup di oggetti del ripristino
- ripristino di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299427"
---
# <a name="backup-restorer-object"></a><span data-ttu-id="f1141-108">Oggetto ripristinatore backup</span><span class="sxs-lookup"><span data-stu-id="f1141-108">Backup Restorer Object</span></span>

<span data-ttu-id="f1141-109">Il ripristino di backup fornisce le interfacce per gestire le licenze di backup, in genere su supporti rimovibili, quindi il ripristino di tali licenze su un nuovo computer.</span><span class="sxs-lookup"><span data-stu-id="f1141-109">The backup restorer provides interfaces to handle backing up licenses, typically onto removable media, and then restoring those licenses onto a new computer.</span></span>

<span data-ttu-id="f1141-110">L'oggetto di ripristino di backup viene creato dalla funzione [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) , che imposta un puntatore a un'interfaccia [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) .</span><span class="sxs-lookup"><span data-stu-id="f1141-110">The backup restorer object is created by the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function, which sets a pointer to an [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) interface.</span></span> <span data-ttu-id="f1141-111">Le altre interfacce dell'oggetto di ripristino di backup possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="f1141-111">The other interfaces of the backup restorer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="f1141-112">Le interfacce seguenti sono supportate dall'oggetto di ripristino di backup.</span><span class="sxs-lookup"><span data-stu-id="f1141-112">The following interfaces are supported by the backup restorer object.</span></span>



| <span data-ttu-id="f1141-113">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f1141-113">Interface</span></span>                                              | <span data-ttu-id="f1141-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1141-114">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1141-115">**IWMBackupRestoreProps**</span><span class="sxs-lookup"><span data-stu-id="f1141-115">**IWMBackupRestoreProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | <span data-ttu-id="f1141-116">Imposta e recupera le proprietà richieste dalle interfacce [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) e [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) .</span><span class="sxs-lookup"><span data-stu-id="f1141-116">Sets and retrieves properties required by the [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) and [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) interfaces.</span></span> |
| [<span data-ttu-id="f1141-117">**IWMLicenseBackup**</span><span class="sxs-lookup"><span data-stu-id="f1141-117">**IWMLicenseBackup**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | <span data-ttu-id="f1141-118">Esegue il backup delle licenze, in genere in modo che possano essere ripristinate su un altro computer.</span><span class="sxs-lookup"><span data-stu-id="f1141-118">Backs up licenses, typically so that they can be restored onto another computer.</span></span>                                                                          |
| [<span data-ttu-id="f1141-119">**IWMLicenseRestore**</span><span class="sxs-lookup"><span data-stu-id="f1141-119">**IWMLicenseRestore**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | <span data-ttu-id="f1141-120">Ripristina le licenze.</span><span class="sxs-lookup"><span data-stu-id="f1141-120">Restores licenses.</span></span>                                                                                                                                        |



 

<span data-ttu-id="f1141-121">L'interfaccia di callback seguente deve essere implementata dall'applicazione per poter utilizzare l'oggetto di ripristino di backup.</span><span class="sxs-lookup"><span data-stu-id="f1141-121">The following callback interface must be implemented by the application in order to use the backup restorer object.</span></span>



| <span data-ttu-id="f1141-122">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f1141-122">Interface</span></span>                                      | <span data-ttu-id="f1141-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1141-123">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="f1141-124">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="f1141-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="f1141-125">Riceve i messaggi di stato dai processi eseguiti in un thread separato.</span><span class="sxs-lookup"><span data-stu-id="f1141-125">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f1141-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1141-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1141-127">**Backup e ripristino di licenze**</span><span class="sxs-lookup"><span data-stu-id="f1141-127">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> <dt>

[<span data-ttu-id="f1141-128">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="f1141-128">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




