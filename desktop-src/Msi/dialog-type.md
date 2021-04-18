---
description: Il tipo di finestra di dialogo di tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave esterna nella tabella della finestra di dialogo fornita dall'utente.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Tipo di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314281"
---
# <a name="dialog-type"></a><span data-ttu-id="4b9d5-104">Tipo di dialogo</span><span class="sxs-lookup"><span data-stu-id="4b9d5-104">Dialog Type</span></span>

<span data-ttu-id="4b9d5-105">Il tipo di finestra di dialogo di [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="4b9d5-105">The Dialog Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="4b9d5-106">Questo tipo è costituito da una chiave esterna nella [tabella della finestra di dialogo](dialog-table.md) fornita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-106">This type consists of a foreign key into the [Dialog table](dialog-table.md) provided by the user.</span></span>

<span data-ttu-id="4b9d5-107">Lo strumento di merge deve sostituire un [identificatore](identifier.md) Windows Installer valido per gli elementi di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="4b9d5-108">Mergemod.dll non impone questa restrizione ed è attivo lo strumento di merge per assicurarsi che l'utente fornisca una chiave valida nella tabella della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Dialog table.</span></span>

<span data-ttu-id="4b9d5-109">Null è un valore valido per questo tipo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="4b9d5-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="4b9d5-110">Il tipo di finestra di dialogo può essere utilizzato con i tipi di ContextData seguenti.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-110">The Dialog type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="4b9d5-111">**ContextData DialogNext**</span><span class="sxs-lookup"><span data-stu-id="4b9d5-111">**DialogNext ContextData**</span></span>

<span data-ttu-id="4b9d5-112">Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una chiave esterna nella tabella della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-112">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="4b9d5-113">Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "finestra di dialogo" nella colonna tipo e immettere "DialogNext" nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="4b9d5-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogNext" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="4b9d5-114">**ContextData DialogPrev**</span><span class="sxs-lookup"><span data-stu-id="4b9d5-114">**DialogPrev ContextData**</span></span>

<span data-ttu-id="4b9d5-115">Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una chiave esterna nella tabella della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-115">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="4b9d5-116">Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "finestra di dialogo" nella colonna tipo e immettere "DialogPrev" nella colonna ContextData della tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-116">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogPrev" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



