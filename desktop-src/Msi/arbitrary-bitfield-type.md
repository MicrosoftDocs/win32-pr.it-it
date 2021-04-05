---
description: Il &\# 0034; Bit&\# 0034; tipo senza richieste di contesto che l'utente fornisca un Integer il cui valore viene usato per impostare uno o più bit in un bit. Questo testo può essere in qualsiasi linguaggio compatibile con la tabella codici del database.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Tipo bit arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131495"
---
# <a name="arbitrary-bitfield-type"></a><span data-ttu-id="476a4-104">Tipo bit arbitrario</span><span class="sxs-lookup"><span data-stu-id="476a4-104">Arbitrary Bitfield Type</span></span>

<span data-ttu-id="476a4-105">Il tipo "bit" senza richieste di contesto fornisce un Integer il cui valore viene usato per impostare uno o più bit in un bit.</span><span class="sxs-lookup"><span data-stu-id="476a4-105">The "Bitfield" type with no context requests that the user provide an integer whose value is used to set one or more bits in a bitfield.</span></span> <span data-ttu-id="476a4-106">Questo testo può essere in qualsiasi linguaggio compatibile con la tabella codici del database.</span><span class="sxs-lookup"><span data-stu-id="476a4-106">This text may be in any language compatible with the code page of the database.</span></span>

<span data-ttu-id="476a4-107">Il tipo di bit arbitrario di [tipo semantico](semantic-types.md) è uno dei tipi bit.</span><span class="sxs-lookup"><span data-stu-id="476a4-107">The Arbitrary Bitfield Type of [semantic type](semantic-types.md) is one of the Bitfield Types.</span></span> <span data-ttu-id="476a4-108">Questo tipo è costituito da un numero intero scelto dall'utente da un set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="476a4-108">This type consists of an integer chosen by the user from a set of choices.</span></span> <span data-ttu-id="476a4-109">Lo strumento di merge sostituisce l'intero selezionato con i modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="476a4-109">The merge tool substitutes the selected integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="476a4-110">Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento nella colonna nome, immettere "3" nella colonna formato, lasciare vuota la colonna tipo e immettere l'elenco dei possibili numeri interi nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="476a4-110">To specify a configurable item of this type, module authors should enter the name of the item into the Name column, enter "3" into the Format column, leave the Type column blank, and enter the list of possible integers in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="476a4-111">La colonna del tipo è riservata e deve essere null.</span><span class="sxs-lookup"><span data-stu-id="476a4-111">The Type column is reserved and must be null.</span></span> <span data-ttu-id="476a4-112">La voce nella colonna ContextData per tutti i tipi di formato bit deve avere il formato " <mask> ;<Name>=</span><span class="sxs-lookup"><span data-stu-id="476a4-112">The entry in the ContextData column for all Bitfield Format types must be in the form "<mask>;<Name>=</span></span><value><span data-ttu-id="476a4-113">;<Name>=</span><span class="sxs-lookup"><span data-stu-id="476a4-113">;<Name>=</span></span><value><span data-ttu-id="476a4-114">.... ", dove <mask> è un valore intero che indica i bit di interesse, <Name> è un nome visualizzato localizzabile per la scelta e</span><span class="sxs-lookup"><span data-stu-id="476a4-114">....", where <mask> is an integer value indicating the bits of interest, <Name> is a localizable display name for the choice, and</span></span> <value> <span data-ttu-id="476a4-115">è un valore integer decimale.</span><span class="sxs-lookup"><span data-stu-id="476a4-115">is a decimal integer value.</span></span> <span data-ttu-id="476a4-116">La colonna context è in uso [CMSM special format](cmsm-special-format.md) e per tutti i tipi bit.</span><span class="sxs-lookup"><span data-stu-id="476a4-116">The context column is in use [CMSM Special Format](cmsm-special-format.md) and for all bitfield types.</span></span> <span data-ttu-id="476a4-117">Un carattere letterale "=" o ";" può essere inserito nel <Name> campo anteponendo il carattere barra rovesciata (' \\ ').</span><span class="sxs-lookup"><span data-stu-id="476a4-117">A literal "=" or ";" character can be entered in the <Name> field by prefixing it with a backslash ('\\') character.</span></span>

 

 



