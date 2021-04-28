---
description: Segnalazione errori Windows Registrazione azioni utente
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Segnalazione errori Windows Registrazione azioni utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abb8adf545152e34c2b2100022068291e3571f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084159"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a><span data-ttu-id="63ee3-103">Segnalazione errori Windows Registrazione azioni utente</span><span class="sxs-lookup"><span data-stu-id="63ee3-103">Windows Error Reporting Problem Steps Recorder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="63ee3-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="63ee3-104">Affected Platforms</span></span>

<span data-ttu-id="63ee3-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="63ee3-105">**Clients** – Windows 7</span></span>  
<span data-ttu-id="63ee3-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63ee3-106">**Servers** – Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="63ee3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63ee3-107">Description</span></span>

<span data-ttu-id="63ee3-108">Prima di Windows 7, Segnalazione errori Windows (WER) raccoglieva segnalazioni di errori che indicava problemi che doveva essere ripristinati.</span><span class="sxs-lookup"><span data-stu-id="63ee3-108">Prior to Windows 7, Windows Error Reporting (WER) collected error reports that indicated problems in need of repair.</span></span> <span data-ttu-id="63ee3-109">Queste segnalazioni di errore contengono informazioni utili che descrivono la natura generale di un problema, ma non informazioni sufficienti per determinarne la causa radice.</span><span class="sxs-lookup"><span data-stu-id="63ee3-109">These error reports contain helpful information that describes the general nature of a problem, but not enough information to determine its root cause.</span></span> <span data-ttu-id="63ee3-110">A tale scopo, gli sviluppatori necessitano di uno strumento per riprodurre lo scenario di arresto anomalo/blocco per il debug.</span><span class="sxs-lookup"><span data-stu-id="63ee3-110">For that, developers need a tool to reproduce the crash/hang scenario for debugging.</span></span>

<span data-ttu-id="63ee3-111">Una nuova applicazione, Registrazione azioni utente (PSR.exe), è disponibile in tutte le build di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="63ee3-111">A new application, Problem Steps Recorder (PSR.exe), is shipping on all builds of Windows 7.</span></span> <span data-ttu-id="63ee3-112">Questa funzionalità consente la raccolta delle azioni eseguite da un utente durante l'arresto anomalo del sistema, in modo che tester e sviluppatori possano riprodurre la situazione per l'analisi e il debug.</span><span class="sxs-lookup"><span data-stu-id="63ee3-112">This feature enables the collection of the actions performed by a user while encountering a crash so that testers and developers can reproduce the situation for analysis and debugging.</span></span>

## <a name="usage"></a><span data-ttu-id="63ee3-113">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="63ee3-113">Usage</span></span>

<span data-ttu-id="63ee3-114">Attualmente, uno sviluppatore Segnalazione errori Windows servizio deve richiedere l'abilitazione di PSR per un'applicazione. Le organizzazioni di supporto Tecnico Microsoft usano anche questo strumento durante la risoluzione dei problemi con gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="63ee3-114">Currently, a Windows Error Reporting service developer must request PSR enablement for an application; Microsoft support organizations also use this tool while troubleshooting with end users.</span></span> <span data-ttu-id="63ee3-115">Sono disponibili piani per rendere disponibile PSR in Windows Quality Online Services (Winqual) dopo il rilascio di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="63ee3-115">Plans are in place to make PSR available at Windows Quality Online Services (Winqual) after the release of Windows 7.</span></span>

<span data-ttu-id="63ee3-116">**Nota:** Con PSR abilitato per un'applicazione, è possibile che si sia verificata una riduzione delle prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="63ee3-116">**Note:** With PSR enabled for an application, the application may see some performance degradation.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="63ee3-117">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="63ee3-117">Links to Other Resources</span></span>

-   [<span data-ttu-id="63ee3-118">Segnalazione errori Windows di blog</span><span class="sxs-lookup"><span data-stu-id="63ee3-118">Windows Error Reporting blog entry</span></span>](/archive/blogs/wer/)
-   [<span data-ttu-id="63ee3-119">Windows Quality Online Services (Winqual)</span><span class="sxs-lookup"><span data-stu-id="63ee3-119">Windows Quality Online Services (Winqual)</span></span>](https://winqual.microsoft.com)

 

 
