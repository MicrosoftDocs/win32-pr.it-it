---
title: Chiamate annidate a SRSetRestorePoint
description: In questo argomento viene descritto il supporto per le chiamate annidate a SRSetRestorePoint tramite i tipi di evento BEGIN NESTED \_ \_ System change \_ e End \_ Nested \_ System \_ Change.
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221533"
---
# <a name="nested-calls-to-srsetrestorepoint"></a><span data-ttu-id="98e36-103">Chiamate annidate a SRSetRestorePoint</span><span class="sxs-lookup"><span data-stu-id="98e36-103">Nested Calls to SRSetRestorePoint</span></span>

<span data-ttu-id="98e36-104">In questo argomento viene descritto il supporto per le chiamate annidate a [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) tramite i tipi di evento Begin nested \_ System change \_ \_ e End \_ Nested \_ System \_ Change.</span><span class="sxs-lookup"><span data-stu-id="98e36-104">This topic describes support for nested calls to [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) through the BEGIN\_NESTED\_SYSTEM\_CHANGE and END\_NESTED\_SYSTEM\_CHANGE event types.</span></span>

<span data-ttu-id="98e36-105">Quando si usano questi tipi di evento, le applicazioni possono chiamare [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="98e36-105">Applications can safely call [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) when using these event types.</span></span> <span data-ttu-id="98e36-106">La prima chiamata alla funzione crea un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="98e36-106">The first call to the function creates a restore point.</span></span> <span data-ttu-id="98e36-107">Le successive chiamate annidate alla funzione non creano punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="98e36-107">Subsequent nested calls to the function do not create restore points.</span></span> <span data-ttu-id="98e36-108">Si supponga, ad esempio, che un'applicazione effettua le chiamate seguenti a **SRSetRestorePoint**:</span><span class="sxs-lookup"><span data-stu-id="98e36-108">For example, suppose an application makes the following calls to **SRSetRestorePoint**:</span></span><dl> <span data-ttu-id="98e36-109">Per il punto di ripristino A con dwEventType = inizio \_ \_ modifica sistema annidato \_</span><span class="sxs-lookup"><span data-stu-id="98e36-109">For restore point A with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="98e36-110">Per il punto di ripristino B con dwEventType = BEGIN \_ Nested \_ System \_ Change</span><span class="sxs-lookup"><span data-stu-id="98e36-110">For restore point B with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="98e36-111">Per il punto di ripristino B con dwEventType = END \_ Nested \_ System \_ Change</span><span class="sxs-lookup"><span data-stu-id="98e36-111">For restore point B with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="98e36-112">Per il punto di ripristino A con dwEventType = fine \_ \_ modifica sistema annidato \_</span><span class="sxs-lookup"><span data-stu-id="98e36-112">For restore point A with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
</dl>

<span data-ttu-id="98e36-113">La seconda chiamata non crea un nuovo punto di ripristino perché la chiamata è annidata.</span><span class="sxs-lookup"><span data-stu-id="98e36-113">The second call does not create a new restore point because the call is nested.</span></span>

 

 




