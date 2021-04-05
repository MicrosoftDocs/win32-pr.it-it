---
title: Introduzione a Win32 e C++
description: L'obiettivo di questa serie introduttiva è insegnare come scrivere un programma desktop in C++ usando le API Win32 e COM.
ms.assetid: a9470cb9-a1e7-4d6d-a4be-61b81d209ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b1ad80530877e9502d158a16295013e3f4a05e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714146"
---
# <a name="get-started-with-win32-and-c"></a><span data-ttu-id="75eaf-103">Introduzione a Win32 e C++</span><span class="sxs-lookup"><span data-stu-id="75eaf-103">Get Started with Win32 and C++</span></span>

<span data-ttu-id="75eaf-104">L'obiettivo di questa serie introduttiva è insegnare come scrivere un programma desktop in C++ usando le API Win32 e COM.</span><span class="sxs-lookup"><span data-stu-id="75eaf-104">The aim of this Get Started series is to teach you how to write a desktop program in C++ using Win32 and COM APIs.</span></span>

<span data-ttu-id="75eaf-105">Nel primo modulo verrà illustrato in modo dettagliato come creare e visualizzare una finestra.</span><span class="sxs-lookup"><span data-stu-id="75eaf-105">In the first module, you'll learn step-by-step how to create and show a window.</span></span> <span data-ttu-id="75eaf-106">I moduli successivi introdurranno il Component Object Model (COM), la grafica e il testo e l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="75eaf-106">Later modules will introduce the Component Object Model (COM), graphics and text, and user input.</span></span>

<span data-ttu-id="75eaf-107">Per questa serie si presuppone che l'utente disponga di una conoscenza efficace della programmazione C++.</span><span class="sxs-lookup"><span data-stu-id="75eaf-107">For this series, it is assumed that you have a good working knowledge of C++ programming.</span></span> <span data-ttu-id="75eaf-108">Non si presuppone alcuna esperienza precedente con la programmazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="75eaf-108">No previous experience with Windows programming is assumed.</span></span> <span data-ttu-id="75eaf-109">Se non si ha familiarità con C++, è possibile trovare materiale didattico in [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx).</span><span class="sxs-lookup"><span data-stu-id="75eaf-109">If you are new to C++, you can find learning material at the [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx).</span></span> <span data-ttu-id="75eaf-110">Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.</span><span class="sxs-lookup"><span data-stu-id="75eaf-110">(This resource may not be available in some languages and countries.)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="75eaf-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="75eaf-111">In this section</span></span>



| <span data-ttu-id="75eaf-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="75eaf-112">Topic</span></span>                                                                                                     | <span data-ttu-id="75eaf-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75eaf-113">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75eaf-114">Introduzione alla programmazione Windows in C++</span><span class="sxs-lookup"><span data-stu-id="75eaf-114">Introduction to Windows Programming in C++</span></span>](introduction-to-windows-programming-in-c--.md)<br/>   | <span data-ttu-id="75eaf-115">In questa sezione vengono descritte alcune delle terminologie di base e le convenzioni di codifica utilizzate nella programmazione Windows.</span><span class="sxs-lookup"><span data-stu-id="75eaf-115">This section describes some of the basic terminology and coding conventions used in Windows programming.</span></span><br/>  |
| [<span data-ttu-id="75eaf-116">Modulo 1. Il primo programma Windows</span><span class="sxs-lookup"><span data-stu-id="75eaf-116">Module 1. Your First Windows Program</span></span>](your-first-windows-program.md)<br/>                         | <span data-ttu-id="75eaf-117">In questo modulo verrà creato un semplice programma Windows che mostra una finestra vuota.</span><span class="sxs-lookup"><span data-stu-id="75eaf-117">In this module, you will create a simple Windows program that shows a blank window.</span></span><br/>                       |
| [<span data-ttu-id="75eaf-118">Modulo 2. Uso di COM nel programma Windows</span><span class="sxs-lookup"><span data-stu-id="75eaf-118">Module 2. Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)<br/> | <span data-ttu-id="75eaf-119">Questo modulo introduce il Component Object Model (COM), che è la base di molte delle API Windows moderne.</span><span class="sxs-lookup"><span data-stu-id="75eaf-119">This module introduces the Component Object Model (COM), which underlies many of the modern Windows APIs.</span></span><br/> |
| [<span data-ttu-id="75eaf-120">Modulo 3. Grafica di Windows</span><span class="sxs-lookup"><span data-stu-id="75eaf-120">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)<br/>                                  | <span data-ttu-id="75eaf-121">Questo modulo introduce l'architettura grafica di Windows, con particolare attenzione a Direct2D.</span><span class="sxs-lookup"><span data-stu-id="75eaf-121">This module introduces the Windows graphics architecture, with a focus on Direct2D.</span></span><br/>                       |
| [<span data-ttu-id="75eaf-122">Modulo 4. Input utente</span><span class="sxs-lookup"><span data-stu-id="75eaf-122">Module 4. User Input</span></span>](module-4--user-input.md)<br/>                                               | <span data-ttu-id="75eaf-123">Questo modulo descrive l'input da tastiera e mouse.</span><span class="sxs-lookup"><span data-stu-id="75eaf-123">This module describes mouse and keyboard input.</span></span><br/>                                                           |
| [<span data-ttu-id="75eaf-124">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="75eaf-124">Sample Code</span></span>](learn-to-program-for-windows--sample-code.md)<br/>                                   | <span data-ttu-id="75eaf-125">Contiene collegamenti per scaricare il codice di esempio per questa serie.</span><span class="sxs-lookup"><span data-stu-id="75eaf-125">Contains links to download the sample code for this series.</span></span><br/>                                               |



 

 

 





