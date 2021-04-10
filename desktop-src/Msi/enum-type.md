---
description: Il tipo enum del tipo semantico è uno dei tipi di formato testo.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Tipo enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967145"
---
# <a name="enum-type"></a><span data-ttu-id="cd0b7-103">Tipo enum</span><span class="sxs-lookup"><span data-stu-id="cd0b7-103">Enum Type</span></span>

<span data-ttu-id="cd0b7-104">Il tipo enum del [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="cd0b7-104">The Enum Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="cd0b7-105">Questo tipo è costituito da una stringa di testo scelta dall'utente da un set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-105">This type consists of a text string chosen by the user from a set of choices.</span></span> <span data-ttu-id="cd0b7-106">Lo strumento di merge sostituisce la stringa selezionata selezionata nei modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="cd0b7-106">The merge tool substitutes the selected string selected into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="cd0b7-107">Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna nome, immettere "0" nella colonna formato, immettere "enum" nella colonna tipo e immettere l'elenco di stringhe possibili nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="cd0b7-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Enum" into the Type column, and enter the list of possible strings in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="cd0b7-108">L'elenco di stringhe possibili deve essere fornito come un elenco di stringhe deliminated da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-108">The list of possible strings must be provided as a list of strings deliminated by semicolons.</span></span> <span data-ttu-id="cd0b7-109">Ogni scelta deve avere il formato "nome = valore".</span><span class="sxs-lookup"><span data-stu-id="cd0b7-109">Each choice must be in the form "Name=Value".</span></span> <span data-ttu-id="cd0b7-110">È possibile aggiungere un punto e virgola letterale al valore anteponendo il punto e virgola con un carattere barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-110">A literal semicolon can be added to the value by prefixing the semicolon with a backslash character.</span></span> <span data-ttu-id="cd0b7-111">Null è un valore valido a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-111">Null is a valid value unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



