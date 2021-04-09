---
description: ICE79 convalida i riferimenti ai componenti e alle funzionalità immessi nei campi del database usando il tipo di dati Condition.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129966"
---
# <a name="ice79"></a><span data-ttu-id="903e2-103">ICE79</span><span class="sxs-lookup"><span data-stu-id="903e2-103">ICE79</span></span>

<span data-ttu-id="903e2-104">ICE79 convalida i riferimenti ai componenti e alle funzionalità immessi nei campi del database usando il tipo di dati [Condition](condition.md) .</span><span class="sxs-lookup"><span data-stu-id="903e2-104">ICE79 validates the references to components and features entered in the database fields using the [Condition](condition.md) data type.</span></span>

## <a name="result"></a><span data-ttu-id="903e2-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="903e2-105">Result</span></span>

<span data-ttu-id="903e2-106">ICE79 invia due avvisi.</span><span class="sxs-lookup"><span data-stu-id="903e2-106">ICE79 posts two warnings.</span></span>



| <span data-ttu-id="903e2-107">Avviso di ICE79</span><span class="sxs-lookup"><span data-stu-id="903e2-107">ICE79 warning</span></span>                                                                      | <span data-ttu-id="903e2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="903e2-108">Description</span></span>                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="903e2-109">Nel database manca la \_ tabella di convalida.</span><span class="sxs-lookup"><span data-stu-id="903e2-109">Database is missing \_Validation table.</span></span> <span data-ttu-id="903e2-110">Non è stato possibile controllare completamente i nomi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="903e2-110">Could not completely check property names.</span></span> | <span data-ttu-id="903e2-111">Nel database manca la [ \_ tabella di convalida](-validation-table.md).</span><span class="sxs-lookup"><span data-stu-id="903e2-111">Database is missing [\_Validation table](-validation-table.md).</span></span> |
| <span data-ttu-id="903e2-112">Errore durante il recupero dei valori dalla colonna \[ 2 \] nella tabella \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="903e2-112">Error retrieving values from column \[2\] in table \[1\].</span></span> <span data-ttu-id="903e2-113">Colonna ignorata.</span><span class="sxs-lookup"><span data-stu-id="903e2-113">Skipping Column.</span></span>         | <span data-ttu-id="903e2-114">Errore durante il recupero del valore.</span><span class="sxs-lookup"><span data-stu-id="903e2-114">Error retrieving value.</span></span>                                          |



 

<span data-ttu-id="903e2-115">ICE79 invia due errori.</span><span class="sxs-lookup"><span data-stu-id="903e2-115">ICE79 posts two errors.</span></span>



| <span data-ttu-id="903e2-116">Errore ICE79</span><span class="sxs-lookup"><span data-stu-id="903e2-116">ICE79 error</span></span>                                                          | <span data-ttu-id="903e2-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="903e2-117">Description</span></span>                               |
|----------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="903e2-118">Si fa riferimento al componente '% ls ' nella colonna '% s'. % s'della riga% s non è valido.</span><span class="sxs-lookup"><span data-stu-id="903e2-118">Component '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span> | <span data-ttu-id="903e2-119">È stato trovato un riferimento a un componente non valido.</span><span class="sxs-lookup"><span data-stu-id="903e2-119">An invalid component reference was found.</span></span> |
| <span data-ttu-id="903e2-120">Funzione '% ls ' a cui viene fatto riferimento nella colonna '% s'.' % s'della riga% s non è valido.</span><span class="sxs-lookup"><span data-stu-id="903e2-120">Feature '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span>   | <span data-ttu-id="903e2-121">È stato trovato un riferimento alla funzionalità non valido</span><span class="sxs-lookup"><span data-stu-id="903e2-121">An invalid feature reference was found</span></span>    |



 

## <a name="example"></a><span data-ttu-id="903e2-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="903e2-122">Example</span></span>

<span data-ttu-id="903e2-123">ICE79 segnala gli errori seguenti per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="903e2-123">ICE79 reports the following errors for the example:</span></span>

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

<span data-ttu-id="903e2-124">In questo esempio, NoSuchComponent è assente dalla [tabella Component](component-table.md) e NoSuchFeature è assente dalla [tabella Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="903e2-124">In this example, NoSuchComponent is absent from the [Component table](component-table.md) and NoSuchFeature is absent from the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="903e2-125">[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="903e2-125">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="903e2-126">Azione</span><span class="sxs-lookup"><span data-stu-id="903e2-126">Action</span></span>  | <span data-ttu-id="903e2-127">Condizione</span><span class="sxs-lookup"><span data-stu-id="903e2-127">Condition</span></span>                                |
|---------|------------------------------------------|
| <span data-ttu-id="903e2-128">Personalizzata1</span><span class="sxs-lookup"><span data-stu-id="903e2-128">Custom1</span></span> | <span data-ttu-id="903e2-129">TESTACTION = 1046 e &NoSuchFeature>2</span><span class="sxs-lookup"><span data-stu-id="903e2-129">TESTACTION=1046 AND &NoSuchFeature>2</span></span>  |
| <span data-ttu-id="903e2-130">Custom2</span><span class="sxs-lookup"><span data-stu-id="903e2-130">Custom2</span></span> | <span data-ttu-id="903e2-131">TESTACTION = 146 e $NoSuchComponent>2</span><span class="sxs-lookup"><span data-stu-id="903e2-131">TESTACTION=146 AND $NoSuchComponent>2</span></span> |



 

<span data-ttu-id="903e2-132">Per correggere questi errori, immettere record validi per NoSuchFeature e NoSuchComponent nelle tabelle feature e Component.</span><span class="sxs-lookup"><span data-stu-id="903e2-132">To fix these errors, enter valid records for NoSuchFeature and NoSuchComponent in the Feature and Component tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="903e2-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="903e2-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="903e2-134">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="903e2-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



