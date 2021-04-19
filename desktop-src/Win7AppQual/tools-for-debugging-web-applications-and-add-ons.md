---
description: .
ms.assetid: ECE4A9C6-8553-4718-AAFA-AC4D9924A786
title: Strumenti per il debug di applicazioni Web e Add-Ons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb68485cd674266235d430d7d26b9a39e6fbec14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319831"
---
# <a name="tools-for-debugging-web-applications-and-add-ons"></a><span data-ttu-id="b98cb-103">Strumenti per il debug di applicazioni Web e Add-Ons</span><span class="sxs-lookup"><span data-stu-id="b98cb-103">Tools for Debugging Web Applications and Add-Ons</span></span>

<span data-ttu-id="b98cb-104">Anziché [risolvere i problemi di compatibilità nelle applicazioni Web e nei componenti](remediating-web-applications-and-add-ons.md)aggiuntivi, è possibile fare in modo che l'applicazione Web o il sito Web funzioni in modo nativo nella modalità standard di Windows Internet Explorer 8 scrivendo il codice agli standard Web più recenti.</span><span class="sxs-lookup"><span data-stu-id="b98cb-104">Instead of [fixing compatibility issues in web applications and add-ons](remediating-web-applications-and-add-ons.md), you can make the web application or website work natively in Windows Internet Explorer 8 standards mode by writing your code to the most recent web standards.</span></span>

<span data-ttu-id="b98cb-105">Per valutare completamente eventuali problemi dell'applicazione o del sito Web, è necessario ricercare la causa radice del problema.</span><span class="sxs-lookup"><span data-stu-id="b98cb-105">To fully assess any problems in your application or website, you should research the root cause of the problem.</span></span> <span data-ttu-id="b98cb-106">Ad esempio, il team di Internet Explorer ha determinato le cause principali utilizzando il Strumenti di sviluppo e riducendo logicamente i possibili problemi.</span><span class="sxs-lookup"><span data-stu-id="b98cb-106">For example, the Internet Explorer team determined root causes by using the Developer Tools and logically reducing possible issues.</span></span> <span data-ttu-id="b98cb-107">Le sezioni seguenti descrivono diversi strumenti che consentono di semplificare il processo di debug.</span><span class="sxs-lookup"><span data-stu-id="b98cb-107">The following sections describe several tools to help simplify the debugging process.</span></span>



| <span data-ttu-id="b98cb-108">Sezione</span><span class="sxs-lookup"><span data-stu-id="b98cb-108">Section</span></span>                                                                                                                    | <span data-ttu-id="b98cb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b98cb-109">Description</span></span>                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b98cb-110">Microsoft Expression Web SuperPreview</span><span class="sxs-lookup"><span data-stu-id="b98cb-110">Microsoft Expression Web SuperPreview</span></span>](microsoft-expression-web-superpreview.md)                                         | <span data-ttu-id="b98cb-111">Strumento di debug visivo autonomo che rende più veloce e semplice la migrazione dei siti da Microsoft Internet Explorer 6 a Windows Internet Explorer 7 o Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="b98cb-111">A stand-alone visual debugging tool that makes it faster and easier to migrate your sites from Microsoft Internet Explorer 6 to Windows Internet Explorer 7 or Internet Explorer 8.</span></span> |
| [<span data-ttu-id="b98cb-112">Internet Explorer Compatibility Test Tool (IECTT)</span><span class="sxs-lookup"><span data-stu-id="b98cb-112">Internet Explorer Compatibility Test Tool (IECTT)</span></span>](inernet-explorer-compatibility-test-tool--iectt-.md)                  | <span data-ttu-id="b98cb-113">Componente di [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install) che consente di diagnosticare i problemi nelle applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="b98cb-113">A component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install) that can help you diagnose issues in your web applications.</span></span>       |
| [<span data-ttu-id="b98cb-114">Strumenti di sviluppo di Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="b98cb-114">Internet Explorer 8 Developer Tools</span></span>](internet-explorer-8-developer-tools.md)                                             | <span data-ttu-id="b98cb-115">Strumenti di sviluppo inclusi in Internet Explorer 8 per il debug.</span><span class="sxs-lookup"><span data-stu-id="b98cb-115">The developer tools that are included in Internet Explorer 8 for debugging.</span></span>                                                                                                         |
| [<span data-ttu-id="b98cb-116">Compatibilità guidata Internet Explorer 8 (aggiorno)</span><span class="sxs-lookup"><span data-stu-id="b98cb-116">Internet Explorer 8 Compatibility Wizard (Aggiorno)</span></span>](inernet-explorer-8-compatibility-wizard--aggiorno-.md)              | <span data-ttu-id="b98cb-117">Strumento di terze parti che aggiorna automaticamente i siti Web per il rendering corretto in Internet Explorer 8 senza interruzioni di compatibilità nei browser meno recenti.</span><span class="sxs-lookup"><span data-stu-id="b98cb-117">A third-party tool that automatically upgrades websites to render correctly in Internet Explorer 8 without breaking compatibility in older browsers.</span></span>                                |
| [<span data-ttu-id="b98cb-118">Strumento Debugger Web Fiddler</span><span class="sxs-lookup"><span data-stu-id="b98cb-118">Fiddler Web Debugger Tool</span></span>](fiddler-web-debugger-tool.md)                                                                 | <span data-ttu-id="b98cb-119">Strumento di terze parti per l'acquisizione del traffico di rete tra Internet e i computer di test.</span><span class="sxs-lookup"><span data-stu-id="b98cb-119">A third-party tool for capturing network traffic between the Internet and test computers.</span></span>                                                                                           |
| [<span data-ttu-id="b98cb-120">Test della compatibilità delle applicazioni utilizzando immagini di Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b98cb-120">Application Compatibility Testing Using Virtual PC Images</span></span>](application-compatibility-testing-using-virtual-pc-images.md) | <span data-ttu-id="b98cb-121">Immagini Virtual PC che semplificano i test di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="b98cb-121">Virtual PC images that simplify compatibility testing.</span></span>                                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="b98cb-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b98cb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b98cb-123">Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="b98cb-123">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
