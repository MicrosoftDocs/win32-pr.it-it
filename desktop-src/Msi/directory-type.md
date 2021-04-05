---
description: Il tipo di directory di tipo semantico è uno dei tipi di formato chiave, costituito da una chiave esterna nella tabella di directory fornita dall'utente.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Tipo di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882981"
---
# <a name="directory-type"></a><span data-ttu-id="3d816-103">Tipo di directory</span><span class="sxs-lookup"><span data-stu-id="3d816-103">Directory Type</span></span>

<span data-ttu-id="3d816-104">Il tipo di directory di [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md), costituito da una chiave esterna nella tabella di [directory](directory-table.md) fornita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3d816-104">The Directory Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md), which consists of a foreign key into the [Directory table](directory-table.md) provided by the user.</span></span>

<span data-ttu-id="3d816-105">Lo strumento di merge deve sostituire un [identificatore](identifier.md) Windows Installer valido per gli elementi di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="3d816-105">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="3d816-106">Mergemod.dll non impone questa restrizione ed è attivo lo strumento di merge per assicurarsi che l'utente fornisca una chiave valida nella tabella di directory.</span><span class="sxs-lookup"><span data-stu-id="3d816-106">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Directory table.</span></span>

<span data-ttu-id="3d816-107">Un elemento configurabile del tipo di directory deve modificare solo la directory di destinazione dell'installazione e non modificare l'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="3d816-107">A configurable item of the Directory type should only modify the destination directory of the installation and not modify the source image.</span></span> <span data-ttu-id="3d816-108">Un elemento configurabile di questo tipo deve pertanto modificare solo le chiavi esterne nella tabella di directory senza modificare direttamente la tabella di directory.</span><span class="sxs-lookup"><span data-stu-id="3d816-108">A configurable item of this type should therefore only modify foreign keys to the Directory table and not modify the Directory table directly.</span></span>

<span data-ttu-id="3d816-109">Poiché la \_ colonna di directory della [tabella dei componenti](component-table.md) è non nullable, null è un valore non valido per un elemento configurabile di questo tipo anche se msmConfigItemNonNullable non è impostato nella colonna Attributes.</span><span class="sxs-lookup"><span data-stu-id="3d816-109">Because the Directory\_ column of the [Component table](component-table.md) is non-nullable, null is an invalid value for a configurable item of this type even if the msmConfigItemNonNullable is not set in the Attributes column.</span></span>

<span data-ttu-id="3d816-110">Il tipo di directory può essere usato con due tipi di ContextData.</span><span class="sxs-lookup"><span data-stu-id="3d816-110">The Directory type may be used with two kinds of ContextData.</span></span>

<span data-ttu-id="3d816-111">**ContextData IsolationDirectory**</span><span class="sxs-lookup"><span data-stu-id="3d816-111">**IsolationDirectory ContextData**</span></span>

<span data-ttu-id="3d816-112">Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una directory di destinazione per i file del modulo.</span><span class="sxs-lookup"><span data-stu-id="3d816-112">A configurable merge module may use this type to enable the user to provide a destination directory for files in the module.</span></span> <span data-ttu-id="3d816-113">Lo strumento di merge sostituisce l'identificatore della directory nei modelli della colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="3d816-113">The merge tool substitutes the directory's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="3d816-114">Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della directory nella colonna nome, immettere "1" nella colonna formato, immettere "directory" nella colonna tipo e immettere "IsolationDirectory" nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="3d816-114">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "IsolationDirectory" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="3d816-115">**ContextData ShortcutLocation**</span><span class="sxs-lookup"><span data-stu-id="3d816-115">**ShortcutLocation ContextData**</span></span>

<span data-ttu-id="3d816-116">Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una directory di destinazione per i collegamenti nel modulo.</span><span class="sxs-lookup"><span data-stu-id="3d816-116">A configurable merge module may use this type to enable the user to provide a destination directory for shortcuts in the module.</span></span> <span data-ttu-id="3d816-117">Lo strumento di merge sostituisce l'identificatore del collegamento nei modelli della colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="3d816-117">The merge tool substitutes the shortcut's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="3d816-118">Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della directory nella colonna nome, immettere "1" nella colonna formato, immettere "directory" nella colonna tipo e immettere "ShortcutLocation" nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="3d816-118">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "ShortcutLocation" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



