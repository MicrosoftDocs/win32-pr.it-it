---
description: .
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Controllo delle versioni del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e71cb671e19463ca6137c9b0ce7af04c2793e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318571"
---
# <a name="operating-system-versioning"></a><span data-ttu-id="52bd8-103">Controllo delle versioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="52bd8-103">Operating System Versioning</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="52bd8-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="52bd8-104">Affected Platforms</span></span>

<span data-ttu-id="52bd8-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="52bd8-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="52bd8-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="52bd8-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="52bd8-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="52bd8-107">Feature Impact</span></span>

<span data-ttu-id="52bd8-108">**Gravità** -alta</span><span class="sxs-lookup"><span data-stu-id="52bd8-108">**Severity** - High</span></span>  
<span data-ttu-id="52bd8-109">**Frequenza** -alta</span><span class="sxs-lookup"><span data-stu-id="52bd8-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="52bd8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52bd8-110">Description</span></span>

<span data-ttu-id="52bd8-111">Il numero di versione interno per Windows 7 e Windows Server 2008 R2 è 6,1.</span><span class="sxs-lookup"><span data-stu-id="52bd8-111">The internal version number for Windows 7 and Windows Server 2008 R2 is 6.1.</span></span> <span data-ttu-id="52bd8-112">La funzione GetVersion restituisce ora questo numero di versione alle applicazioni quando viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="52bd8-112">The GetVersion function will now return this version number to applications when queried.</span></span> <span data-ttu-id="52bd8-113">Questa operazione è particolarmente importante per l'AntiVirus, il backup, le applicazioni di utilità e la protezione della copia.</span><span class="sxs-lookup"><span data-stu-id="52bd8-113">This is especially important for AntiVirus, backup, utility applications, and copy protection.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="52bd8-114">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="52bd8-114">Manifestation of Impact</span></span>

<span data-ttu-id="52bd8-115">La manifestazione di questa modifica è specifica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52bd8-115">The manifestation of this change is application-specific.</span></span> <span data-ttu-id="52bd8-116">Ciò significa che qualsiasi applicazione che verifica in modo specifico la versione del sistema operativo otterrà un numero di versione superiore, che può causare una o più delle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="52bd8-116">This means that any application that specifically checks for the operating system version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="52bd8-117">I programmi di installazione delle applicazioni potrebbero non essere in grado di installare l'applicazione e le applicazioni potrebbero non essere in grado di avviarsi</span><span class="sxs-lookup"><span data-stu-id="52bd8-117">Application installers might be unable to install the application, and applications might be unable to start</span></span>
-   <span data-ttu-id="52bd8-118">Le applicazioni potrebbero diventare instabili o arrestarsi</span><span class="sxs-lookup"><span data-stu-id="52bd8-118">Applications might become unstable or crash</span></span>
-   <span data-ttu-id="52bd8-119">Le applicazioni possono generare messaggi di errore, ma continuare a funzionare correttamente</span><span class="sxs-lookup"><span data-stu-id="52bd8-119">Applications might generate error messages, but continue to function properly</span></span>

## <a name="mitigation"></a><span data-ttu-id="52bd8-120">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="52bd8-120">Mitigation</span></span>

<span data-ttu-id="52bd8-121">La maggior parte delle applicazioni funziona correttamente in Windows 7 e Windows Server 2008 R2 perché la compatibilità delle applicazioni in Windows 7 e Windows Server 2008 R2 è molto elevata.</span><span class="sxs-lookup"><span data-stu-id="52bd8-121">Most applications will function properly on Windows 7 and Windows Server 2008 R2 because the application compatibility in Windows 7 and Windows Server 2008 R2 is very high.</span></span> <span data-ttu-id="52bd8-122">Tuttavia, Windows 7 e Windows Server 2008 R2 includono una visualizzazione di compatibilità per i programmi di installazione e le applicazioni che controllano la versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="52bd8-122">However, Windows 7 and Windows Server 2008 R2 include a Compatibility View for installers and applications that check for operating system version.</span></span>

<span data-ttu-id="52bd8-123">Per abilitare la visualizzazione compatibilità, gli utenti possono fare clic con il pulsante destro del mouse sul collegamento o sul file eseguibile, quindi applicare la visualizzazione compatibilità di Windows XP SP2 o Windows Vista dalla scheda compatibilità. Nella maggior parte dei casi, questa operazione dovrebbe consentire il funzionamento corretto dell'applicazione senza la necessità di apportare modifiche all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52bd8-123">To enable the compatibility view, users can right-click the shortcut or the executable file, and then apply the Windows XP SP2 or Windows Vista Compatibility View from the Compatibility tab. In most cases, this should enable the application to operate properly without the need for any changes to the application.</span></span>

