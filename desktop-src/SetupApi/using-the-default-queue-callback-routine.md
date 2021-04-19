---
description: La routine di callback della coda predefinita può essere specificata per gestire le notifiche inviate da SetupCommitFileQueue oppure può essere chiamata da una routine di callback personalizzata che si basa sulla funzionalità della routine di callback della coda predefinita.
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: Uso della routine di callback della coda predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311920"
---
# <a name="using-the-default-queue-callback-routine"></a><span data-ttu-id="84643-103">Uso della routine di callback della coda predefinita</span><span class="sxs-lookup"><span data-stu-id="84643-103">Using the Default Queue Callback Routine</span></span>

<span data-ttu-id="84643-104">La routine di callback della coda predefinita può essere specificata per gestire le notifiche inviate da [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)oppure può essere chiamata da una routine di callback personalizzata che si basa sulla funzionalità della routine di callback della coda predefinita.</span><span class="sxs-lookup"><span data-stu-id="84643-104">The default queue callback routine can be specified to handle notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), or it can be called by a custom callback routine that builds on the functionality of the default queue callback routine.</span></span>

<span data-ttu-id="84643-105">Nelle sezioni seguenti viene illustrato come inizializzare e terminare il contesto utilizzato da una routine di callback della coda predefinita.</span><span class="sxs-lookup"><span data-stu-id="84643-105">The following sections explain how to initialize and terminate the context used by a default queue callback routine.</span></span> <span data-ttu-id="84643-106">Le sezioni descrivono anche come usare la routine di callback della coda predefinita con [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) o una routine di callback personalizzata.</span><span class="sxs-lookup"><span data-stu-id="84643-106">The sections also describe how to use the default queue callback routine with [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) or a custom callback routine.</span></span>

-   [<span data-ttu-id="84643-107">Inizializzazione e terminazione del contesto di callback</span><span class="sxs-lookup"><span data-stu-id="84643-107">Initializing and Terminating the Callback Context</span></span>](initializing-and-terminating-the-callback-context.md)
-   [<span data-ttu-id="84643-108">Chiamata della routine di callback della coda predefinita</span><span class="sxs-lookup"><span data-stu-id="84643-108">Calling the Default Queue Callback Routine</span></span>](calling-the-default-queue-callback-routine.md)

 

 



