---
description: Le specifiche di esempio includono l'invio di messaggi ActionData quando un'azione personalizzata crea o rimuove un account utente e segnala un errore se non è possibile creare un account.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Creazione di tabelle ActionText e Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881097"
---
# <a name="authoring-the-actiontext-and-error-tables"></a><span data-ttu-id="6e1bf-103">Creazione di tabelle ActionText e Error</span><span class="sxs-lookup"><span data-stu-id="6e1bf-103">Authoring the ActionText and Error Tables</span></span>

<span data-ttu-id="6e1bf-104">Le specifiche di esempio includono l'invio di messaggi ActionData quando un'azione personalizzata crea o rimuove un account utente e segnala un errore se non è possibile creare un account.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-104">The sample specifications include sending ActionData messages when a custom action creates or removes a user account, and reporting an error if an account cannot be created.</span></span>

<span data-ttu-id="6e1bf-105">Immettere le voci seguenti nella tabella ActionText per fornire le informazioni usate dai messaggi di ActionText.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-105">Enter the following entries into the ActionText table to provide information used by ActionText messages.</span></span>

[<span data-ttu-id="6e1bf-106">Tabella ActionText</span><span class="sxs-lookup"><span data-stu-id="6e1bf-106">ActionText Table</span></span>](actiontext-table.md)



| <span data-ttu-id="6e1bf-107">Azione</span><span class="sxs-lookup"><span data-stu-id="6e1bf-107">Action</span></span>            | <span data-ttu-id="6e1bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e1bf-108">Description</span></span>                                                       | <span data-ttu-id="6e1bf-109">Modello</span><span class="sxs-lookup"><span data-stu-id="6e1bf-109">Template</span></span>                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="6e1bf-110">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="6e1bf-110">ProcessAccounts</span></span>   | <span data-ttu-id="6e1bf-111">Generazione di azioni per la creazione di account utente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-111">Generating actions to create user accounts on the local computer.</span></span> | <span data-ttu-id="6e1bf-112">Account: \[ 1 \] , attributi: \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="6e1bf-112">Account: \[1\], Attributes: \[2\]</span></span> |
| <span data-ttu-id="6e1bf-113">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="6e1bf-113">CreateAccount</span></span>     | <span data-ttu-id="6e1bf-114">Creazione dell'account utente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-114">Creating user account on the local computer.</span></span>                      | <span data-ttu-id="6e1bf-115">Account: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="6e1bf-115">Account: \[1\]</span></span>                    |
| <span data-ttu-id="6e1bf-116">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="6e1bf-116">RemoveAccount</span></span>     | <span data-ttu-id="6e1bf-117">Rimozione dell'account utente dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-117">Removing user account from the local computer.</span></span>                    | <span data-ttu-id="6e1bf-118">Account: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="6e1bf-118">Account: \[1\]</span></span>                    |
| <span data-ttu-id="6e1bf-119">RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="6e1bf-119">RollbackAccount</span></span>   | <span data-ttu-id="6e1bf-120">Rollback della creazione degli account utente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-120">Rolling back the creation of user accounts on the local computer.</span></span> | <span data-ttu-id="6e1bf-121">Account: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="6e1bf-121">Account: \[1\]</span></span>                    |
| <span data-ttu-id="6e1bf-122">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="6e1bf-122">UninstallAccounts</span></span> | <span data-ttu-id="6e1bf-123">Generazione di azioni per la rimozione di account utente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-123">Generating actions to remove user accounts on the local computer.</span></span> | <span data-ttu-id="6e1bf-124">Account: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="6e1bf-124">Account: \[1\]</span></span>                    |



 

<span data-ttu-id="6e1bf-125">Immettere le voci seguenti nella tabella degli errori per fornire informazioni utilizzate da segnalazione errori.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-125">Enter the following entries into the Error table to provide information used by error reporting.</span></span>

[<span data-ttu-id="6e1bf-126">Tabella degli errori</span><span class="sxs-lookup"><span data-stu-id="6e1bf-126">Error Table</span></span>](error-table.md)



| <span data-ttu-id="6e1bf-127">Errore</span><span class="sxs-lookup"><span data-stu-id="6e1bf-127">Error</span></span> | <span data-ttu-id="6e1bf-128">Message</span><span class="sxs-lookup"><span data-stu-id="6e1bf-128">Message</span></span>                                                                        |
|-------|--------------------------------------------------------------------------------|
| <span data-ttu-id="6e1bf-129">25001</span><span class="sxs-lookup"><span data-stu-id="6e1bf-129">25001</span></span> | <span data-ttu-id="6e1bf-130">Non è possibile creare l'account utente ' \[ 2 \] ' nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-130">Unable to create user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="6e1bf-131">Codice di errore: \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="6e1bf-131">Error Code: \[3\].</span></span> |
| <span data-ttu-id="6e1bf-132">25002</span><span class="sxs-lookup"><span data-stu-id="6e1bf-132">25002</span></span> | <span data-ttu-id="6e1bf-133">L'account utente ' \[ 2 \] ' esiste già nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-133">User account '\[2\]' already exists on the local machine.</span></span>                      |
| <span data-ttu-id="6e1bf-134">25003</span><span class="sxs-lookup"><span data-stu-id="6e1bf-134">25003</span></span> | <span data-ttu-id="6e1bf-135">Non è possibile rimuovere l'account utente ' \[ 2 \] ' nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-135">Unable to remove user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="6e1bf-136">Codice di errore: \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="6e1bf-136">Error Code: \[3\].</span></span> |
| <span data-ttu-id="6e1bf-137">25004</span><span class="sxs-lookup"><span data-stu-id="6e1bf-137">25004</span></span> | <span data-ttu-id="6e1bf-138">L'account utente ' \[ 2 \] ' non esiste nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="6e1bf-138">User account '\[2\]' does not exist on the local machine.</span></span>                      |



 

<span data-ttu-id="6e1bf-139">Continuare con [la creazione della tabella InstallExecuteSequence](authoring-the-installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6e1bf-139">Continue to [Authoring the InstallExecuteSequence Table](authoring-the-installexecutesequence-table.md).</span></span>

 

 



