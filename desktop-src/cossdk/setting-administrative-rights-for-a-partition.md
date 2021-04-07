---
description: Impostazione dei diritti amministrativi per una partizione
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Impostazione dei diritti amministrativi per una partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748279"
---
# <a name="setting-administrative-rights-for-a-partition"></a><span data-ttu-id="05c78-103">Impostazione dei diritti amministrativi per una partizione</span><span class="sxs-lookup"><span data-stu-id="05c78-103">Setting Administrative Rights for a Partition</span></span>

<span data-ttu-id="05c78-104">Agli utenti assegnati al ruolo di amministratore dell'applicazione di sistema COM+ è consentito creare, modificare ed eliminare partizioni COM+.</span><span class="sxs-lookup"><span data-stu-id="05c78-104">Users assigned the Administrator role of the COM+ System Application are allowed to create, modify, and delete COM+ partitions.</span></span> <span data-ttu-id="05c78-105">All'interno dello strumento di amministrazione Servizi componenti, i ruoli amministrativi possono essere assegnati agli utenti espandendo la cartella **ruoli** dell'applicazione di sistema com+.</span><span class="sxs-lookup"><span data-stu-id="05c78-105">Within the Component Services administrative tool, administrative roles can be assigned to users by expanding the **Roles** folder of the COM+ System Application.</span></span>

<span data-ttu-id="05c78-106">A partire da Windows Server 2003, la funzionalità di autenticazione per l'applicazione di sistema COM+ include il valore EOAC \_ Disable \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="05c78-106">As of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="05c78-107">Questo valore, che disabilita le attivazioni di Activate-As-Activator (AAA), viene usato nella chiamata [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) quando viene avviata l'applicazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="05c78-107">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="05c78-108">Impostando la funzionalità di autenticazione su EOAC \_ Disable AAA è possibile consentire a \_ un'applicazione in esecuzione con un account con privilegi, ad esempio LocalSystem, di impedire l'utilizzo dell'identità per l'avvio di componenti non attendibili.</span><span class="sxs-lookup"><span data-stu-id="05c78-108">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05c78-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05c78-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05c78-110">Raccolta delle metriche della partizione</span><span class="sxs-lookup"><span data-stu-id="05c78-110">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="05c78-111">Configurazione della cache della partizione</span><span class="sxs-lookup"><span data-stu-id="05c78-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="05c78-112">Raggruppamento di applicazioni in partizioni</span><span class="sxs-lookup"><span data-stu-id="05c78-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="05c78-113">Gestione delle partizioni locali</span><span class="sxs-lookup"><span data-stu-id="05c78-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="05c78-114">Gestione di partizioni all'interno Active Directory</span><span class="sxs-lookup"><span data-stu-id="05c78-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
