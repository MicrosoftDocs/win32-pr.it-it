---
description: Il valore logico di una proprietà impostata è true.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Uso delle proprietà nelle istruzioni condizionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307240"
---
# <a name="using-properties-in-conditional-statements"></a><span data-ttu-id="d0c19-103">Uso delle proprietà nelle istruzioni condizionali</span><span class="sxs-lookup"><span data-stu-id="d0c19-103">Using Properties in Conditional Statements</span></span>

<span data-ttu-id="d0c19-104">Il valore logico di una proprietà impostata è true.</span><span class="sxs-lookup"><span data-stu-id="d0c19-104">The logical value of a property that has been set is True.</span></span> <span data-ttu-id="d0c19-105">Per determinare se una proprietà è impostata senza ottenere effettivamente il relativo valore, testare l'espressione logica "SetProperty" o "not SetProperty".</span><span class="sxs-lookup"><span data-stu-id="d0c19-105">To determine whether a property is set without actually getting its value, test the logical expression "MyProperty" or "Not MyProperty".</span></span> <span data-ttu-id="d0c19-106">Quando viene impostata la proprietà Property, il primo restituisce true e il secondo come false.</span><span class="sxs-lookup"><span data-stu-id="d0c19-106">When the property MyProperty is set, the former evaluates as True and the latter as False.</span></span>

<span data-ttu-id="d0c19-107">Una o più proprietà possono essere combinate con operatori per formare espressioni logiche utilizzate in un'istruzione condizionale.</span><span class="sxs-lookup"><span data-stu-id="d0c19-107">One or more properties can be combined with operators to form logical expressions used in a conditional statements.</span></span> <span data-ttu-id="d0c19-108">Per ulteriori informazioni sugli operatori che possono essere utilizzati nelle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d0c19-108">For more information about the operators that can be used in conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="d0c19-109">È possibile immettere un'istruzione condizionale che utilizza proprietà nella colonna condizione della [tabella Condition](condition-table.md) per modificare lo stato di selezione di qualsiasi voce nella [tabella Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0c19-109">A conditional statement using properties can be entered into the Condition column of the [Condition table](condition-table.md) to modify the selection state of any entry in the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="d0c19-110">Le istruzioni condizionali con una o più proprietà vengono comunemente utilizzate nella colonna condizione delle tabelle di database.</span><span class="sxs-lookup"><span data-stu-id="d0c19-110">Conditional statements with one or more properties are commonly used in the Condition column of database tables.</span></span>

<span data-ttu-id="d0c19-111">Le tabelle seguenti includono ognuna una colonna per le espressioni condizionali:</span><span class="sxs-lookup"><span data-stu-id="d0c19-111">The following tables each have a column for conditional expressions:</span></span>

-   [<span data-ttu-id="d0c19-112">Tabella Condition</span><span class="sxs-lookup"><span data-stu-id="d0c19-112">Condition table</span></span>](condition-table.md)
-   [<span data-ttu-id="d0c19-113">Tabella ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d0c19-113">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="d0c19-114">Tabella LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="d0c19-114">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="d0c19-115">Tabella InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="d0c19-115">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="d0c19-116">Tabella InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="d0c19-116">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="d0c19-117">Tabella ControlCondition</span><span class="sxs-lookup"><span data-stu-id="d0c19-117">ControlCondition table</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="d0c19-118">Tabella AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="d0c19-118">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="d0c19-119">Tabella AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="d0c19-119">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="d0c19-120">Tabella AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="d0c19-120">AdminUISequence table</span></span>](adminuisequence-table.md)

<span data-ttu-id="d0c19-121">Si noti che le sei tabelle di sequenza delle azioni hanno campi per una condizione.</span><span class="sxs-lookup"><span data-stu-id="d0c19-121">Note that the six action sequence tables have fields for a condition.</span></span> <span data-ttu-id="d0c19-122">Se l'espressione condizionale in questo campo restituisce false, l'azione verrà ignorata dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="d0c19-122">If the conditional expression in this field evaluates to False, the installer skips that action.</span></span>

<span data-ttu-id="d0c19-123">Se si imposta una [proprietà privata](private-properties.md) nella sequenza dell'interfaccia utente creando un'azione personalizzata in una delle tabelle di sequenza dell'interfaccia utente, tale proprietà non viene impostata nella sequenza di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d0c19-123">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="d0c19-124">Per impostare la proprietà nella sequenza di esecuzione, è inoltre necessario inserire un'azione personalizzata in una tabella della sequenza di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d0c19-124">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="d0c19-125">In alternativa, è possibile rendere la proprietà una [proprietà pubblica](public-properties.md) e includerla nella proprietà [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="d0c19-125">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="d0c19-126">Per ulteriori informazioni, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md) o [utilizzo delle proprietà](using-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d0c19-126">For more information, see [Using a Sequence Table](using-a-sequence-table.md) or [Using Properties](using-properties.md).</span></span>

 

 



