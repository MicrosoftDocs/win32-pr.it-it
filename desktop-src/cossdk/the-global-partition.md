---
description: Partizione globale
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: Partizione globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc218067bbf7170a1c2df6f306b6dfe5787ac2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483861"
---
# <a name="the-global-partition"></a><span data-ttu-id="c0061-103">Partizione globale</span><span class="sxs-lookup"><span data-stu-id="c0061-103">The Global Partition</span></span>

<span data-ttu-id="c0061-104">Oltre alle partizioni e ai set di partizioni definiti dall'amministratore, esiste una partizione speciale in ogni computer denominato *partizione globale*.</span><span class="sxs-lookup"><span data-stu-id="c0061-104">In addition to administrator-defined partitions and partition sets, there is a special partition on each computer called a *global partition*.</span></span> <span data-ttu-id="c0061-105">Quando si installa COM+, viene creata automaticamente una partizione globale.</span><span class="sxs-lookup"><span data-stu-id="c0061-105">A global partition is automatically created when COM+ is installed.</span></span> <span data-ttu-id="c0061-106">La partizione globale è progettata per contenere applicazioni a livello di sistema che devono essere accessibili a tutti gli utenti in un server o nel dominio.</span><span class="sxs-lookup"><span data-stu-id="c0061-106">The global partition is designed to contain system-wide applications that need to be accessible to all users on a server or in the domain.</span></span> <span data-ttu-id="c0061-107">L'installazione di un'applicazione nella partizione globale elimina la necessità di installare una copia dell'applicazione nel set di partizioni di ogni singolo utente.</span><span class="sxs-lookup"><span data-stu-id="c0061-107">Installing an application into the global partition removes the need to install a copy of the application into each individual user's partition set.</span></span>

<span data-ttu-id="c0061-108">Se il set di partizioni di un utente non include un'applicazione specifica a cui l'utente sta tentando di accedere, ma tale applicazione viene installata nella partizione globale, l'applicazione viene attivata dalla partizione globale.</span><span class="sxs-lookup"><span data-stu-id="c0061-108">If a user's partition set does not include a specific application that the user is attempting to access, but that application is installed in the global partition, the application is activated from the global partition.</span></span> <span data-ttu-id="c0061-109">In questo caso, tuttavia, tutti i componenti dell'applicazione installati nella partizione globale devono essere contrassegnati come componenti pubblici, non privati.</span><span class="sxs-lookup"><span data-stu-id="c0061-109">In this case, however, all components of the application installed in the global partition must be marked as public, not private, components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0061-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0061-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0061-111">Partizioni predefinite</span><span class="sxs-lookup"><span data-stu-id="c0061-111">Default Partitions</span></span>](default-partitions.md)
</dt> <dt>

[<span data-ttu-id="c0061-112">Partizioni locali</span><span class="sxs-lookup"><span data-stu-id="c0061-112">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="c0061-113">Proprietà partizione</span><span class="sxs-lookup"><span data-stu-id="c0061-113">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="c0061-114">Partizioni e Active Directory</span><span class="sxs-lookup"><span data-stu-id="c0061-114">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> </dl>

 

 



