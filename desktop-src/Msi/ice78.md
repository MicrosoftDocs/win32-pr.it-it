---
description: ICE78 verifica che la tabella AdvtUISequence non esista o sia vuota. Questa operazione è necessaria perché durante la pubblicità non è consentita alcuna interfaccia utente.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129967"
---
# <a name="ice78"></a><span data-ttu-id="6b818-104">ICE78</span><span class="sxs-lookup"><span data-stu-id="6b818-104">ICE78</span></span>

<span data-ttu-id="6b818-105">ICE78 verifica che la [tabella AdvtUISequence](advtuisequence-table.md) non esista o sia vuota.</span><span class="sxs-lookup"><span data-stu-id="6b818-105">ICE78 verifies that the [AdvtUISequence table](advtuisequence-table.md) either does not exist or is empty.</span></span> <span data-ttu-id="6b818-106">Questa operazione è necessaria perché durante la pubblicità non è consentita alcuna interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6b818-106">This is required because no user interface is allowed during advertising.</span></span>

## <a name="result"></a><span data-ttu-id="6b818-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="6b818-107">Result</span></span>

<span data-ttu-id="6b818-108">ICE78 Invia un errore se la tabella AdvtUISequence esiste e non è vuota.</span><span class="sxs-lookup"><span data-stu-id="6b818-108">ICE78 posts an error if the AdvtUISequence table exists and is not empty.</span></span>

## <a name="example"></a><span data-ttu-id="6b818-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="6b818-109">Example</span></span>

<span data-ttu-id="6b818-110">ICE78 segnala l'errore seguente per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="6b818-110">ICE78 reports the following error for the example:</span></span>

<span data-ttu-id="6b818-111">L'azione ' action1' è stata trovata nella tabella AdvtUISequence.</span><span class="sxs-lookup"><span data-stu-id="6b818-111">Action 'Action1' found in AdvtUISequence table.</span></span> <span data-ttu-id="6b818-112">Non sono consentite interfacce utente durante la pubblicità.</span><span class="sxs-lookup"><span data-stu-id="6b818-112">No UI is allowed during advertising.</span></span> <span data-ttu-id="6b818-113">La tabella AdvtUISequence deve pertanto essere vuota o non presente.</span><span class="sxs-lookup"><span data-stu-id="6b818-113">Therefore AdvtUISequence table must be empty or not present.</span></span>

<span data-ttu-id="6b818-114">[Tabella AdvtUISequence](advtuisequence-table.md)(parziale)</span><span class="sxs-lookup"><span data-stu-id="6b818-114">[AdvtUISequence table](advtuisequence-table.md)(partial)</span></span>



| <span data-ttu-id="6b818-115">Azione</span><span class="sxs-lookup"><span data-stu-id="6b818-115">Action</span></span>  | <span data-ttu-id="6b818-116">Condizione</span><span class="sxs-lookup"><span data-stu-id="6b818-116">Condition</span></span> | <span data-ttu-id="6b818-117">Sequenza</span><span class="sxs-lookup"><span data-stu-id="6b818-117">Sequence</span></span> |
|---------|-----------|----------|
| <span data-ttu-id="6b818-118">Action1</span><span class="sxs-lookup"><span data-stu-id="6b818-118">Action1</span></span> | <span data-ttu-id="6b818-119">true</span><span class="sxs-lookup"><span data-stu-id="6b818-119">TRUE</span></span>      | <span data-ttu-id="6b818-120">1</span><span class="sxs-lookup"><span data-stu-id="6b818-120">1</span></span>        |



 

<span data-ttu-id="6b818-121">Per correggere l'errore, rimuovere "action1" dalla tabella oppure rimuovere la tabella.</span><span class="sxs-lookup"><span data-stu-id="6b818-121">To fix the error, either remove "Action1" from the table, or remove the table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b818-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b818-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b818-123">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="6b818-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



