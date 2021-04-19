---
description: Il tipo di testo arbitrario di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Tipo di testo arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311054"
---
# <a name="arbitrary-text-type"></a><span data-ttu-id="3b303-103">Tipo di testo arbitrario</span><span class="sxs-lookup"><span data-stu-id="3b303-103">Arbitrary Text Type</span></span>

<span data-ttu-id="3b303-104">Il tipo di testo arbitrario di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="3b303-104">The Arbitrary Text Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="3b303-105">Questo tipo è costituito da una stringa di testo arbitraria di qualsiasi lunghezza fornita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3b303-105">This type consists of an arbitrary text string of any length provided by the user.</span></span> <span data-ttu-id="3b303-106">Lo strumento di merge sostituisce questa stringa arbitraria nei modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="3b303-106">The merge tool substitutes this arbitrary string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="3b303-107">Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna nome, immettere "0" nella colonna formato e lasciare vuote le colonne Type e ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md). La stringa di testo arbitrario può essere in qualsiasi linguaggio compatibile con la tabella codici del database.</span><span class="sxs-lookup"><span data-stu-id="3b303-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).The arbitrary text string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="3b303-108">Per informazioni dettagliate, vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="3b303-108">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="3b303-109">Null è un valore valido per la stringa di testo a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3b303-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



