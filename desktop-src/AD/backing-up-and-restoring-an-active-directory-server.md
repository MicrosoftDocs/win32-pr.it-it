---
title: Backup e ripristino di un server di Active Directory
description: Active Directory Domain Services forniscono funzioni per il backup e il ripristino dei dati nel database di directory.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, utilizzo, backup e ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724650"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a><span data-ttu-id="2e746-104">Backup e ripristino di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="2e746-104">Backing Up and Restoring an Active Directory Server</span></span>

<span data-ttu-id="2e746-105">Active Directory Domain Services forniscono funzioni per il backup e il ripristino dei dati nel database di directory.</span><span class="sxs-lookup"><span data-stu-id="2e746-105">Active Directory Domain Services provide functions for backing up and restoring data in the directory database.</span></span> <span data-ttu-id="2e746-106">In questa sezione viene descritto come [eseguire il backup](backing-up-an-active-directory-server.md) e il [ripristino](restoring-an-active-directory-server.md) di un server Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2e746-106">This section describes how to [back up](backing-up-an-active-directory-server.md) and [restore](restoring-an-active-directory-server.md) an Active Directory server.</span></span> <span data-ttu-id="2e746-107">Per ulteriori informazioni sul backup di un server di Active Directory utilizzando le utilità disponibili nei sistemi operativi Windows 2000 e Windows Server 2003, vedere il Resource Kit applicabile, disponibile sul sito Web Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="2e746-107">For more information about backing up an Active Directory server using the utilities provided in Windows 2000 and Windows Server 2003 operating systems, see the applicable Resource Kit, available on the Microsoft TechNet website.</span></span>

<span data-ttu-id="2e746-108">Il backup di un server di Active Directory deve essere eseguito online e deve essere eseguito durante l'installazione del Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="2e746-108">Backup of an Active Directory server must be performed online and must be performed when the Active Directory Domain Services are installed.</span></span> <span data-ttu-id="2e746-109">Active Directory Domain Services si basano su un database speciale ed esporta un set di funzioni di backup che forniscono l'interfaccia di backup a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="2e746-109">Active Directory Domain Services are built on a special database and export a set of backup functions that provide the programmatic backup interface.</span></span> <span data-ttu-id="2e746-110">Il backup non supporta i backup incrementali.</span><span class="sxs-lookup"><span data-stu-id="2e746-110">The backup does not support incremental backups.</span></span> <span data-ttu-id="2e746-111">Un'applicazione di backup viene associata a una DLL sul lato client locale con i punti di ingresso definiti in ntdsbcli. h.</span><span class="sxs-lookup"><span data-stu-id="2e746-111">A backup application binds to a local client-side DLL with entry points defined in Ntdsbcli.h.</span></span>

<span data-ttu-id="2e746-112">Il ripristino di un server di Active Directory viene sempre eseguito offline.</span><span class="sxs-lookup"><span data-stu-id="2e746-112">Restoration of an Active Directory server is always performed offline.</span></span>

<span data-ttu-id="2e746-113">Sebbene gli argomenti di questa sezione descrivano solo come eseguire il backup e il ripristino di un server di Active Directory, tenere presente che Windows 2000 e i sistemi operativi Windows Server 2003 hanno diversi componenti "stato del sistema" che devono essere sottoposti a backup e ripristinati insieme.</span><span class="sxs-lookup"><span data-stu-id="2e746-113">Although the topics in this section describe only how to back up and restore an Active Directory server, be aware that Windows 2000 and the Windows Server 2003 operating systems have several "system state" components that must be backed up and restored together.</span></span> <span data-ttu-id="2e746-114">Questi componenti di stato del sistema sono costituiti da:</span><span class="sxs-lookup"><span data-stu-id="2e746-114">These system state components consist of:</span></span>

-   <span data-ttu-id="2e746-115">File di avvio, ad esempio Ntldr, Ntdetect, tutti i file protetti da SFP e la configurazione del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="2e746-115">Boot files such as ntldr, ntdetect, all files protected by SFP, and performance counter configuration</span></span>
-   <span data-ttu-id="2e746-116">Controller di Dominio di Active Directory</span><span class="sxs-lookup"><span data-stu-id="2e746-116">The Active Directory Domain Controller</span></span>
-   <span data-ttu-id="2e746-117">SysVol (solo controller di dominio)</span><span class="sxs-lookup"><span data-stu-id="2e746-117">SysVol (domain controller only)</span></span>
-   <span data-ttu-id="2e746-118">Server di certificazione (solo CA)</span><span class="sxs-lookup"><span data-stu-id="2e746-118">Certificate Server (CA only)</span></span>
-   <span data-ttu-id="2e746-119">Database cluster (solo nodo cluster)</span><span class="sxs-lookup"><span data-stu-id="2e746-119">Cluster database (cluster node only)</span></span>
-   <span data-ttu-id="2e746-120">Registro</span><span class="sxs-lookup"><span data-stu-id="2e746-120">Registry</span></span>
-   <span data-ttu-id="2e746-121">Database di registrazione della classe COM+</span><span class="sxs-lookup"><span data-stu-id="2e746-121">COM+ class registration database</span></span>

<span data-ttu-id="2e746-122">È possibile eseguire il backup dello stato del sistema in qualsiasi ordine, ma il ripristino dello stato del sistema deve essere eseguito nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="2e746-122">The system state can be backed up in any order, but restoration of the system state must occur in the following order:</span></span>

1.  <span data-ttu-id="2e746-123">Ripristinare i file di avvio.</span><span class="sxs-lookup"><span data-stu-id="2e746-123">Restore the boot files.</span></span>
2.  <span data-ttu-id="2e746-124">Ripristinare SysVol, server di certificati, database cluster e database di registrazione della classe COM+, come applicabile.</span><span class="sxs-lookup"><span data-stu-id="2e746-124">Restore SysVol, Certificate Server, Cluster database and COM+ class registration database, as applicable.</span></span>
3.  <span data-ttu-id="2e746-125">Ripristinare il server Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2e746-125">Restore the Active Directory server.</span></span>
4.  <span data-ttu-id="2e746-126">Ripristinare il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2e746-126">Restore the registry.</span></span>

<span data-ttu-id="2e746-127">Per ulteriori informazioni sul backup e il ripristino di Servizi certificati, vedere [utilizzo delle funzioni di backup e ripristino di Servizi certificati](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span><span class="sxs-lookup"><span data-stu-id="2e746-127">For more information about backing up and restoring Certificate Services, see [Using the Certificate Services Backup and Restore Functions](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span></span>

<span data-ttu-id="2e746-128">Per ulteriori informazioni sul backup e il ripristino di Active Directory Domain Services, vedere:</span><span class="sxs-lookup"><span data-stu-id="2e746-128">For more information about backing up and restoring Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="2e746-129">Considerazioni per il backup Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="2e746-129">Considerations for Active Directory Domain Services Backup</span></span>](considerations-for-active-directory-domain-services-backup.md)
-   [<span data-ttu-id="2e746-130">Esecuzione del backup di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="2e746-130">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
-   [<span data-ttu-id="2e746-131">Ripristino di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="2e746-131">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
-   [<span data-ttu-id="2e746-132">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="2e746-132">Directory Backup Functions</span></span>](directory-backup-functions.md)

 

 