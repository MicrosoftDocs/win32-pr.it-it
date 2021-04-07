---
description: Errori di registrazione
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Errori di registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745970"
---
# <a name="logging-errors"></a><span data-ttu-id="8c087-103">Errori di registrazione</span><span class="sxs-lookup"><span data-stu-id="8c087-103">Logging Errors</span></span>

<span data-ttu-id="8c087-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="8c087-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8c087-105">[DirectShow editing Services](directshow-editing-services.md) (des) fornisce un meccanismo incorporato per la registrazione degli errori che si verificano durante il caricamento, la costruzione o il rendering di un progetto des.</span><span class="sxs-lookup"><span data-stu-id="8c087-105">[DirectShow Editing Services](directshow-editing-services.md) (DES) provides a built-in mechanism for logging errors that occur when loading, constructing, or rendering a DES project.</span></span> <span data-ttu-id="8c087-106">Questo articolo presenta un'applicazione console di esempio che carica un file di progetto XML e tenta di eseguirne il rendering.</span><span class="sxs-lookup"><span data-stu-id="8c087-106">This article presents a sample console application that loads an XML project file and attempts to render it.</span></span> <span data-ttu-id="8c087-107">Se si verifica un errore, l'applicazione stampa un messaggio di errore nella finestra della console.</span><span class="sxs-lookup"><span data-stu-id="8c087-107">If an error occurs, the application prints an error message in the console window.</span></span> <span data-ttu-id="8c087-108">Il codice di esempio presentato in questo articolo si basa sull'esempio fornito in [caricamento e anteprima di un progetto](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="8c087-108">The sample code presented in this article builds on the example given in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

> [!Note]  
> <span data-ttu-id="8c087-109">L'applicazione non è necessaria per implementare la registrazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="8c087-109">Your application is not required to implement error logging.</span></span> <span data-ttu-id="8c087-110">Il DES non registra gli errori a meno che non venga richiesto in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="8c087-110">DES does not log errors unless you explicitly request it.</span></span>

 

<span data-ttu-id="8c087-111">Questo articolo presuppone che si conosca la programmazione dei client COM e il modello di sequenza temporale DES.</span><span class="sxs-lookup"><span data-stu-id="8c087-111">This article assumes that you understand COM client programming and the DES timeline model.</span></span> <span data-ttu-id="8c087-112">Inoltre, è necessario comprendere le nozioni di base della programmazione di oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="8c087-112">In addition, you need to understand the basics of COM object programming.</span></span> <span data-ttu-id="8c087-113">Per informazioni sulle sequenze temporali in DES, vedere [il modello di sequenza temporale](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="8c087-113">For information about timelines in DES, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="8c087-114">Questo articolo include le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8c087-114">This article contains the following sections.</span></span>

-   [<span data-ttu-id="8c087-115">Panoramica della registrazione degli errori</span><span class="sxs-lookup"><span data-stu-id="8c087-115">Overview of Error Logging</span></span>](overview-of-error-logging.md)
-   [<span data-ttu-id="8c087-116">Creazione di una classe di registrazione degli errori</span><span class="sxs-lookup"><span data-stu-id="8c087-116">Creating an Error Logging Class</span></span>](creating-an-error-logging-class.md)
-   [<span data-ttu-id="8c087-117">Implementazione di IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="8c087-117">Implementing IAMErrorLog</span></span>](implementing-iamerrorlog.md)
-   [<span data-ttu-id="8c087-118">Impostazione del log degli errori</span><span class="sxs-lookup"><span data-stu-id="8c087-118">Setting the Error Log</span></span>](setting-the-error-log.md)
-   [<span data-ttu-id="8c087-119">Registrazione degli errori DES: codice di esempio</span><span class="sxs-lookup"><span data-stu-id="8c087-119">DES Error Logging: Example Code</span></span>](des-error-logging--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="8c087-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c087-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c087-121">Uso dei servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="8c087-121">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