<span data-ttu-id="52bd8-124">I professionisti IT possono inoltre applicare le correzioni di compatibilità di VersionLie applicabili usando lo strumento Compatibility Administrator, che viene installato con Application Compatibility Toolkit (ACT).</span><span class="sxs-lookup"><span data-stu-id="52bd8-124">IT Professionals can also apply any of the applicable VersionLie compatibility fixes, by using the Compatibility Administrator tool, which installs with the Application Compatibility Toolkit (ACT).</span></span> <span data-ttu-id="52bd8-125">Se, ad esempio, un'applicazione non riesce a funzionare perché sta controllando, ma non trova, le informazioni sulla versione di Windows XP® con Service Pack 2 (SP2), è possibile applicare WinXPSP2VersionLie per restituire le informazioni sul numero di versione appropriate all'applicazione, indipendentemente dalla versione effettiva del sistema operativo in esecuzione nel computer.</span><span class="sxs-lookup"><span data-stu-id="52bd8-125">For example, if an application fails to function because it is checking for, but not finding, the Windows XP® with Service Pack 2 (SP2) version information, the WinXPSP2VersionLie can be applied to return the proper version number information to the application, regardless of the actual operating system version that is running on the computer.</span></span> <span data-ttu-id="52bd8-126">Le correzioni di compatibilità di VersionLie disponibili sono:</span><span class="sxs-lookup"><span data-stu-id="52bd8-126">The available VersionLie compatibility fixes are:</span></span>

-   <span data-ttu-id="52bd8-127">Win95VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-127">Win95VersionLie</span></span>
-   <span data-ttu-id="52bd8-128">Win98VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-128">Win98VersionLie</span></span>
-   <span data-ttu-id="52bd8-129">WinNT4SP5VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-129">WinNT4SP5VersionLie</span></span>
-   <span data-ttu-id="52bd8-130">Win2000VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-130">Win2000VersionLie</span></span>
-   <span data-ttu-id="52bd8-131">Win2000SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-131">Win2000SP1VersionLie</span></span>
-   <span data-ttu-id="52bd8-132">Win2000SP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-132">Win2000SP2VersionLie</span></span>
-   <span data-ttu-id="52bd8-133">Win2000SP3VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-133">Win2000SP3VersionLie</span></span>
-   <span data-ttu-id="52bd8-134">WinXPVersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-134">WinXPVersionLie</span></span>
-   <span data-ttu-id="52bd8-135">WinXPSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-135">WinXPSP1VersionLie</span></span>
-   <span data-ttu-id="52bd8-136">WinXPSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-136">WinXPSP2VersionLie</span></span>
-   <span data-ttu-id="52bd8-137">VistaRTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-137">VistaRTMVersionLie</span></span>
-   <span data-ttu-id="52bd8-138">VistaSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-138">VistaSP1VersionLie</span></span>
-   <span data-ttu-id="52bd8-139">VistaSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-139">VistaSP2VersionLie</span></span>
-   <span data-ttu-id="52bd8-140">Win2K3RTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-140">Win2K3RTMVersionLie</span></span>
-   <span data-ttu-id="52bd8-141">Win2K3SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="52bd8-141">Win2K3SP1VersionLie</span></span>

## <a name="solution"></a><span data-ttu-id="52bd8-142">Soluzione</span><span class="sxs-lookup"><span data-stu-id="52bd8-142">Solution</span></span>

<span data-ttu-id="52bd8-143">In genere, le applicazioni non devono eseguire controlli della versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="52bd8-143">Generally, applications should not perform operating system version checks.</span></span> <span data-ttu-id="52bd8-144">Se un'applicazione necessita di una funzionalità specifica, è preferibile provare a individuare la funzionalità e non riuscire solo se manca la funzionalità necessaria.</span><span class="sxs-lookup"><span data-stu-id="52bd8-144">If an application needs a specific feature, it is preferable to try to find the feature, and fail only if the needed feature is missing.</span></span> <span data-ttu-id="52bd8-145">Come minimo, le applicazioni devono sempre accettare i numeri di versione maggiori o uguali alla versione più bassa supportata del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="52bd8-145">At a minimum, applications should always accept version numbers greater than or equal to the lowest supported version of the operating system.</span></span> <span data-ttu-id="52bd8-146">Le eccezioni dovrebbero verificarsi solo se è presente un requisito specifico per i componenti legali, aziendali o di sistema.</span><span class="sxs-lookup"><span data-stu-id="52bd8-146">Exceptions should occur only if there is a specific legal, business, or system-component requirement.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="52bd8-147">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="52bd8-147">Links to Other Resources</span></span>

-   [<span data-ttu-id="52bd8-148">Download di Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="52bd8-148">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="52bd8-149">[Correzioni di compatibilità note, modalità di compatibilità e messaggi AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="52bd8-149">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>

 

 
