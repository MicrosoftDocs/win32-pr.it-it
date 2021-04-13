---
title: Gadget desktop rimossi
description: Gadget desktop rimossi
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- Gadget
- gadget desktop
- Barra laterale di Windows
- Barra laterale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104399813"
---
# <a name="desktop-gadgets-removed"></a><span data-ttu-id="b749d-107">Gadget desktop rimossi</span><span class="sxs-lookup"><span data-stu-id="b749d-107">Desktop gadgets removed</span></span>

## <a name="platforms"></a><span data-ttu-id="b749d-108">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="b749d-108">Platforms</span></span>

 <span data-ttu-id="b749d-109">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="b749d-109">**Clients** - Windows 8</span></span>  
<span data-ttu-id="b749d-110">**Server** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b749d-110">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="b749d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b749d-111">Description</span></span>

<span data-ttu-id="b749d-112">Dal punto di vista della funzionalità, i gadget sono già stati deprecati e sono stati sottoclassati da nuovi riquadri animati e app.</span><span class="sxs-lookup"><span data-stu-id="b749d-112">From a functionality standpoint, Gadgets have already been deprecated and are outclassed by new live tiles and apps.</span></span> <span data-ttu-id="b749d-113">I gadget presentano anche un rischio per la sicurezza per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="b749d-113">Gadgets also present a security risk to users.</span></span> <span data-ttu-id="b749d-114">Come piattaforma, esistono vulnerabilità in modo che possano essere sfruttati anche i gadget benigni.</span><span class="sxs-lookup"><span data-stu-id="b749d-114">As a platform, vulnerabilities exist such that even benign Gadgets could be exploited.</span></span> <span data-ttu-id="b749d-115">Pertanto, per poter sostenere Windows 8 come sistema operativo più moderno e sicuro, si è scelto di rimuovere i gadget dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b749d-115">Therefore, in order to uphold Windows 8 as our most modern and secure operating system, we have chosen to remove Gadgets from the operating system entirely.</span></span> <span data-ttu-id="b749d-116">Gli utenti di Windows 7 con gadget sul desktop riceveranno una notifica e i gadget verranno disinstallati.</span><span class="sxs-lookup"><span data-stu-id="b749d-116">Windows 7 users with Gadgets on their Desktop will be notified and Gadgets will be uninstalled.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b749d-117">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="b749d-117">Manifestation</span></span>

<span data-ttu-id="b749d-118">I gadget desktop non saranno disponibili sul desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="b749d-118">Desktop Gadgets will not be available on the Windows Desktop.</span></span>

## <a name="mitigation"></a><span data-ttu-id="b749d-119">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="b749d-119">Mitigation</span></span>

<span data-ttu-id="b749d-120">L'API gadget desktop e la struttura di cartelle rimarranno invariate per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b749d-120">The Desktop Gadgets API and folder structure will remain in place for Windows 8.</span></span> <span data-ttu-id="b749d-121">Le applicazioni che installano ed eseguono i Gadget a livello di codice tramite questa API continueranno a funzionare senza errori (anche se i gadget non lo sono).</span><span class="sxs-lookup"><span data-stu-id="b749d-121">Applications which programmatically install and run Gadgets using this API will continue to run without fail (although the Gadgets themselves will not).</span></span>

## <a name="solution"></a><span data-ttu-id="b749d-122">Soluzione</span><span class="sxs-lookup"><span data-stu-id="b749d-122">Solution</span></span>

<span data-ttu-id="b749d-123">Gli sviluppatori di app desktop non devono creare pacchetti di gadget nei programmi di installazione.</span><span class="sxs-lookup"><span data-stu-id="b749d-123">Desktop app developers should not package Gadgets in their installers.</span></span> <span data-ttu-id="b749d-124">In questi gadget sarà sufficiente spazio per l'utente e non sarà possibile eseguirlo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b749d-124">These Gadgets will just take up space for the user and will not be able to be run in the system.</span></span>

## <a name="tests"></a><span data-ttu-id="b749d-125">Test</span><span class="sxs-lookup"><span data-stu-id="b749d-125">Tests</span></span>

<span data-ttu-id="b749d-126">Gli sviluppatori sono in grado di testare la compatibilità di questa modifica disabilitando il componente facoltativo per i gadget desktop in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b749d-126">Developers are able to test compatibility of this change by disabling the optional component for Desktop Gadgets in Windows 7.</span></span> <span data-ttu-id="b749d-127">Per disabilitare i gadget in un PC Windows 7, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="b749d-127">To disable Gadgets on a Windows 7 PC, follow the steps below:</span></span>

1.  <span data-ttu-id="b749d-128">Passare a attivare o disattivare le funzionalità Windows dal pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="b749d-128">Navigate to Turn Windows Features on or off from the Control Panel.</span></span>
2.  <span data-ttu-id="b749d-129">Deselezionare la casella accanto a "piattaforma Gadget Windows".</span><span class="sxs-lookup"><span data-stu-id="b749d-129">Uncheck the box next to “Windows Gadget Platform”.</span></span>
3.  <span data-ttu-id="b749d-130">Fare clic su OK e seguire le istruzioni aggiuntive sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="b749d-130">Click OK and follow any additional on-screen instructions.</span></span>

## <a name="resources"></a><span data-ttu-id="b749d-131">Risorse</span><span class="sxs-lookup"><span data-stu-id="b749d-131">Resources</span></span>

[<span data-ttu-id="b749d-132">Le vulnerabilità nei gadget potrebbero consentire l'esecuzione di codice in modalità remota</span><span class="sxs-lookup"><span data-stu-id="b749d-132">Vulnerabilities in Gadgets Could Allow Remote Code Execution</span></span>](https://support.microsoft.com/kb/2719662)

 

 




