---
title: Esempi di codice Win32 per desktop
description: Informazioni sui repository di esempio per Win32 e su come eseguirne la ricerca.
ms.topic: article
ms.date: 03/19/2021
ms.openlocfilehash: 5a4083697d444f36b31c553a2d6159d4370565d4
ms.sourcegitcommit: 46e75903326c49a6c5cc576ee2b4f67f64a6d5ff
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323869"
---
# <a name="desktop-win32-code-samples"></a><span data-ttu-id="c2353-103">Esempi di codice Win32 per desktop</span><span class="sxs-lookup"><span data-stu-id="c2353-103">Desktop Win32 code samples</span></span>

<span data-ttu-id="c2353-104">Vedere anche [esempi di codice](https://developer.microsoft.com/windows/samples/).</span><span class="sxs-lookup"><span data-stu-id="c2353-104">Also see [Code samples](https://developer.microsoft.com/windows/samples/).</span></span>

## <a name="find-a-sample-for-the-api-youre-interested-in"></a><span data-ttu-id="c2353-105">Trovare un esempio per l'API a cui si è interessati</span><span class="sxs-lookup"><span data-stu-id="c2353-105">Find a sample for the API you're interested in</span></span>

<span data-ttu-id="c2353-106">È possibile usare Microsoft Visual Studio per cercare il codice sorgente di un intero repository per verificare se è in corso la dimostrazione dell'utilizzo di un'API Windows specifica.</span><span class="sxs-lookup"><span data-stu-id="c2353-106">You can use Microsoft Visual Studio to search an entire repo's source code to see whether the usage of a particular Windows API is being demonstrated.</span></span>

* <span data-ttu-id="c2353-107">Clonare i repository elencati nelle sezioni seguenti (oppure scaricare il file ZIP) nel file system locale.</span><span class="sxs-lookup"><span data-stu-id="c2353-107">Clone any of the repos listed in the sections below (or download the ZIP) to your local file system.</span></span>
* <span data-ttu-id="c2353-108">**Trovare quindi nei file** in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c2353-108">Then **Find in Files** in Visual Studio.</span></span> <span data-ttu-id="c2353-109">Impostare **Cerca nella** cartella clonata o scaricata e cercare il nome dell'API a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="c2353-109">Set **Look in** to the folder you cloned or downloaded into, and search for the name of the API you're interested in.</span></span> <span data-ttu-id="c2353-110">Il controllo del **case di corrispondenza** fornisce risultati ottimali.</span><span class="sxs-lookup"><span data-stu-id="c2353-110">Checking **Match case** gives best results.</span></span>
* <span data-ttu-id="c2353-111">Se l'API può  essere chiamata in varie forme &mdash; , ad esempio **CreateMutex**, **CreateMutexA** e **CreateMutexW**, prestare attenzione nel controllare la parola intera.</span><span class="sxs-lookup"><span data-stu-id="c2353-111">Be careful of checking **Match whole word** if the API can be called in various forms&mdash;for example, **CreateMutex**, **CreateMutexA**, and **CreateMutexW**.</span></span> <span data-ttu-id="c2353-112">In tal caso, cercare **CreateMutex** con la **parola intera corrispondente** deselezionata.</span><span class="sxs-lookup"><span data-stu-id="c2353-112">In that case, search for **CreateMutex** with **Match whole word** unchecked.</span></span>

> [!NOTE]
> <span data-ttu-id="c2353-113">È possibile installare [Visual Studio](https://visualstudio.microsoft.com/downloads/) senza spese.</span><span class="sxs-lookup"><span data-stu-id="c2353-113">You can install [Visual Studio](https://visualstudio.microsoft.com/downloads/) without expense.</span></span> <span data-ttu-id="c2353-114">Una Community Edition è disponibile &mdash; gratuitamente per studenti, collaboratori open source e singoli utenti.</span><span class="sxs-lookup"><span data-stu-id="c2353-114">A Community edition is available&mdash;it's free for students, open-source contributors, and individuals.</span></span> <span data-ttu-id="c2353-115">Naturalmente, è possibile eseguire la stessa operazione con un repository di esempi.</span><span class="sxs-lookup"><span data-stu-id="c2353-115">Of course you can do the same thing with any samples repo.</span></span>

## <a name="the-windows-classic-samples-repo"></a><span data-ttu-id="c2353-116">Repository di esempi classici di Windows</span><span class="sxs-lookup"><span data-stu-id="c2353-116">The Windows classic samples repo</span></span>

<span data-ttu-id="c2353-117">Il repository principale contenente le app di Windows di esempio che usano l'API Win32 è il repository degli [esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples) .</span><span class="sxs-lookup"><span data-stu-id="c2353-117">The main repo containing sample Windows apps using the Win32 API is the [Windows classic samples](https://github.com/Microsoft/Windows-classic-samples) repo.</span></span>

## <a name="directx-samples"></a><span data-ttu-id="c2353-118">Esempi di DirectX</span><span class="sxs-lookup"><span data-stu-id="c2353-118">DirectX samples</span></span>

<span data-ttu-id="c2353-119">Vedere il repository [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) per gli esempi di grafica DirectX 12 che illustrano come creare applicazioni con utilizzo intensivo di grafica per Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c2353-119">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="c2353-120">Vedere anche [esempi di DirectX](/windows/uwp/gaming/directx-samples).</span><span class="sxs-lookup"><span data-stu-id="c2353-120">Also see [DirectX samples](/windows/uwp/gaming/directx-samples).</span></span>

## <a name="older-samples"></a><span data-ttu-id="c2353-121">Esempi meno recenti</span><span class="sxs-lookup"><span data-stu-id="c2353-121">Older samples</span></span>

<span data-ttu-id="c2353-122">Alcune app di esempio Win32 precedenti sono disponibili nel repository di [esempi Microsoft per la raccolta di codici MSDN](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) .</span><span class="sxs-lookup"><span data-stu-id="c2353-122">You can find some older Win32 sample apps in the [MSDN Code Gallery Microsoft samples](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) repo.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2353-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2353-123">See also</span></span>

* [<span data-ttu-id="c2353-124">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="c2353-124">Code samples</span></span>](https://developer.microsoft.com/windows/samples/)
* [<span data-ttu-id="c2353-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c2353-125">Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="c2353-126">Esempi di Windows classico</span><span class="sxs-lookup"><span data-stu-id="c2353-126">Windows classic samples</span></span>](https://github.com/Microsoft/Windows-classic-samples)
* [<span data-ttu-id="c2353-127">DirectX-Graphics-Samples</span><span class="sxs-lookup"><span data-stu-id="c2353-127">DirectX-Graphics-Samples</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples)
* [<span data-ttu-id="c2353-128">Esempi di DirectX</span><span class="sxs-lookup"><span data-stu-id="c2353-128">DirectX samples</span></span>](/windows/uwp/gaming/directx-samples)
* [<span data-ttu-id="c2353-129">Esempi di Microsoft su MSDN Code Gallery</span><span class="sxs-lookup"><span data-stu-id="c2353-129">MSDN Code Gallery Microsoft samples</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft)
