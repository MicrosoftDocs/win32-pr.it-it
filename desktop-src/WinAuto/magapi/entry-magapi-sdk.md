---
title: API Magnification
description: L'API di ingrandimento consente alle applicazioni di ingrandire l'intero schermo o parti dello schermo e di applicare gli effetti dei colori.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/08/2020
ms.locfileid: "103857974"
---
# <a name="magnification-api"></a><span data-ttu-id="4eddc-103">API Magnification</span><span class="sxs-lookup"><span data-stu-id="4eddc-103">Magnification API</span></span>

## <a name="purpose"></a><span data-ttu-id="4eddc-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="4eddc-104">Purpose</span></span>

<span data-ttu-id="4eddc-105">L'API di ingrandimento consente alle applicazioni di ingrandire l'intero schermo o parti dello schermo e di applicare gli effetti dei colori.</span><span class="sxs-lookup"><span data-stu-id="4eddc-105">The Magnification API enables applications to magnify the entire screen or portions of the screen, and to apply color effects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="4eddc-106">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="4eddc-106">Where applicable</span></span>

<span data-ttu-id="4eddc-107">Utilizzando l'API di ingrandimento, gli sviluppatori possono creare applicazioni per la tecnologia per l'accessibilità basate su Windows che ingrandiscono lo schermo e applicano effetti cromatici al contenuto della schermata ingrandita.</span><span class="sxs-lookup"><span data-stu-id="4eddc-107">By using the Magnification API, developers can create Windows-based assistive-technology applications that magnify the screen and apply color effects to the magnified screen content.</span></span> <span data-ttu-id="4eddc-108">Per gli utenti con ipovisione, le dimensioni delle immagini ingrandite e gli effetti dei colori consentono di semplificare la visualizzazione e l'utilizzo del computer.</span><span class="sxs-lookup"><span data-stu-id="4eddc-108">For users with low vision, the enlarged image size and color effects can help make the computer easier to see and use.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4eddc-109">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="4eddc-109">Developer audience</span></span>

<span data-ttu-id="4eddc-110">L'API di ingrandimento è progettata principalmente per gli sviluppatori C e C++ che conoscono la programmazione Windows e conoscono i concetti di programmazione della grafica.</span><span class="sxs-lookup"><span data-stu-id="4eddc-110">The Magnification API is designed primarily for C and C++ developers who understand Windows programming and who are familiar with graphics programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4eddc-111">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="4eddc-111">Run-time requirements</span></span>

<span data-ttu-id="4eddc-112">La versione iniziale dell'API di ingrandimento è supportata in Windows Vista e nei sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="4eddc-112">The initial release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="4eddc-113">Una seconda versione aggiunge funzionalità di ingrandimento a schermo intero ed è supportata in Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4eddc-113">A second release adds fullscreen magnification capabilities and is supported on Windows 8 and later.</span></span>

<span data-ttu-id="4eddc-114">L'API è supportata da Magnification.dll.</span><span class="sxs-lookup"><span data-stu-id="4eddc-114">The API is supported by Magnification.dll.</span></span> <span data-ttu-id="4eddc-115">Per compilare l'applicazione, includere ingrandimento. h e collegamento a ingrandimento. lib.</span><span class="sxs-lookup"><span data-stu-id="4eddc-115">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="4eddc-116">L'API di ingrandimento non è supportata in WOW64; ovvero, un'applicazione di Magnifier a 32 bit non verrà eseguita correttamente in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4eddc-116">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4eddc-117">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="4eddc-117">In this section</span></span>

| <span data-ttu-id="4eddc-118">Argomento</span><span class="sxs-lookup"><span data-stu-id="4eddc-118">Topic</span></span> | <span data-ttu-id="4eddc-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4eddc-119">Description</span></span> |
|:---|:---|
| [<span data-ttu-id="4eddc-120">Panoramica dell'API di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="4eddc-120">Magnification API Overview</span></span>](magapi-intro.md)<br/> | <span data-ttu-id="4eddc-121">Questo argomento descrive l'API di ingrandimento e spiega come usarlo in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4eddc-121">This topic describes the Magnification API and explains how to use it in an application.</span></span><br/> |
| [<span data-ttu-id="4eddc-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4eddc-122">Reference</span></span>](entry-magapi-ref.md)<br/>  | <span data-ttu-id="4eddc-123">Questa sezione contiene informazioni di riferimento per l'API di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="4eddc-123">This section contains reference information for the Magnification API.</span></span><br/>|
| [<span data-ttu-id="4eddc-124">Esempi</span><span class="sxs-lookup"><span data-stu-id="4eddc-124">Samples</span></span>](magapi-samples-entry.md)<br/> | <span data-ttu-id="4eddc-125">Nell'applicazione di esempio seguente viene illustrato come utilizzare l'API di ingrandimento per creare una lente di ingrandimento a schermo intero che consente di ingrandire l'intero schermo e una lente di ingrandimento a finestra che ingrandisce e visualizza una parte della schermata in una finestra.</span><span class="sxs-lookup"><span data-stu-id="4eddc-125">The following sample application demonstrates how to use the Magnification API to create a full screen magnifier that magnifies the entire screen, and a windowed magnifier that magnifies and displays a portion of the screen in a window.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="4eddc-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4eddc-126">Related topics</span></span>

<span data-ttu-id="4eddc-127">[Sito Web Microsoft Accessibility](https://www.microsoft.com/accessibility/), [accessibilità in Windows 10](/windows/apps/accessibility)</span><span class="sxs-lookup"><span data-stu-id="4eddc-127">[Microsoft Accessibility website](https://www.microsoft.com/accessibility/), [Accessibility in Windows 10](/windows/apps/accessibility)</span></span>
