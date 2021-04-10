---
title: Interfacce private Container-Specific
description: Interfacce private Container-Specific
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332359"
---
# <a name="container-specific-private-interfaces"></a><span data-ttu-id="330bc-103">Interfacce private Container-Specific</span><span class="sxs-lookup"><span data-stu-id="330bc-103">Container-Specific Private Interfaces</span></span>

<span data-ttu-id="330bc-104">Alcuni contenitori forniscono interfacce private specifiche del contenitore per funzionalità aggiuntive o prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="330bc-104">Some containers provide container-specific private interfaces for additional functionality or improved performance.</span></span> <span data-ttu-id="330bc-105">I controlli basati su tali interfacce specifiche del contenitore dovrebbero, se possibile, funzionare senza le interfacce specifiche del contenitore presenti, in modo che il controllo funzioni in contenitori diversi.</span><span class="sxs-lookup"><span data-stu-id="330bc-105">Controls that rely on those container-specific interfaces should, if possible, work without those container-specific interfaces present so that the control functions in different containers.</span></span> <span data-ttu-id="330bc-106">Ad esempio, Visual Basic implementa interfacce private che forniscono la funzionalità di formattazione delle stringhe ai controlli.</span><span class="sxs-lookup"><span data-stu-id="330bc-106">For example, Visual Basic implements private interfaces that provide string formatting functionality to controls.</span></span> <span data-ttu-id="330bc-107">Se un controllo Usa queste interfacce di formattazione privata, dovrebbe essere in grado di eseguire con il supporto predefinito per la formattazione se queste interfacce non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="330bc-107">If a control makes use of these private formatting interfaces, it should be able to run with default formatting support if these interfaces are not available.</span></span> <span data-ttu-id="330bc-108">Se il controllo può funzionare senza le interfacce private, deve adottare un'azione appropriata, ad esempio avvisare l'utente di una funzionalità ridotta, ma continuare a lavorare.</span><span class="sxs-lookup"><span data-stu-id="330bc-108">If the control can function without the private interfaces, it should take appropriate action (such as warn the user of reduced functionality) but continue to work.</span></span> <span data-ttu-id="330bc-109">Se non si tratta di un'opzione, la categoria di un componente deve essere registrata come richiesto, in modo che solo i contenitori che supportano questa funzionalità possano ospitare tali controlli.</span><span class="sxs-lookup"><span data-stu-id="330bc-109">If this is not an option, a component category should be registered as required so that only containers supporting this functionality can host these controls.</span></span>

 

 




