---
description: Il tipo formattato di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Tipo formattato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049702"
---
# <a name="formatted-type"></a><span data-ttu-id="19bee-103">Tipo formattato</span><span class="sxs-lookup"><span data-stu-id="19bee-103">Formatted Type</span></span>

<span data-ttu-id="19bee-104">Il tipo formattato di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="19bee-104">The Formatted Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="19bee-105">Questo tipo è costituito da una stringa di testo arbitraria di qualsiasi lunghezza fornita dall'utente e nel formato di testo formattato Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="19bee-105">This type consists of an arbitrary text string of any length provided by the user and in the Windows Installer formatted text format.</span></span> <span data-ttu-id="19bee-106">Per informazioni dettagliate, vedere [formattato](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="19bee-106">For details, see [Formatted](formatted.md).</span></span> <span data-ttu-id="19bee-107">Lo strumento di merge sostituisce questa stringa nei modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="19bee-107">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="19bee-108">Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna nome, immettere "0" nella colonna formato, immettere "formattato" nella colonna tipo e lasciare vuota la colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md). La stringa può essere in qualsiasi linguaggio compatibile con la tabella codici del database.</span><span class="sxs-lookup"><span data-stu-id="19bee-108">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Formatted" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="19bee-109">Per informazioni dettagliate, vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="19bee-109">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="19bee-110">Null è un valore valido per la stringa di testo a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="19bee-110">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



