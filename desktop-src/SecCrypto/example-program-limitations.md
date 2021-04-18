---
description: Limitazioni del programma di esempio
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Limitazioni del programma di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315388"
---
# <a name="example-program-limitations"></a><span data-ttu-id="e0b04-103">Limitazioni del programma di esempio</span><span class="sxs-lookup"><span data-stu-id="e0b04-103">Example Program Limitations</span></span>

<span data-ttu-id="e0b04-104">I principi delle procedure di programmazione valide non sono sempre seguiti in questi programmi di esempio per fornire codice più conciso e leggibile.</span><span class="sxs-lookup"><span data-stu-id="e0b04-104">Principles of good programming practice are not always followed in these sample programs in order to provide more concise, more readable code.</span></span> <span data-ttu-id="e0b04-105">In particolare:</span><span class="sxs-lookup"><span data-stu-id="e0b04-105">In particular:</span></span>

-   <span data-ttu-id="e0b04-106">Vengono visualizzate solo le risposte di errore limitate.</span><span class="sxs-lookup"><span data-stu-id="e0b04-106">Only limited error responses are shown.</span></span> <span data-ttu-id="e0b04-107">I programmi di lavoro devono sempre controllare i codici di errore restituiti ed eseguire le azioni appropriate quando viene rilevato un errore.</span><span class="sxs-lookup"><span data-stu-id="e0b04-107">Working programs should always check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="e0b04-108">Viene eseguita solo la memoria limitata e la gestione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e0b04-108">Only limited memory and resource management is done.</span></span> <span data-ttu-id="e0b04-109">Nei programmi in esecuzione, tutti gli [*hash*](../secgloss/h-gly.md) e le chiavi devono essere eliminati, è necessario liberare tutta la memoria allocata, tutti i file devono essere chiusi e tutti gli handle devono essere rilasciati.</span><span class="sxs-lookup"><span data-stu-id="e0b04-109">In working programs, all keys and [*hashes*](../secgloss/h-gly.md) should be destroyed, all allocated memory should be freed, all files should be closed, and all handles should be released.</span></span> <span data-ttu-id="e0b04-110">Questi programmi di esempio forniscono solo dimostrazioni limitate dell'utilizzo di funzioni che eseguono queste attività.</span><span class="sxs-lookup"><span data-stu-id="e0b04-110">These example programs provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="e0b04-111">Questi programmi di esempio non eseguono attività di memoria o di gestione delle risorse in caso di interruzione del programma a causa di errori.</span><span class="sxs-lookup"><span data-stu-id="e0b04-111">These example programs perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

 

 
