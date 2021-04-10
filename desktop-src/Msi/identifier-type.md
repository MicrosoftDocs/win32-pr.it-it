---
description: Il tipo di identificatore di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Tipo di identificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131482"
---
# <a name="identifier-type"></a><span data-ttu-id="eb099-103">Tipo di identificatore</span><span class="sxs-lookup"><span data-stu-id="eb099-103">Identifier Type</span></span>

<span data-ttu-id="eb099-104">Il tipo di identificatore di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="eb099-104">The Identifier Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="eb099-105">Questo tipo è costituito da una stringa di testo fornita dall'utente nel formato di un [identificatore](identifier.md)Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="eb099-105">This type consists of an text string provided by the user in the format of a Windows Installer [Identifier](identifier.md).</span></span> <span data-ttu-id="eb099-106">Lo strumento di merge sostituisce questa stringa nei modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb099-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="eb099-107">Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna nome, immettere "0" nella colonna formato, immettere "Identifier" nella colonna tipo e lasciare vuota la colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md). La stringa può essere in qualsiasi linguaggio compatibile con la tabella codici del database.</span><span class="sxs-lookup"><span data-stu-id="eb099-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Identifier" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="eb099-108">Vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="eb099-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="eb099-109">Null è un valore valido per la stringa di testo a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="eb099-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



