---
description: ICE46 verifica la presenza di proprietà personalizzate in condizioni, testo formattato e altri percorsi diversi da una proprietà definita dal sistema solo in caso di uno o più caratteri.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756224"
---
# <a name="ice46"></a><span data-ttu-id="9bbb9-103">ICE46</span><span class="sxs-lookup"><span data-stu-id="9bbb9-103">ICE46</span></span>

<span data-ttu-id="9bbb9-104">ICE46 verifica la presenza di proprietà personalizzate in condizioni, testo formattato e altri percorsi diversi da una proprietà definita dal sistema solo in caso di uno o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-104">ICE46 checks for custom properties in conditions, formatted text, and other locations that differ from a system defined property only by the case of one or more characters.</span></span>

## <a name="result"></a><span data-ttu-id="9bbb9-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="9bbb9-105">Result</span></span>

<span data-ttu-id="9bbb9-106">ICE46 Invia un messaggio informativo se è presente una proprietà personalizzata in una condizione, in un testo formattato e in un'altra posizione diversa da una proprietà definita dal sistema solo nel caso di uno o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-106">ICE46 posts an informational message if there is a custom property in a condition, formatted text, and other location that differs from a system defined properties only in the case of one or more characters.</span></span>

## <a name="example"></a><span data-ttu-id="9bbb9-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="9bbb9-107">Example</span></span>

<span data-ttu-id="9bbb9-108">ICE46 segnala gli errori seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-108">ICE46 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="9bbb9-109">Errore ICE46</span><span class="sxs-lookup"><span data-stu-id="9bbb9-109">ICE46 error</span></span>                                                                                                                                            | <span data-ttu-id="9bbb9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bbb9-110">Description</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bbb9-111">La proprietà ReinstallMode definita nella tabella delle proprietà differisce da un'altra proprietà definita solo per caso.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-111">Property ReinstallMode defined in property table differs from another defined property only by case.</span></span>                                                   | <span data-ttu-id="9bbb9-112">Il nome di proprietà definito dal sistema **REINSTALLMODE** differisce dalla proprietà personalizzata solo per caso.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-112">The system defined property name **REINSTALLMODE** differs from the custom property by case only.</span></span> <span data-ttu-id="9bbb9-113">Le proprietà fanno distinzione tra maiuscole e minuscole, pertanto la proprietà personalizzata non corrisponde alla proprietà di sistema.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-113">Properties are case sensitive, so custom property is not the same as the system property.</span></span> <span data-ttu-id="9bbb9-114">Si tratta di una delle cause comuni degli errori.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-114">This is a common cause of errors.</span></span> |
| <span data-ttu-id="9bbb9-115">Proprietà' setProperty ' a cui viene fatto riferimento nella colonna ' InstallExecuteSequence '. La condizione ' della riga ' InstallFinalize ' differisce da una proprietà definita solo per caso.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-115">Property 'Myproperty' referenced in column 'InstallExecuteSequence'.'Condition' of row 'InstallFinalize' differs from a defined property by case only.</span></span> | <span data-ttu-id="9bbb9-116">La tabella delle proprietà definisce la proprietà della tabella, ma la proprietà a cui si fa riferimento è SetProperty.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-116">The property table defines the table MyProperty, but the referenced property is Myproperty.</span></span> <span data-ttu-id="9bbb9-117">Le proprietà fanno distinzione tra maiuscole e minuscole, pertanto le due proprietà non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-117">Properties are case sensitive, so the two properties are NOT the same.</span></span> <span data-ttu-id="9bbb9-118">Si tratta di una delle cause comuni degli errori.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-118">This is a common cause of errors.</span></span>                          |



 

[<span data-ttu-id="9bbb9-119">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="9bbb9-119">Property Table</span></span>](property-table.md)



| <span data-ttu-id="9bbb9-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9bbb9-120">Property</span></span>      | <span data-ttu-id="9bbb9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9bbb9-121">Value</span></span>   |
|---------------|---------|
| <span data-ttu-id="9bbb9-122">ReinstallMode</span><span class="sxs-lookup"><span data-stu-id="9bbb9-122">ReinstallMode</span></span> | <span data-ttu-id="9bbb9-123">omus</span><span class="sxs-lookup"><span data-stu-id="9bbb9-123">omus</span></span>    |
| <span data-ttu-id="9bbb9-124">MyProperty</span><span class="sxs-lookup"><span data-stu-id="9bbb9-124">MyProperty</span></span>    | <span data-ttu-id="9bbb9-125">valore</span><span class="sxs-lookup"><span data-stu-id="9bbb9-125">a value</span></span> |



 

<span data-ttu-id="9bbb9-126">[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="9bbb9-126">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="9bbb9-127">Azione</span><span class="sxs-lookup"><span data-stu-id="9bbb9-127">Action</span></span>          | <span data-ttu-id="9bbb9-128">Condizione</span><span class="sxs-lookup"><span data-stu-id="9bbb9-128">Condition</span></span>  |
|-----------------|------------|
| <span data-ttu-id="9bbb9-129">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="9bbb9-129">InstallFinalize</span></span> | <span data-ttu-id="9bbb9-130">MyProperty</span><span class="sxs-lookup"><span data-stu-id="9bbb9-130">Myproperty</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9bbb9-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bbb9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bbb9-132">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="9bbb9-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



