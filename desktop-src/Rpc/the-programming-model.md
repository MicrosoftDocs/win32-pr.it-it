---
title: Modello di programmazione
description: Nei primi giorni della programmazione del computer, ogni programma è stato scritto come un blocco monolitico di grandi dimensioni, riempito con istruzioni GOTO.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710894"
---
# <a name="the-programming-model"></a><span data-ttu-id="bb000-103">Modello di programmazione</span><span class="sxs-lookup"><span data-stu-id="bb000-103">The Programming Model</span></span>

<span data-ttu-id="bb000-104">Nei primi giorni della programmazione del computer, ogni programma è stato scritto come un blocco monolitico di grandi dimensioni, riempito con istruzioni **goto** .</span><span class="sxs-lookup"><span data-stu-id="bb000-104">In the early days of computer programming, each program was written as a large monolithic chunk, filled with **goto** statements.</span></span> <span data-ttu-id="bb000-105">Ogni programma doveva gestire un input e un output propri a dispositivi hardware diversi.</span><span class="sxs-lookup"><span data-stu-id="bb000-105">Each program had to manage its own input and output to different hardware devices.</span></span> <span data-ttu-id="bb000-106">Con la maturità della disciplina di programmazione, questo codice monolitico è stato organizzato in procedure, con le procedure utilizzate più di frequente nelle librerie per la condivisione e il riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="bb000-106">As the programming discipline matured, this monolithic code was organized into procedures, with the most commonly used procedures packed in libraries for sharing and reuse.</span></span>

![istruzioni goto monolitiche rispetto alle procedure compresse in librerie condivise](images/prog-a06.png)

<span data-ttu-id="bb000-108">Il linguaggio di programmazione C supporta la programmazione orientata a procedure.</span><span class="sxs-lookup"><span data-stu-id="bb000-108">The C programming language supports procedure-oriented programming.</span></span> <span data-ttu-id="bb000-109">In C, la procedura principale si riferisce a tutte le altre procedure come caselle nere.</span><span class="sxs-lookup"><span data-stu-id="bb000-109">In C, the main procedure relates to all other procedures as black boxes.</span></span> <span data-ttu-id="bb000-110">La procedura principale, ad esempio, non è in grado di determinare il funzionamento delle procedure A, B e X.</span><span class="sxs-lookup"><span data-stu-id="bb000-110">For example, the main procedure cannot find out how procedures A, B, and X do their work.</span></span> <span data-ttu-id="bb000-111">La routine Main chiama solo un'altra procedura. non sono disponibili informazioni sulla modalità di implementazione di tale procedura.</span><span class="sxs-lookup"><span data-stu-id="bb000-111">The main procedure only calls another procedure; it has no information about how that procedure is implemented.</span></span>

![isolamento delle attività eseguite in procedure esterne](images/prog-a08.png)

<span data-ttu-id="bb000-113">I linguaggi di programmazione orientati alle procedure forniscono semplici meccanismi per specificare e scrivere procedure.</span><span class="sxs-lookup"><span data-stu-id="bb000-113">Procedure-oriented programming languages provide simple mechanisms for specifying and writing procedures.</span></span> <span data-ttu-id="bb000-114">Il prototipo di funzione C-standard ANSI, ad esempio, è un costrutto usato per specificare il nome di una routine, il tipo del risultato restituito (se presente) e il numero, la sequenza e il tipo dei relativi parametri.</span><span class="sxs-lookup"><span data-stu-id="bb000-114">For example, the ANSI-standard C-function prototype is a construct used to specify the name of a procedure, the type of the result it returns (if any) and the number, sequence, and type of its parameters.</span></span> <span data-ttu-id="bb000-115">L'utilizzo del prototipo di funzione è un metodo formale per specificare un'interfaccia tra le routine.</span><span class="sxs-lookup"><span data-stu-id="bb000-115">Using the function prototype is a formal way to specify an interface between procedures.</span></span>

<span data-ttu-id="bb000-116">Microsoft RPC si basa sul modello di programmazione, consentendo alle procedure, raggruppate in interfacce, di risiedere in processi diversi rispetto al chiamante.</span><span class="sxs-lookup"><span data-stu-id="bb000-116">Microsoft RPC builds on that programming model by allowing procedures, grouped together in interfaces, to reside in different processes than the caller.</span></span> <span data-ttu-id="bb000-117">Microsoft RPC aggiunge inoltre un approccio più formale alla definizione della procedura che consente al chiamante e alla routine chiamata di adottare un contratto per lo scambio remoto di dati e la chiamata di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bb000-117">Microsoft RPC also adds a more formal approach to procedure definition that allows the caller and the called routine to adopt a contract for remotely exchanging data and invoking functionality.</span></span> <span data-ttu-id="bb000-118">Nel modello di programmazione RPC Microsoft, le chiamate di funzione tradizionali sono integrate con due elementi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="bb000-118">In the Microsoft RPC programming model, traditional function calls are supplemented with two additional elements.</span></span>

-   <span data-ttu-id="bb000-119">Il primo elemento è un file. idl/. ACF che descrive esattamente lo scambio di dati e il meccanismo di passaggio del parametro tra il chiamante e la routine chiamata.</span><span class="sxs-lookup"><span data-stu-id="bb000-119">The first element is an .idl/.acf file that precisely describes the data exchange and parameter-passing mechanism between the caller and called procedure.</span></span>
-   <span data-ttu-id="bb000-120">Il secondo elemento è un set di API di runtime che forniscono agli sviluppatori un controllo granulare della chiamata di procedura remota, inclusi gli aspetti di sicurezza, la gestione dello stato sul server, l'indicazione dei client che possono comunicare con il server e così via.</span><span class="sxs-lookup"><span data-stu-id="bb000-120">The second element is a set of run-time APIs that provide developers with granular control of the remote procedure call, including security aspects, managing state on the server, specifying which clients can talk to the server, and so on.</span></span>

 

 




