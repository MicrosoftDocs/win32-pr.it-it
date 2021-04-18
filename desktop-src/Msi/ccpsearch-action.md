---
description: L'azione CCPSearch usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Azione CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310998"
---
# <a name="ccpsearch-action"></a><span data-ttu-id="11293-103">Azione CCPSearch</span><span class="sxs-lookup"><span data-stu-id="11293-103">CCPSearch Action</span></span>

<span data-ttu-id="11293-104">L'azione CCPSearch usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="11293-104">The CCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="11293-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="11293-105">Sequence Restrictions</span></span>

<span data-ttu-id="11293-106">È necessario creare l'azione CCPSearch nella tabella [InstallUISequence](installuisequence-table.md) e nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="11293-106">CCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="11293-107">Il programma di installazione impedisce l'esecuzione dell'azione CCPSearch nella sequenza InstallExecuteSequence se l'azione è già stata eseguita nella sequenza InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="11293-107">The installer prevents the CCPSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span> <span data-ttu-id="11293-108">L'azione CCPSearch deve precedere l'azione [RMCCPSearch](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="11293-108">The CCPSearch action must come before the [RMCCPSearch](rmccpsearch-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="11293-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="11293-109">ActionData Messages</span></span>

<span data-ttu-id="11293-110">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="11293-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="11293-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="11293-111">Remarks</span></span>

<span data-ttu-id="11293-112">L'azione CCPSearch Cerca le firme dei file elencate nella tabella CCPSearch del sistema usando le tabelle seguenti nell'ordine: Signature, CompLocator, RegLocator, IniLocator e DrLocator.</span><span class="sxs-lookup"><span data-stu-id="11293-112">The CCPSearch action searches for file signatures listed in the CCPSearch table on the system using the following tables in order: Signature, CompLocator, RegLocator, IniLocator, and DrLocator.</span></span>

<span data-ttu-id="11293-113">Se viene determinata una firma esistente, la proprietà **CCP \_ Success** è impostata su 1 e l'azione CCPSearch termina.</span><span class="sxs-lookup"><span data-stu-id="11293-113">If any signature is determined to exist, the **CCP\_Success** property is set to 1 and the CCPSearch action terminates.</span></span>

<span data-ttu-id="11293-114">L'assenza della firma dalla tabella delle firme indica una directory.</span><span class="sxs-lookup"><span data-stu-id="11293-114">The absence of the signature from the Signature table denotes a directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11293-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11293-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11293-116">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="11293-116">CCPSearch</span></span>](ccpsearch-table.md)
</dt> <dt>

[<span data-ttu-id="11293-117">Firma</span><span class="sxs-lookup"><span data-stu-id="11293-117">Signature</span></span>](signature-table.md)
</dt> <dt>

[<span data-ttu-id="11293-118">CompLocator</span><span class="sxs-lookup"><span data-stu-id="11293-118">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="11293-119">RegLocator</span><span class="sxs-lookup"><span data-stu-id="11293-119">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="11293-120">IniLocator</span><span class="sxs-lookup"><span data-stu-id="11293-120">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="11293-121">DrLocator</span><span class="sxs-lookup"><span data-stu-id="11293-121">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



