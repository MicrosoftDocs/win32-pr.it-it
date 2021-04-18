---
title: Ripristino del sistema
description: Quando il computer viene usato nel tempo, i punti di ripristino vengono raccolti nell'archivio dati senza alcuna gestione o intervento richiesto dall'utente.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c5ff4aef88ec9eca591ee3c1afb1ad570689a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298233"
---
# <a name="restoring-the-system"></a><span data-ttu-id="c039b-103">Ripristino del sistema</span><span class="sxs-lookup"><span data-stu-id="c039b-103">Restoring the System</span></span>

<span data-ttu-id="c039b-104">Quando il computer viene usato nel tempo, i punti di ripristino vengono raccolti nell'archivio dati senza alcuna gestione o intervento richiesto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c039b-104">As the computer is used over time, restore points are collected in the data archive without any management or intervention required by the user.</span></span> <span data-ttu-id="c039b-105">Se l'utente deve sempre ripristinare lo stato precedente del sistema, i punti di ripristino disponibili vengono resi visibili all'utente tramite l'interfaccia utente di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="c039b-105">If the user ever needs to restore the system to a previous state, the available restore points are made visible to the user through the System Restore user interface.</span></span> <span data-ttu-id="c039b-106">L'utente può scegliere uno di questi punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c039b-106">The user can choose any of these restore points.</span></span> <span data-ttu-id="c039b-107">L'unico modo per accedere a questo archivio dei punti di ripristino è tramite l'interfaccia utente di ripristino del sistema e l'API di ripristino del sistema. Ciò consente di proteggere l'integrità dei dati ed evitare modifiche accidentali apportate dall'utente, dalle applicazioni o da altri agenti.</span><span class="sxs-lookup"><span data-stu-id="c039b-107">The only way to access this archive of restore points is through the System Restore user interface and the System Restore API; this is to protect data integrity and prevent accidental changes made by the user, applications, or other agents.</span></span>

<span data-ttu-id="c039b-108">Per ripristinare un sistema, ripristino configurazione di sistema Annulla le modifiche apportate ai file monitorati, riacquisendo lo stato del file al momento del punto di ripristino selezionato.</span><span class="sxs-lookup"><span data-stu-id="c039b-108">To restore a system, System Restore undoes file changes made to monitored files, recapturing the file state at the time of the selected restore point.</span></span> <span data-ttu-id="c039b-109">Sostituisce quindi il registro di sistema corrente con quello salvato per il punto di ripristino selezionato.</span><span class="sxs-lookup"><span data-stu-id="c039b-109">It then replaces the current registry with the one saved for the selected restore point.</span></span>

<span data-ttu-id="c039b-110">Per assicurarsi che l'applicazione abbia il comportamento desiderato dopo un ripristino, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c039b-110">To ensure that your application has the desired behavior after a restore, do the following:</span></span>

-   <span data-ttu-id="c039b-111">Non archiviare nel registro di sistema le informazioni che impediscono agli utenti di accedere ai file di dati personali o alle applicazioni in ripristino configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="c039b-111">Do not store information in the registry that prevents user access to personal data files or applications on system restore.</span></span> <span data-ttu-id="c039b-112">In caso contrario, è necessario fornire un meccanismo mediante il quale l'utente può scaricare e reinstallare le applicazioni senza doverle pagare di nuovo.</span><span class="sxs-lookup"><span data-stu-id="c039b-112">Otherwise, you must provide a mechanism by which the user can download and reinstall the applications without having to pay for them again.</span></span>
-   <span data-ttu-id="c039b-113">Utilizzare l' [API ripristino configurazione di sistema](system-restore-api.md) per creare punti di ripristino significativi in fase di installazione e disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="c039b-113">Use the [System Restore API](system-restore-api.md) to create meaningful restore points at install and uninstall.</span></span>
-   <span data-ttu-id="c039b-114">In Windows XP, i file binari dell'applicazione chiave da proteggere devono utilizzare le estensioni coerenti con quelle utilizzate in Filelist.xml.</span><span class="sxs-lookup"><span data-stu-id="c039b-114">In Windows XP, the key application binaries to be protected must use extensions consistent with those used in Filelist.xml.</span></span> <span data-ttu-id="c039b-115">Per altre informazioni, vedere [estensioni di file monitorate](monitored-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="c039b-115">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span> <span data-ttu-id="c039b-116">Questo file non viene utilizzato da Windows 7 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c039b-116">This file is not used by Windows 7 and Windows Vista.</span></span> <span data-ttu-id="c039b-117">Non usare i tipi di estensione monitorati per i file modificabili dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c039b-117">Do not use monitored extension types for user-editable files.</span></span> <span data-ttu-id="c039b-118">Ad esempio, se si rinomina un file di dati personali di un utente usando Extension. ini, l'utente potrebbe perdere lavoro in seguito a un ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="c039b-118">For example, if you name a user's personal data file using the extension .ini, the user may lose work as a result of a system restore.</span></span>

 

 




