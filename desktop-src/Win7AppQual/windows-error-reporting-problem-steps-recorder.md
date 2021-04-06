---
description: .
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Registrazione passaggi Segnalazione errori Windows problema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25fb70acef867b878063bd6011fde6867f7f0e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759785"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a><span data-ttu-id="fad3b-103">Registrazione passaggi Segnalazione errori Windows problema</span><span class="sxs-lookup"><span data-stu-id="fad3b-103">Windows Error Reporting Problem Steps Recorder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="fad3b-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="fad3b-104">Affected Platforms</span></span>

<span data-ttu-id="fad3b-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="fad3b-105">**Clients** – Windows 7</span></span>  
<span data-ttu-id="fad3b-106">**Server** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fad3b-106">**Servers** – Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="fad3b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fad3b-107">Description</span></span>

<span data-ttu-id="fad3b-108">Prima di Windows 7, Segnalazione errori Windows (WER) raccoglieva segnalazioni di errori che indicavano problemi che necessitano di riparazione.</span><span class="sxs-lookup"><span data-stu-id="fad3b-108">Prior to Windows 7, Windows Error Reporting (WER) collected error reports that indicated problems in need of repair.</span></span> <span data-ttu-id="fad3b-109">Queste segnalazioni di errori contengono informazioni utili che descrivono la natura generale di un problema, ma non informazioni sufficienti per determinarne la causa principale.</span><span class="sxs-lookup"><span data-stu-id="fad3b-109">These error reports contain helpful information that describes the general nature of a problem, but not enough information to determine its root cause.</span></span> <span data-ttu-id="fad3b-110">Per questo, gli sviluppatori hanno bisogno di uno strumento per riprodurre lo scenario di arresto anomalo/blocco per il debug.</span><span class="sxs-lookup"><span data-stu-id="fad3b-110">For that, developers need a tool to reproduce the crash/hang scenario for debugging.</span></span>

<span data-ttu-id="fad3b-111">Una nuova applicazione, registrazione passaggi problema (PSR.exe), viene fornita in tutte le build di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fad3b-111">A new application, Problem Steps Recorder (PSR.exe), is shipping on all builds of Windows 7.</span></span> <span data-ttu-id="fad3b-112">Questa funzionalità consente la raccolta delle azioni eseguite da un utente in caso di arresto anomalo, in modo che i tester e gli sviluppatori possano riprodurre la situazione per l'analisi e il debug.</span><span class="sxs-lookup"><span data-stu-id="fad3b-112">This feature enables the collection of the actions performed by a user while encountering a crash so that testers and developers can reproduce the situation for analysis and debugging.</span></span>

## <a name="usage"></a><span data-ttu-id="fad3b-113">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="fad3b-113">Usage</span></span>

<span data-ttu-id="fad3b-114">Attualmente, uno sviluppatore di servizi di Segnalazione errori Windows deve richiedere l'abilitazione di PSR per un'applicazione; Le organizzazioni del supporto tecnico Microsoft usano questo strumento anche durante la risoluzione dei problemi con gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="fad3b-114">Currently, a Windows Error Reporting service developer must request PSR enablement for an application; Microsoft support organizations also use this tool while troubleshooting with end users.</span></span> <span data-ttu-id="fad3b-115">Sono previsti piani per rendere PSR disponibile in Windows Quality Online Services (Winqual) dopo il rilascio di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fad3b-115">Plans are in place to make PSR available at Windows Quality Online Services (Winqual) after the release of Windows 7.</span></span>

<span data-ttu-id="fad3b-116">**Nota:** Con la funzionalità PSR abilitata per un'applicazione, è possibile che si verifichi una riduzione delle prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fad3b-116">**Note:** With PSR enabled for an application, the application may see some performance degradation.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="fad3b-117">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="fad3b-117">Links to Other Resources</span></span>

-   [<span data-ttu-id="fad3b-118">Intervento di Segnalazione errori Windows Blog</span><span class="sxs-lookup"><span data-stu-id="fad3b-118">Windows Error Reporting blog entry</span></span>](/archive/blogs/wer/)
-   [<span data-ttu-id="fad3b-119">Servizi online di qualità Windows (Winqual)</span><span class="sxs-lookup"><span data-stu-id="fad3b-119">Windows Quality Online Services (Winqual)</span></span>](https://winqual.microsoft.com)

 

 
