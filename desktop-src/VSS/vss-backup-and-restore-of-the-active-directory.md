---
description: Il writer di Active Directory non richiede azioni speciali durante le operazioni di backup.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Backup e ripristino del servizio Copia Shadow del volume del Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526292"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a><span data-ttu-id="92774-103">Backup e ripristino del servizio Copia Shadow del volume del Active Directory</span><span class="sxs-lookup"><span data-stu-id="92774-103">VSS Backup and Restore of the Active Directory</span></span>

<span data-ttu-id="92774-104">Il writer di Active Directory non richiede azioni speciali durante le operazioni di backup.</span><span class="sxs-lookup"><span data-stu-id="92774-104">The Active Directory writer requires no special actions during backup operations.</span></span> <span data-ttu-id="92774-105">Il writer fornirà al richiedente il componente e le informazioni sui set di file e il richiedente utilizzerà tali informazioni per decidere quali file copiare nei supporti di backup.</span><span class="sxs-lookup"><span data-stu-id="92774-105">The writer will provide the requester with component and file set information, and the requester uses that information to decide which files to copy to backup media.</span></span> <span data-ttu-id="92774-106">Non è necessario usare API speciali per eseguire il backup del Active Directory.</span><span class="sxs-lookup"><span data-stu-id="92774-106">There is no need to use any special APIs to back up the Active Directory.</span></span>

<span data-ttu-id="92774-107">Il modo in cui viene eseguito un ripristino varia a seconda che il Active Directory venga ripristinato come parte di un'operazione di ripristino di emergenza o se il ripristino è a un sistema in cui è in esecuzione il Active Directory.</span><span class="sxs-lookup"><span data-stu-id="92774-107">How a restore is performed depends on whether the Active Directory is be restored as part of a disaster recovery operation, or if the restore is to a system on which the Active Directory is running.</span></span> <span data-ttu-id="92774-108">Inoltre, l'età della copia di backup dello stato del Active Directory potrebbe essere un problema a causa di Active Directory oggetti contrassegnati per la rimozione definitiva.</span><span class="sxs-lookup"><span data-stu-id="92774-108">In addition, the age of the backup copy of the Active Directory state may be an issue because of Active Directory tombstones.</span></span>

## <a name="active-directory-restoration-following-disaster-recovery"></a><span data-ttu-id="92774-109">Ripristino di Active Directory dopo il ripristino di emergenza</span><span class="sxs-lookup"><span data-stu-id="92774-109">Active Directory Restoration following Disaster Recovery</span></span>

<span data-ttu-id="92774-110">In seguito a un arresto anomalo che richiede il ripristino di emergenza, è possibile ripristinare il Active Directory come parte del ripristino dello stato del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="92774-110">Following a crash requiring disaster recovery, the Active Directory can be restored as part of the restoration of the operating system state.</span></span>

<span data-ttu-id="92774-111">Questa operazione di ripristino è essenzialmente un ripristino di scrittura.</span><span class="sxs-lookup"><span data-stu-id="92774-111">This restore operation is essentially a writerless restore.</span></span>

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a><span data-ttu-id="92774-112">Active Directory il ripristino sul sistema in cui è in esecuzione</span><span class="sxs-lookup"><span data-stu-id="92774-112">Active Directory Restoration on the System where It Is Running</span></span>

<span data-ttu-id="92774-113">Il sistema deve essere riavviato in modalità ripristino servizi directory se il Active Directory è attualmente in esecuzione nel server.</span><span class="sxs-lookup"><span data-stu-id="92774-113">The system must be rebooted in Directory Services Restore mode if the Active Directory is currently running on the server.</span></span>

<span data-ttu-id="92774-114">Il sistema operativo verrà quindi eseguito senza il Active Directory e la convalida dell'utente viene eseguita tramite Gestione account di sicurezza (SAM) nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="92774-114">The operating system will then be running without the Active Directory, and all user validation occurs through the Security Accounts Manager (SAM) in the registry.</span></span> <span data-ttu-id="92774-115">Solo l'amministratore dispone dell'autorizzazione per recuperare il Active Directory.</span><span class="sxs-lookup"><span data-stu-id="92774-115">Only the administrator has permission to recover the Active Directory.</span></span>

<span data-ttu-id="92774-116">Una volta in modalità ripristino servizio directory, un ripristino VSS può procedere normalmente.</span><span class="sxs-lookup"><span data-stu-id="92774-116">Once in Directory Service Restore mode, a VSS restore can proceed normally.</span></span> <span data-ttu-id="92774-117">Non esiste alcun motivo per usare API Win32 non VSS Active Directory per ripristinare lo stato di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="92774-117">There is no reason to use non-VSS Win32 Active Directory APIs to restore the Active Directory state.</span></span>

## <a name="active-directory-restores-and-active-directory-tombstones"></a><span data-ttu-id="92774-118">Active Directory ripristini e Active Directory oggetti contrassegnati per la rimozione definitiva</span><span class="sxs-lookup"><span data-stu-id="92774-118">Active Directory Restores and Active Directory Tombstones</span></span>

<span data-ttu-id="92774-119">Qualsiasi piano di ripristino deve garantire che l'età del backup non superi la durata Active Directory rimozione definitiva (il valore predefinito è 60 giorni).</span><span class="sxs-lookup"><span data-stu-id="92774-119">Any recovery plan should ensure that the age of the backup should not exceed the Active Directory Tombstone Lifetime (default is 60 days).</span></span>

<span data-ttu-id="92774-120">Il ripristino di un backup precedente alla rimozione definitiva determinerà l'esecuzione di oggetti che non vengono replicati negli altri server da parte di un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="92774-120">Restoration of a backup older than the tombstone will cause a domain controller to have objects that are not replicated to the other servers.</span></span>

<span data-ttu-id="92774-121">Gli oggetti che non vengono replicati non verranno eliminati automaticamente nel controller di dominio (ripristinato), perché gli oggetti contrassegnati per la rimozione definitiva di tali oggetti sulle altre repliche sono già stati eliminati.</span><span class="sxs-lookup"><span data-stu-id="92774-121">Those objects that are not replicated will not be deleted automatically on that (restored) domain controller because the tombstones of those objects on the other replicas have already been deleted.</span></span>

<span data-ttu-id="92774-122">Un amministratore dovrà eliminare manualmente ogni oggetto sul controller di dominio ripristinato che non viene replicato.</span><span class="sxs-lookup"><span data-stu-id="92774-122">An administrator will have to manually delete each of the objects on the restored domain controller that are not replicated.</span></span> <span data-ttu-id="92774-123">I backup incrementali della Active Directory non sono supportati. è necessario un backup completo.</span><span class="sxs-lookup"><span data-stu-id="92774-123">Incremental backups of the Active Directory are not supported; a full backup is required.</span></span>

 

 



