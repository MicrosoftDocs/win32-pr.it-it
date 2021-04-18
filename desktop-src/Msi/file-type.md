---
description: Il tipo di file di tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave esterna nella tabella file fornita dall'utente.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315474"
---
# <a name="file-type"></a><span data-ttu-id="c9efd-104">Tipo di file</span><span class="sxs-lookup"><span data-stu-id="c9efd-104">File Type</span></span>

<span data-ttu-id="c9efd-105">Il tipo di file di [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="c9efd-105">The File Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="c9efd-106">Questo tipo è costituito da una chiave esterna nella [tabella file](file-table.md) fornita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c9efd-106">This type consists of a foreign key into the [File table](file-table.md) provided by the user.</span></span>

<span data-ttu-id="c9efd-107">Il tipo di file può essere usato con i tipi di ContextData seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9efd-107">The File type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="c9efd-108">**ContextData AssemblyContext**</span><span class="sxs-lookup"><span data-stu-id="c9efd-108">**AssemblyContext ContextData**</span></span>

<span data-ttu-id="c9efd-109">Questo tipo può essere utilizzato per consentire agli utenti di configurare chiavi esterne per gli assembly Win32 o Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="c9efd-109">This type may be used to enable users to configure foreign keys to Win32 or common language runtime assemblies.</span></span> <span data-ttu-id="c9efd-110">Lo strumento di merge deve sostituire un [identificatore](identifier.md) Windows Installer per gli elementi di questo tipo nel modello nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="c9efd-110">The merge tool must substitute a Windows Installer [Identifier](identifier.md) for items of this type into the template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="c9efd-111">Mergemod.dll non impone questa operazione ed è lo strumento di merge per assicurarsi che l'utente fornisca una chiave valida nella tabella file.</span><span class="sxs-lookup"><span data-stu-id="c9efd-111">Mergemod.dll does not enforce this and it is up to the merge tool to ensure that the user provides a valid key into the File table.</span></span>

<span data-ttu-id="c9efd-112">Null è un valore valido per questo tipo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="c9efd-112">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



