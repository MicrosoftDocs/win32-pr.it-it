---
description: Questi valori vengono utilizzati con la composizione ImmGetCompositionString e WM \_ IME \_ .
ms.assetid: 14087598-8041-4e02-a168-f5538a437be0
title: Valori stringa di composizione IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5b3935329e56f015cdb08a764e1660142a067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879562"
---
# <a name="ime-composition-string-values"></a><span data-ttu-id="1d710-103">Valori stringa di composizione IME</span><span class="sxs-lookup"><span data-stu-id="1d710-103">IME Composition String Values</span></span>

<span data-ttu-id="1d710-104">Questi valori vengono utilizzati con la composizione [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) e [**WM \_ IME \_**](wm-ime-composition.md).</span><span class="sxs-lookup"><span data-stu-id="1d710-104">These values are used with [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) and [**WM\_IME\_COMPOSITION**](wm-ime-composition.md).</span></span>



| <span data-ttu-id="1d710-105">Valore</span><span class="sxs-lookup"><span data-stu-id="1d710-105">Value</span></span>                 | <span data-ttu-id="1d710-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d710-106">Description</span></span>                                                                                |
|-----------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d710-107">comaccarezzatore cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-107">GCS\_COMPATTR</span></span>         | <span data-ttu-id="1d710-108">Recuperare o aggiornare l'attributo della stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="1d710-108">Retrieve or update the attribute of the composition string.</span></span>                                |
| <span data-ttu-id="1d710-109">COMPCLAUSE cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-109">GCS\_COMPCLAUSE</span></span>       | <span data-ttu-id="1d710-110">Recuperare o aggiornare le informazioni sulla clausola della stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="1d710-110">Retrieve or update clause information of the composition string.</span></span>                           |
| <span data-ttu-id="1d710-111">COMPREADATTR cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-111">GCS\_COMPREADATTR</span></span>     | <span data-ttu-id="1d710-112">Recuperare o aggiornare gli attributi della stringa di lettura della composizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1d710-112">Retrieve or update the attributes of the reading string of the current composition.</span></span>        |
| <span data-ttu-id="1d710-113">COMPREADCLAUSE cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-113">GCS\_COMPREADCLAUSE</span></span>   | <span data-ttu-id="1d710-114">Recuperare o aggiornare le informazioni sulla clausola della stringa di lettura della stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="1d710-114">Retrieve or update the clause information of the reading string of the composition string.</span></span> |
| <span data-ttu-id="1d710-115">COMPREADSTR cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-115">GCS\_COMPREADSTR</span></span>      | <span data-ttu-id="1d710-116">Recupera o aggiorna la stringa di lettura della composizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1d710-116">Retrieve or update the reading string of the current composition.</span></span>                          |
| <span data-ttu-id="1d710-117">COMPSTR cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-117">GCS\_COMPSTR</span></span>          | <span data-ttu-id="1d710-118">Recupera o aggiorna la stringa di composizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1d710-118">Retrieve or update the current composition string.</span></span>                                         |
| <span data-ttu-id="1d710-119">CURSORPOS cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-119">GCS\_CURSORPOS</span></span>        | <span data-ttu-id="1d710-120">Recupera o aggiorna la posizione del cursore nella stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="1d710-120">Retrieve or update the cursor position in composition string.</span></span>                              |
| <span data-ttu-id="1d710-121">DELTASTART cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-121">GCS\_DELTASTART</span></span>       | <span data-ttu-id="1d710-122">Recuperare o aggiornare la posizione iniziale di tutte le modifiche nella stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="1d710-122">Retrieve or update the starting position of any changes in composition string.</span></span>             |
| <span data-ttu-id="1d710-123">RESULTCLAUSE cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-123">GCS\_RESULTCLAUSE</span></span>     | <span data-ttu-id="1d710-124">Recuperare o aggiornare le informazioni sulla clausola della stringa di risultato.</span><span class="sxs-lookup"><span data-stu-id="1d710-124">Retrieve or update clause information of the result string.</span></span>                                |
| <span data-ttu-id="1d710-125">RESULTREADCLAUSE cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-125">GCS\_RESULTREADCLAUSE</span></span> | <span data-ttu-id="1d710-126">Recuperare o aggiornare le informazioni sulla clausola della stringa di lettura.</span><span class="sxs-lookup"><span data-stu-id="1d710-126">Retrieve or update clause information of the reading string.</span></span>                               |
| <span data-ttu-id="1d710-127">RESULTREADSTR cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-127">GCS\_RESULTREADSTR</span></span>    | <span data-ttu-id="1d710-128">Recuperare o aggiornare la stringa di lettura.</span><span class="sxs-lookup"><span data-stu-id="1d710-128">Retrieve or update the reading string.</span></span>                                                     |
| <span data-ttu-id="1d710-129">RESULTSTR cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="1d710-129">GCS\_RESULTSTR</span></span>        | <span data-ttu-id="1d710-130">Recuperare o aggiornare la stringa del risultato della composizione.</span><span class="sxs-lookup"><span data-stu-id="1d710-130">Retrieve or update the string of the composition result.</span></span>                                   |



 

 

 



