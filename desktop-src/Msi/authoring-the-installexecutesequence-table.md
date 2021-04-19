---
description: Le azioni personalizzate ProcessAccounts e UninstallAccounts generano le azioni personalizzate posticipate che creano, rimuovono o ripristinano gli account utente.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Creazione della tabella InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311032"
---
# <a name="authoring-the-installexecutesequence-table"></a><span data-ttu-id="e574a-103">Creazione della tabella InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="e574a-103">Authoring the InstallExecuteSequence Table</span></span>

<span data-ttu-id="e574a-104">Le azioni personalizzate ProcessAccounts e UninstallAccounts generano le azioni personalizzate posticipate che creano, rimuovono o ripristinano gli account utente.</span><span class="sxs-lookup"><span data-stu-id="e574a-104">The custom actions ProcessAccounts and UninstallAccounts generate the deferred custom actions that create, remove, or rollback user accounts.</span></span> <span data-ttu-id="e574a-105">È necessario immettere le azioni personalizzate ProcessAccounts e UninstallAccounts nella [tabella InstallExecuteSequence](installexecutesequence-table.md) da eseguire.</span><span class="sxs-lookup"><span data-stu-id="e574a-105">The custom actions ProcessAccounts and UninstallAccounts must be entered into the [InstallExecuteSequence table](installexecutesequence-table.md) to be executed.</span></span> <span data-ttu-id="e574a-106">Aggiungere le voci seguenti alla [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="e574a-106">Add the following entries to the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="e574a-107">Poiché queste azioni personalizzate devono far parte della generazione di script, entrambe le azioni personalizzate devono essere sequenziate dopo l' [azione InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e574a-107">Because these custom actions must be a part of the script generation, both custom actions must be sequenced after the [InstallInitialize action](installinitialize-action.md).</span></span>

<span data-ttu-id="e574a-108">La condizione in ProcessAccounts garantisce quanto segue.</span><span class="sxs-lookup"><span data-stu-id="e574a-108">The condition on ProcessAccounts ensures the following.</span></span> <span data-ttu-id="e574a-109">Vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e574a-109">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

-   <span data-ttu-id="e574a-110">ProcessAccounts viene eseguito solo se il componente TestAccount viene installato localmente nel computer.</span><span class="sxs-lookup"><span data-stu-id="e574a-110">ProcessAccounts runs only if the component TestAccount is being installed locally on the computer.</span></span>
-   <span data-ttu-id="e574a-111">L'account di test del componente non è attualmente installato o è installato per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="e574a-111">The component Test Account is currently not installed or is installed to run from the source.</span></span>

<span data-ttu-id="e574a-112">La condizione in UninstallAccount garantisce quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e574a-112">The condition on UninstallAccount ensures the following:</span></span>

-   <span data-ttu-id="e574a-113">UninstallAccounts viene eseguito solo se il componente TestAccount è installato localmente nel computer.</span><span class="sxs-lookup"><span data-stu-id="e574a-113">UninstallAccounts runs only if the component TestAccount is installed locally on the computer.</span></span>
-   <span data-ttu-id="e574a-114">L'account di test del componente verrà rimosso o installato per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="e574a-114">The component Test Account is being removed or being installed to run from the source.</span></span>

[<span data-ttu-id="e574a-115">Tabella InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="e574a-115">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="e574a-116">Azione</span><span class="sxs-lookup"><span data-stu-id="e574a-116">Action</span></span>            | <span data-ttu-id="e574a-117">Condizione</span><span class="sxs-lookup"><span data-stu-id="e574a-117">Condition</span></span>                                                           | <span data-ttu-id="e574a-118">Sequenza</span><span class="sxs-lookup"><span data-stu-id="e574a-118">Sequence</span></span> |
|-------------------|---------------------------------------------------------------------|----------|
| <span data-ttu-id="e574a-119">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="e574a-119">ProcessAccounts</span></span>   | <span data-ttu-id="e574a-120">VersionNT e (? TestAccount = 2 o? TestAccount = 4) e $TestAccount = 3</span><span class="sxs-lookup"><span data-stu-id="e574a-120">VersionNT AND (?TestAccount=2 OR ?TestAccount=4) AND $TestAccount=3</span></span> | <span data-ttu-id="e574a-121">1550</span><span class="sxs-lookup"><span data-stu-id="e574a-121">1550</span></span>     |
| <span data-ttu-id="e574a-122">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="e574a-122">UninstallAccounts</span></span> | <span data-ttu-id="e574a-123">VersionNT e? TestAccount = 3 e ($TestAccount = 4 o $TestAccount = 2)</span><span class="sxs-lookup"><span data-stu-id="e574a-123">VersionNT AND ?TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2)</span></span> | <span data-ttu-id="e574a-124">1560</span><span class="sxs-lookup"><span data-stu-id="e574a-124">1560</span></span>     |



 

<span data-ttu-id="e574a-125">Continuare a [creare l'interfaccia utente per l'input della password](authoring-the-user-interface-for-password-input.md).</span><span class="sxs-lookup"><span data-stu-id="e574a-125">Continue to [Authoring the user interface for password input](authoring-the-user-interface-for-password-input.md).</span></span>

 

 



