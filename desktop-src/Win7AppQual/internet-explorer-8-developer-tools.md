---
description: Strumenti di sviluppo di Internet Explorer 8
ms.assetid: D721167E-B04B-4B06-A9EE-56711A7A1942
title: Strumenti di sviluppo di Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a4314d5d0392b9bc4933b945f7da32040e1570
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088209"
---
# <a name="internet-explorer-8-developer-tools"></a><span data-ttu-id="43ba5-103">Strumenti di sviluppo di Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="43ba5-103">Internet Explorer 8 Developer Tools</span></span>

<span data-ttu-id="43ba5-104">Windows Internet Explorer 8 include la Strumenti di sviluppo funzionalità.</span><span class="sxs-lookup"><span data-stu-id="43ba5-104">Windows Internet Explorer 8 includes the Developer Tools feature.</span></span> <span data-ttu-id="43ba5-105">Questa funzionalità consente di eseguire rapidamente il debug di Microsoft JScript, analizzare un comportamento specifico di Windows Internet Explorer o eseguire rapidamente l'iterazione per creare prototipi o testare una nuova soluzione di progettazione.</span><span class="sxs-lookup"><span data-stu-id="43ba5-105">This feature enables you to debug Microsoft JScript quickly, investigate a Windows Internet Explorer-specific behavior, or iterate rapidly to prototype or test a new design solution.</span></span>

<span data-ttu-id="43ba5-106">Le sezioni seguenti descrivono le caratteristiche importanti del Strumenti di sviluppo in Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="43ba5-106">The following sections describe the important characteristics of the Developer Tools in Internet Explorer 8.</span></span>

## <a name="integrated-and-simple-to-use"></a><span data-ttu-id="43ba5-107">Integrazione e semplicità d'uso</span><span class="sxs-lookup"><span data-stu-id="43ba5-107">Integrated and Simple to Use</span></span>

<span data-ttu-id="43ba5-108">I Strumenti di sviluppo sono inclusi in ogni installazione di Internet Explorer 8, pertanto è possibile eseguire il debug dei problemi in qualsiasi computer che esegue Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="43ba5-108">The Developer Tools are included with every installation of Internet Explorer 8, so you can debug issues on any computer that is running Internet Explorer 8.</span></span> <span data-ttu-id="43ba5-109">Inoltre, gli strumenti vengono caricati solo quando sono necessari per limitare l'impatto sulle prestazioni del browser.</span><span class="sxs-lookup"><span data-stu-id="43ba5-109">In addition, the tools load only when you need them to limit how they impact the browser's performance.</span></span> <span data-ttu-id="43ba5-110">Usando il Strumenti di sviluppo, è possibile eseguire rapidamente il debug solo del processo Internet Explorer corrente, invece di eseguire il debug per tutte le Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="43ba5-110">By using the Developer Tools, you can rapidly debug only the current Internet Explorer process, instead of debugging for all of Internet Explorer.</span></span>

## <a name="provide-a-visual-interface-to-the-platform"></a><span data-ttu-id="43ba5-111">Fornire un'interfaccia visiva alla piattaforma</span><span class="sxs-lookup"><span data-stu-id="43ba5-111">Provide a Visual Interface to the Platform</span></span>

<span data-ttu-id="43ba5-112">Anziché reverse engineering il funzionamento del sito Web o la modifica del sito per l'output delle informazioni di debug, il Strumenti di sviluppo consente di esaminare Internet Explorer per visualizzarne la rappresentazione del sito.</span><span class="sxs-lookup"><span data-stu-id="43ba5-112">Instead of reverse engineering how your website works or modifying your site to output debug information, the Developer Tools let you look into Internet Explorer to view its representation of your site.</span></span> <span data-ttu-id="43ba5-113">Questa visualizzazione riduce il tempo necessario per il debug di siti dinamici, in cui l'ispezione dell'origine non è utile, o l'analisi di un comportamento specifico di Internet Explorer, in cui uno strumento di creazione generico non è utile.</span><span class="sxs-lookup"><span data-stu-id="43ba5-113">This view reduces the time that you spend debugging dynamic sites, where source inspection is not useful, or investigating an Internet Explorer-specific behavior, where a generic authoring tool cannot help.</span></span>

## <a name="enable-fast-experimentation"></a><span data-ttu-id="43ba5-114">Abilitare La sperimentazione rapida</span><span class="sxs-lookup"><span data-stu-id="43ba5-114">Enable Fast Experimentation</span></span>

<span data-ttu-id="43ba5-115">Quando si crea un prototipo di una nuova progettazione o si testano correzioni nelle versioni precedenti di Internet Explorer, probabilmente si modifica l'origine, la si salva, si aggiorna la pagina nel browser e si ripete l'operazione.</span><span class="sxs-lookup"><span data-stu-id="43ba5-115">When you are prototyping a new design or testing fixes in previous versions of Internet Explorer, you likely edit your source, save it, refresh your page in the browser, and repeat.</span></span> <span data-ttu-id="43ba5-116">Il Strumenti di sviluppo semplificare questo scenario consentendo di modificare il sito all'interno del browser e visualizzare immediatamente le modifiche.</span><span class="sxs-lookup"><span data-stu-id="43ba5-116">The Developer Tools streamline this scenario by enabling you to edit your site within the browser and see changes immediately.</span></span>

## <a name="optimize-application-performance"></a><span data-ttu-id="43ba5-117">Ottimizzare le prestazioni dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="43ba5-117">Optimize Application Performance</span></span>

<span data-ttu-id="43ba5-118">Per identificare e risolvere i problemi di prestazioni, è probabile che si eserciti l'iterazione concentrandosi su uno scenario alla volta.</span><span class="sxs-lookup"><span data-stu-id="43ba5-118">To identify and fix performance issues, you likely iterate by focusing on one scenario at a time.</span></span> <span data-ttu-id="43ba5-119">Usando il profiler di script nel Strumenti di sviluppo, è possibile raccogliere statistiche, tra cui il tempo di esecuzione e il numero di volte in cui viene chiamata una funzione JavaScript.</span><span class="sxs-lookup"><span data-stu-id="43ba5-119">By using the script profiler in the Developer Tools, you can collect statistics, including execution time and the number of times that a JavaScript function is called.</span></span> <span data-ttu-id="43ba5-120">È possibile usare queste informazioni durante il test dell'applicazione e il report del profilo per identificare e correggere rapidamente i colli di bottiglia delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="43ba5-120">You can use this information as you test your application and use the profile report to quickly identify and fix performance bottlenecks.</span></span>

<span data-ttu-id="43ba5-121">Per accedere al Strumenti di sviluppo, premere F12 mentre si visualizza una pagina **Web o** scegliere Strumenti di sviluppo **dal** menu Strumenti.</span><span class="sxs-lookup"><span data-stu-id="43ba5-121">To access the Developer Tools, press F12 while you are viewing a webpage or click **Developer Tools** on the **Tools** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43ba5-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43ba5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43ba5-123">Strumenti per il debug di applicazioni Web e componenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="43ba5-123">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 



