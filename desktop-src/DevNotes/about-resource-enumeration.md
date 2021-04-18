---
description: L'enumerazione Resource fornisce una visualizzazione accurata e precisa dell'attività di strumentazione che si verifica quando un'applicazione è in esecuzione.
ms.assetid: 4a421006-32ff-4555-a3c8-69fffdb46845
title: Informazioni sull'enumerazione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601e65550dacbd07d493f35a6c35fece98657b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304412"
---
# <a name="about-resource-enumeration"></a><span data-ttu-id="c9b38-103">Informazioni sull'enumerazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="c9b38-103">About Resource Enumeration</span></span>

<span data-ttu-id="c9b38-104">L'enumerazione Resource fornisce una visualizzazione accurata e precisa dell'attività di strumentazione che si verifica quando un'applicazione è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c9b38-104">Resource enumeration provides a close and precise view of instrumentation activity that takes place when an application is running.</span></span> <span data-ttu-id="c9b38-105">Le informazioni di strumentazione possono essere astratte e categorizzate come un set di elementi specifici del processo come parte del processo di debug.</span><span class="sxs-lookup"><span data-stu-id="c9b38-105">The instrumentation information can be abstracted and categorized as a set of process-specific items as part of the debugging process.</span></span>

<span data-ttu-id="c9b38-106">Gli strumenti, ad esempio i debugger, richiedono spesso l'accesso alle informazioni di strumentazione, ma potrebbero trovarlo non disponibile.</span><span class="sxs-lookup"><span data-stu-id="c9b38-106">Tools, such as debuggers, often require access to instrumentation information but may find it is unavailable.</span></span> <span data-ttu-id="c9b38-107">Per risolvere questo problema, la funzione [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) estrae questo tipo di informazioni dalle applicazioni per fornire informazioni di contesto migliori per il problema di cui è in corso il debug.</span><span class="sxs-lookup"><span data-stu-id="c9b38-107">To solve this problem, the [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) function extracts this type of information from applications to provide better context information for the problem being debugged.</span></span>

 

 



