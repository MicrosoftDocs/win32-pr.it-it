---
description: Il tipo di icona del tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave nella tabella delle icone fornita dall'utente.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Tipo di icona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7c90de925ff34977e7ff192dffe0b8614e5734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308188"
---
# <a name="icon-type"></a><span data-ttu-id="0d57d-104">Tipo di icona</span><span class="sxs-lookup"><span data-stu-id="0d57d-104">Icon Type</span></span>

<span data-ttu-id="0d57d-105">Il tipo di icona del [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="0d57d-105">The Icon Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="0d57d-106">Questo tipo è costituito da una chiave nella [tabella delle icone](icon-table.md) fornita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0d57d-106">This type consists of a key into the [Icon table](icon-table.md) provided by the user.</span></span>

<span data-ttu-id="0d57d-107">Lo strumento di merge deve sostituire un [identificatore](identifier.md) Windows Installer valido per gli elementi di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="0d57d-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="0d57d-108">Mergemod.dll non impone questa restrizione ed è attivo lo strumento di merge per assicurarsi che l'utente fornisca una chiave valida nella tabella delle icone.</span><span class="sxs-lookup"><span data-stu-id="0d57d-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Icon table.</span></span>

<span data-ttu-id="0d57d-109">Null è un valore valido per questo tipo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="0d57d-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="0d57d-110">Il tipo binario può essere utilizzato con i tipi di ContextData seguenti.</span><span class="sxs-lookup"><span data-stu-id="0d57d-110">The Binary type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="0d57d-111">**ContextData ShortcutIcon**</span><span class="sxs-lookup"><span data-stu-id="0d57d-111">**ShortcutIcon ContextData**</span></span>

<span data-ttu-id="0d57d-112">Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una chiave esterna a una riga nella [tabella delle icone](icon-table.md) che contiene un'immagine adatta per l'utilizzo come icona di collegamento.</span><span class="sxs-lookup"><span data-stu-id="0d57d-112">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the [Icon Table](icon-table.md) that contains an image suitable for use as a shortcut icon.</span></span> <span data-ttu-id="0d57d-113">Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "Icon" nella colonna tipo e immettere "ShorcutIcon" nella colonna ContextData della tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d57d-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Icon" into the Type column, and enter "ShorcutIcon" into the ContextData column of the ModuleConfiguration table.</span></span> <span data-ttu-id="0d57d-114">Questo tipo non è appropriato per l'utilizzo in una tabella dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0d57d-114">This type is not appropriate for use in a user interface table.</span></span> <span data-ttu-id="0d57d-115">Per modificare una chiave nella tabella delle icone in queste tabelle, vedere icona ContextData in [tipo binario](binary-type.md).</span><span class="sxs-lookup"><span data-stu-id="0d57d-115">To modify a key to the Icon table in these tables see Icon ContextData under [Binary Type](binary-type.md).</span></span>

 

 



