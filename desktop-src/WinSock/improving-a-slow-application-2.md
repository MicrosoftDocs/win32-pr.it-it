---
description: In questa sezione viene esaminata una parte di un'applicazione di esempio che opera sulla rete molto lentamente. In questa sezione vengono apportate modifiche al codice iniziale per migliorarne le prestazioni.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Miglioramento di un'applicazione lenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306951"
---
# <a name="improving-a-slow-application"></a><span data-ttu-id="c5929-104">Miglioramento di un'applicazione lenta</span><span class="sxs-lookup"><span data-stu-id="c5929-104">Improving a Slow Application</span></span>

<span data-ttu-id="c5929-105">In questa sezione viene esaminata una parte di un'applicazione di esempio che opera sulla rete molto lentamente.</span><span class="sxs-lookup"><span data-stu-id="c5929-105">This section examines a portion of a sample application that operates over the network very slowly.</span></span> <span data-ttu-id="c5929-106">In questa sezione vengono apportate modifiche al codice iniziale per migliorarne le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c5929-106">Throughout this section, modifications are made to the initial code to improve its performance.</span></span>

<span data-ttu-id="c5929-107">L'esempio fittizio è la parte aggiornata per un gioco denominato Life.</span><span class="sxs-lookup"><span data-stu-id="c5929-107">The mock sample is the updated portion for a game called Life.</span></span> <span data-ttu-id="c5929-108">L'applicazione viene scritta in modo che il client esegua i calcoli per gli aggiornamenti e li invii al server.</span><span class="sxs-lookup"><span data-stu-id="c5929-108">The application is written such that the client performs the calculations for the updates and sends them to the server.</span></span> <span data-ttu-id="c5929-109">Il server Visualizza quindi il campo relativo alla durata risultante.</span><span class="sxs-lookup"><span data-stu-id="c5929-109">The server then displays the resulting Life field.</span></span> <span data-ttu-id="c5929-110">L'output del client è un flusso di byte, raggruppati in tre (triplette), ognuno dei quali rappresenta un aggiornamento di una cella.</span><span class="sxs-lookup"><span data-stu-id="c5929-110">The output from the client is a stream of bytes, grouped in threes (triplets), each triplet representing one cell update.</span></span> <span data-ttu-id="c5929-111">I byte nella tripletta rappresentano rispettivamente la riga, la colonna e il valore per la cella.</span><span class="sxs-lookup"><span data-stu-id="c5929-111">The bytes in the triplet represent the row, column, and value, respectively, for the cell.</span></span>

<span data-ttu-id="c5929-112">Questo esempio inizia come un'applicazione intenzionalmente scadente, che fornisce la linea di base da cui è possibile illustrare i miglioramenti delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c5929-112">This sample begins as an intentionally poor performing application, which provides the baseline from which performance improvements can be illustrated.</span></span> <span data-ttu-id="c5929-113">A questo punto, il codice è migliorato tre volte per risolvere vari problemi che influiscono sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c5929-113">From there, the code is improved three times to address various issues that affect performance.</span></span> <span data-ttu-id="c5929-114">Questi esempi devono essere letti in ordine, in quanto ogni iterazione migliora la versione precedente.</span><span class="sxs-lookup"><span data-stu-id="c5929-114">These samples should be read in order, as each iteration improves on the previous version.</span></span>

<span data-ttu-id="c5929-115">Il codice di base e le revisioni che migliorano tale codice sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5929-115">The baseline code, and the revisions that improve that code, are the following:</span></span>

-   [<span data-ttu-id="c5929-116">Versione di base: applicazione con prestazioni molto scarsa</span><span class="sxs-lookup"><span data-stu-id="c5929-116">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
-   [<span data-ttu-id="c5929-117">Revisione 1: pulizia dell'ovvia</span><span class="sxs-lookup"><span data-stu-id="c5929-117">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
-   [<span data-ttu-id="c5929-118">Revisione 2: riprogettazione per un minor numero di connessioni</span><span class="sxs-lookup"><span data-stu-id="c5929-118">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
-   [<span data-ttu-id="c5929-119">Revisione 3: invio blocco compresso</span><span class="sxs-lookup"><span data-stu-id="c5929-119">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
-   [<span data-ttu-id="c5929-120">Miglioramenti futuri</span><span class="sxs-lookup"><span data-stu-id="c5929-120">Future Improvements</span></span>](future-improvements-2.md)

> [!WARNING]
> <span data-ttu-id="c5929-121">I primi esempi dell'applicazione forniscono prestazioni intenzionalmente insoddisfacenti, per illustrare i miglioramenti delle prestazioni possibili con le modifiche al codice.</span><span class="sxs-lookup"><span data-stu-id="c5929-121">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="c5929-122">Non usare questi esempi di codice nell'applicazione. sono solo a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="c5929-122">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c5929-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5929-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5929-124">Applicazioni Windows Sockets a prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="c5929-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



