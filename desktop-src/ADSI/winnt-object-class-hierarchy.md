---
title: Gerarchia di classi di oggetti WinNT
description: La gerarchia di classi di oggetti WinNT inizia dall'oggetto spazio dei nomi.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- ADSI provider di servizi WinNT, gerarchia di classi di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515451"
---
# <a name="winnt-object-class-hierarchy"></a><span data-ttu-id="10695-104">Gerarchia di classi di oggetti WinNT</span><span class="sxs-lookup"><span data-stu-id="10695-104">WinNT Object Class Hierarchy</span></span>

<span data-ttu-id="10695-105">La gerarchia di classi di oggetti WinNT inizia dall'oggetto spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="10695-105">The WinNT object class hierarchy starts from the Namespace object.</span></span>



| <span data-ttu-id="10695-106">Object (classe)</span><span class="sxs-lookup"><span data-stu-id="10695-106">Object class</span></span>                   | <span data-ttu-id="10695-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10695-107">Description</span></span>                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="10695-108">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="10695-108">Namespace</span></span><br/>           | <span data-ttu-id="10695-109">Contenitore di oggetti di primo livello.</span><span class="sxs-lookup"><span data-stu-id="10695-109">Top-level object container.</span></span><br/>                                            |
| <span data-ttu-id="10695-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="10695-110">Domain</span></span><br/>              | <span data-ttu-id="10695-111">Dominio Windows NT.</span><span class="sxs-lookup"><span data-stu-id="10695-111">The Windows NT domain.</span></span><br/>                                                 |
| <span data-ttu-id="10695-112">User</span><span class="sxs-lookup"><span data-stu-id="10695-112">User</span></span><br/>                | <span data-ttu-id="10695-113">Account utente.</span><span class="sxs-lookup"><span data-stu-id="10695-113">User account.</span></span><br/>                                                          |
| <span data-ttu-id="10695-114">Group</span><span class="sxs-lookup"><span data-stu-id="10695-114">Group</span></span><br/>               | <span data-ttu-id="10695-115">Account di gruppo per la gestione dei diritti di accesso.</span><span class="sxs-lookup"><span data-stu-id="10695-115">Group account for managing access rights.</span></span><br/>                              |
| <span data-ttu-id="10695-116">UserGroupCollection</span><span class="sxs-lookup"><span data-stu-id="10695-116">UserGroupCollection</span></span><br/> | <span data-ttu-id="10695-117">Set di gruppi di utenti che implementa [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span><span class="sxs-lookup"><span data-stu-id="10695-117">A set of user groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/>  |
| <span data-ttu-id="10695-118">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="10695-118">GroupCollection</span></span><br/>     | <span data-ttu-id="10695-119">Un set di altri gruppi che implementano [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span><span class="sxs-lookup"><span data-stu-id="10695-119">A set of other groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/> |
| <span data-ttu-id="10695-120">Computer</span><span class="sxs-lookup"><span data-stu-id="10695-120">Computer</span></span><br/>            | <span data-ttu-id="10695-121">Server o workstation Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="10695-121">Windows NT 4.0 server or workstation.</span></span><br/>                                  |
| <span data-ttu-id="10695-122">PrintJob</span><span class="sxs-lookup"><span data-stu-id="10695-122">PrintJob</span></span><br/>            | <span data-ttu-id="10695-123">Processo di stampa nella coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="10695-123">Print job in the print queue.</span></span><br/>                                          |
| <span data-ttu-id="10695-124">PrintJobsCollection</span><span class="sxs-lookup"><span data-stu-id="10695-124">PrintJobsCollection</span></span><br/> | <span data-ttu-id="10695-125">Set di processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="10695-125">A set of print jobs.</span></span><br/>                                                   |
| <span data-ttu-id="10695-126">PrintQueue</span><span class="sxs-lookup"><span data-stu-id="10695-126">PrintQueue</span></span><br/>          | <span data-ttu-id="10695-127">Coda di stampa sullo spooler di una stampante.</span><span class="sxs-lookup"><span data-stu-id="10695-127">Print queue on a printer spooler.</span></span><br/>                                      |
| <span data-ttu-id="10695-128">Servizio</span><span class="sxs-lookup"><span data-stu-id="10695-128">Service</span></span><br/>             | <span data-ttu-id="10695-129">Applicazione in esecuzione come servizio.</span><span class="sxs-lookup"><span data-stu-id="10695-129">Application running as a service.</span></span><br/>                                      |
| <span data-ttu-id="10695-130">FileService</span><span class="sxs-lookup"><span data-stu-id="10695-130">FileService</span></span><br/>         | <span data-ttu-id="10695-131">Servizi che accedono a file system.</span><span class="sxs-lookup"><span data-stu-id="10695-131">Services accessing file system.</span></span><br/>                                        |
| <span data-ttu-id="10695-132">FileShare</span><span class="sxs-lookup"><span data-stu-id="10695-132">FileShare</span></span><br/>           | <span data-ttu-id="10695-133">Punto di condivisione file.</span><span class="sxs-lookup"><span data-stu-id="10695-133">File share point.</span></span><br/>                                                      |
| <span data-ttu-id="10695-134">Risorsa</span><span class="sxs-lookup"><span data-stu-id="10695-134">Resource</span></span><br/>            | <span data-ttu-id="10695-135">Risorsa nel servizio.</span><span class="sxs-lookup"><span data-stu-id="10695-135">A resource in the service.</span></span><br/>                                             |
| <span data-ttu-id="10695-136">Sessione</span><span class="sxs-lookup"><span data-stu-id="10695-136">Session</span></span><br/>             | <span data-ttu-id="10695-137">Connessione al servizio file attiva.</span><span class="sxs-lookup"><span data-stu-id="10695-137">An active file service connection.</span></span><br/>                                     |
| <span data-ttu-id="10695-138">User</span><span class="sxs-lookup"><span data-stu-id="10695-138">User</span></span><br/>                | <span data-ttu-id="10695-139">Account utente locale.</span><span class="sxs-lookup"><span data-stu-id="10695-139">Local user account.</span></span><br/>                                                    |
| <span data-ttu-id="10695-140">Group</span><span class="sxs-lookup"><span data-stu-id="10695-140">Group</span></span><br/>               | <span data-ttu-id="10695-141">Gruppo locale.</span><span class="sxs-lookup"><span data-stu-id="10695-141">Local group.</span></span><br/>                                                           |
| <span data-ttu-id="10695-142">UserCollection</span><span class="sxs-lookup"><span data-stu-id="10695-142">UserCollection</span></span><br/>      | <span data-ttu-id="10695-143">Raccolta di utenti locali.</span><span class="sxs-lookup"><span data-stu-id="10695-143">Collection of local users.</span></span><br/>                                             |
| <span data-ttu-id="10695-144">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="10695-144">GroupCollection</span></span><br/>     | <span data-ttu-id="10695-145">Raccolta di gruppi locali.</span><span class="sxs-lookup"><span data-stu-id="10695-145">Collection of local groups.</span></span><br/>                                            |
| <span data-ttu-id="10695-146">SCHEMA</span><span class="sxs-lookup"><span data-stu-id="10695-146">Schema</span></span><br/>              | <span data-ttu-id="10695-147">Contenitore dello schema WinNT.</span><span class="sxs-lookup"><span data-stu-id="10695-147">WinNT Schema container.</span></span><br/>                                                |
| <span data-ttu-id="10695-148">Classe</span><span class="sxs-lookup"><span data-stu-id="10695-148">Class</span></span><br/>               | <span data-ttu-id="10695-149">Definizione della classe dello schema.</span><span class="sxs-lookup"><span data-stu-id="10695-149">Schema class definition.</span></span><br/>                                               |
| <span data-ttu-id="10695-150">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10695-150">Property</span></span><br/>            | <span data-ttu-id="10695-151">Definizione dell'attributo dello schema.</span><span class="sxs-lookup"><span data-stu-id="10695-151">Schema attribute definition.</span></span><br/>                                           |
| <span data-ttu-id="10695-152">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10695-152">Syntax</span></span><br/>              | <span data-ttu-id="10695-153">Sintassi di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="10695-153">Syntax of a property.</span></span><br/>                                                  |



 

 

 





