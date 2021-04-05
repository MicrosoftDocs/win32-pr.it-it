---
description: .
ms.assetid: D721167E-B04B-4B06-A9EE-56711A7A1942
title: Strumenti di sviluppo di Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a184b513717655ee0a738be6318b4c8f2515ca3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131827"
---
# <a name="internet-explorer-8-developer-tools"></a><span data-ttu-id="105ed-103">Strumenti di sviluppo di Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="105ed-103">Internet Explorer 8 Developer Tools</span></span>

<span data-ttu-id="105ed-104">Windows Internet Explorer 8 include la funzionalità Strumenti di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="105ed-104">Windows Internet Explorer 8 includes the Developer Tools feature.</span></span> <span data-ttu-id="105ed-105">Questa funzionalità consente di eseguire rapidamente il debug di Microsoft JScript, analizzare un comportamento specifico di Windows Internet Explorer o eseguire rapidamente il prototipo o testare una nuova soluzione di progettazione.</span><span class="sxs-lookup"><span data-stu-id="105ed-105">This feature enables you to debug Microsoft JScript quickly, investigate a Windows Internet Explorer-specific behavior, or iterate rapidly to prototype or test a new design solution.</span></span>

<span data-ttu-id="105ed-106">Nelle sezioni seguenti vengono descritte le caratteristiche importanti del Strumenti di sviluppo in Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="105ed-106">The following sections describe the important characteristics of the Developer Tools in Internet Explorer 8.</span></span>

## <a name="integrated-and-simple-to-use"></a><span data-ttu-id="105ed-107">Integrato e semplice da usare</span><span class="sxs-lookup"><span data-stu-id="105ed-107">Integrated and Simple to Use</span></span>

<span data-ttu-id="105ed-108">Le Strumenti di sviluppo sono incluse in tutte le installazioni di Internet Explorer 8, pertanto è possibile eseguire il debug dei problemi in qualsiasi computer in cui è in esecuzione Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="105ed-108">The Developer Tools are included with every installation of Internet Explorer 8, so you can debug issues on any computer that is running Internet Explorer 8.</span></span> <span data-ttu-id="105ed-109">Inoltre, gli strumenti vengono caricati solo quando sono necessari per limitare il modo in cui incidono sulle prestazioni del browser.</span><span class="sxs-lookup"><span data-stu-id="105ed-109">In addition, the tools load only when you need them to limit how they impact the browser's performance.</span></span> <span data-ttu-id="105ed-110">Utilizzando la Strumenti di sviluppo, è possibile eseguire rapidamente il debug solo del processo corrente di Internet Explorer, anziché eseguire il debug di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="105ed-110">By using the Developer Tools, you can rapidly debug only the current Internet Explorer process, instead of debugging for all of Internet Explorer.</span></span>

## <a name="provide-a-visual-interface-to-the-platform"></a><span data-ttu-id="105ed-111">Fornire un'interfaccia visiva alla piattaforma</span><span class="sxs-lookup"><span data-stu-id="105ed-111">Provide a Visual Interface to the Platform</span></span>

<span data-ttu-id="105ed-112">Invece di reverse engineering come funziona il sito Web o di modificare il sito per restituire le informazioni di debug, il Strumenti di sviluppo consente di esaminare Internet Explorer per visualizzare la relativa rappresentazione del sito.</span><span class="sxs-lookup"><span data-stu-id="105ed-112">Instead of reverse engineering how your website works or modifying your site to output debug information, the Developer Tools let you look into Internet Explorer to view its representation of your site.</span></span> <span data-ttu-id="105ed-113">Questa vista consente di ridurre il tempo impiegato per il debug di siti dinamici, in cui l'ispezione del codice sorgente non è utile o l'analisi di un comportamento specifico di Internet Explorer, in cui un strumento di authoring generico non può essere utile.</span><span class="sxs-lookup"><span data-stu-id="105ed-113">This view reduces the time that you spend debugging dynamic sites, where source inspection is not useful, or investigating an Internet Explorer-specific behavior, where a generic authoring tool cannot help.</span></span>

## <a name="enable-fast-experimentation"></a><span data-ttu-id="105ed-114">Abilita sperimentazione rapida</span><span class="sxs-lookup"><span data-stu-id="105ed-114">Enable Fast Experimentation</span></span>

<span data-ttu-id="105ed-115">Quando si esegue il prototipo di un nuovo progetto o correzioni di test nelle versioni precedenti di Internet Explorer, è probabile che si modifichi l'origine, lo si salvi, si aggiorni la pagina nel browser e si ripeta.</span><span class="sxs-lookup"><span data-stu-id="105ed-115">When you are prototyping a new design or testing fixes in previous versions of Internet Explorer, you likely edit your source, save it, refresh your page in the browser, and repeat.</span></span> <span data-ttu-id="105ed-116">Il Strumenti di sviluppo semplificare questo scenario consentendo di modificare il sito all'interno del browser e di visualizzare immediatamente le modifiche.</span><span class="sxs-lookup"><span data-stu-id="105ed-116">The Developer Tools streamline this scenario by enabling you to edit your site within the browser and see changes immediately.</span></span>

## <a name="optimize-application-performance"></a><span data-ttu-id="105ed-117">Ottimizzare le prestazioni dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="105ed-117">Optimize Application Performance</span></span>

<span data-ttu-id="105ed-118">Per identificare e correggere i problemi di prestazioni, è probabile che l'iterazione si concentri su uno scenario alla volta.</span><span class="sxs-lookup"><span data-stu-id="105ed-118">To identify and fix performance issues, you likely iterate by focusing on one scenario at a time.</span></span> <span data-ttu-id="105ed-119">Tramite il profiler dello script nella Strumenti di sviluppo è possibile raccogliere statistiche, inclusi i tempi di esecuzione e il numero di volte in cui viene chiamata una funzione JavaScript.</span><span class="sxs-lookup"><span data-stu-id="105ed-119">By using the script profiler in the Developer Tools, you can collect statistics, including execution time and the number of times that a JavaScript function is called.</span></span> <span data-ttu-id="105ed-120">È possibile utilizzare queste informazioni durante il test dell'applicazione e utilizzare il rapporto profilo per identificare e correggere rapidamente i colli di bottiglia delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="105ed-120">You can use this information as you test your application and use the profile report to quickly identify and fix performance bottlenecks.</span></span>

<span data-ttu-id="105ed-121">Per accedere alla Strumenti di sviluppo, premere F12 mentre si visualizza una pagina Web o fare clic su **strumenti di sviluppo** dal menu **strumenti** .</span><span class="sxs-lookup"><span data-stu-id="105ed-121">To access the Developer Tools, press F12 while you are viewing a webpage or click **Developer Tools** on the **Tools** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="105ed-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="105ed-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="105ed-123">Strumenti per il debug di applicazioni Web e componenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="105ed-123">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 



