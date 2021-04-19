---
description: I moduli merge richiedono raramente un'interfaccia utente.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Creazione di interfacce utente nei moduli merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311028"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a><span data-ttu-id="b27f6-103">Creazione di interfacce utente nei moduli merge</span><span class="sxs-lookup"><span data-stu-id="b27f6-103">Authoring User Interfaces in Merge Modules</span></span>

<span data-ttu-id="b27f6-104">I moduli merge richiedono raramente un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b27f6-104">Merge modules rarely require a user interface.</span></span> <span data-ttu-id="b27f6-105">Il rilascio di un modulo merge che contiene entrambi i componenti installabili e un'interfaccia utente limita la flessibilità dell'utente del modulo.</span><span class="sxs-lookup"><span data-stu-id="b27f6-105">Releasing a merge module that contains both installable components and a user interface ultimately restricts the flexibility of the module user.</span></span> <span data-ttu-id="b27f6-106">La combinazione di componenti e interfaccia utente in un modulo può impedire agli sviluppatori di usare la propria interfaccia utente o di fornire installazioni invisibili.</span><span class="sxs-lookup"><span data-stu-id="b27f6-106">Combining both components and UI into one module can prevent developers from using their own UI or from providing silent installations.</span></span> <span data-ttu-id="b27f6-107">Un'alternativa migliore consiste nel rilasciare due moduli unione, uno che installa automaticamente i componenti e un secondo modulo facoltativo che contiene l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b27f6-107">A better alternative is to release two merge modules, one that silently installs the components and a second optional module that contains the UI.</span></span> <span data-ttu-id="b27f6-108">Il modulo con l'interfaccia utente dovrebbe elencare il modulo Component nella [tabella ModuleDependency](moduledependency-table.md).</span><span class="sxs-lookup"><span data-stu-id="b27f6-108">The module with the UI should list the component module in its [ModuleDependency table](moduledependency-table.md).</span></span> <span data-ttu-id="b27f6-109">Questo metodo consente agli autori di moduli di fornire un'interfaccia utente senza forzarla sugli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="b27f6-109">This method enables module authors to provide a UI without forcing it on developers.</span></span>

<span data-ttu-id="b27f6-110">Quando le tabelle dell'interfaccia utente vengono utilizzate nei modelli unione, possono essere unite allo stesso modo di qualsiasi altra tabella.</span><span class="sxs-lookup"><span data-stu-id="b27f6-110">When UI tables are used in merge modules they can be merged in the same way as any other tables.</span></span>

 

 



