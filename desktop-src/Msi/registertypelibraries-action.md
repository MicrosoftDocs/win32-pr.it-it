---
description: L'azione RegisterTypeLibraries registra le librerie dei tipi con il sistema. Questa azione viene applicata a ogni file a cui si fa riferimento nella tabella TypeLib pianificata per l'installazione.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Azione RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311706"
---
# <a name="registertypelibraries-action"></a><span data-ttu-id="8a0c4-104">Azione RegisterTypeLibraries</span><span class="sxs-lookup"><span data-stu-id="8a0c4-104">RegisterTypeLibraries Action</span></span>

<span data-ttu-id="8a0c4-105">L'azione RegisterTypeLibraries registra le librerie dei tipi con il sistema.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-105">The RegisterTypeLibraries action registers type libraries with the system.</span></span> <span data-ttu-id="8a0c4-106">Questa azione viene applicata a ogni file a cui si fa riferimento nella [tabella TypeLib](typelib-table.md) pianificata per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-106">This action is applied to each file referred to in the [TypeLib table](typelib-table.md) that is scheduled for install.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8a0c4-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="8a0c4-107">Sequence Restrictions</span></span>

<span data-ttu-id="8a0c4-108">L'azione RegisterTypeLibraries deve essere successiva all'azione [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8a0c4-108">The RegisterTypeLibraries action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8a0c4-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="8a0c4-109">ActionData Messages</span></span>



| <span data-ttu-id="8a0c4-110">Campo</span><span class="sxs-lookup"><span data-stu-id="8a0c4-110">Field</span></span> | <span data-ttu-id="8a0c4-111">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="8a0c4-111">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="8a0c4-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8a0c4-112">\[1\]</span></span> | <span data-ttu-id="8a0c4-113">[GUID](guid.md) della libreria dei tipi registrati.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-113">[GUID](guid.md) of registered type library.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8a0c4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a0c4-114">Remarks</span></span>

<span data-ttu-id="8a0c4-115">Per l'azione RegisterTypeLibraries è necessario che il linguaggio della libreria dei tipi venga creato correttamente nel campo Language della tabella TypeLib.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-115">The RegisterTypeLibraries action requires that the type library language be correctly authored in the Language field of the TypeLib table.</span></span> <span data-ttu-id="8a0c4-116">Una modifica errata del campo del linguaggio può causare la mancata registrazione di una libreria dei tipi altrimenti valida nel programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-116">Incorrect authoring of the Language field can cause the installer to fail to register an otherwise valid type library.</span></span>

 

 



