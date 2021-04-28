---
description: Servizi Desktop remoto (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Servizi Desktop remoto (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725844d49f465c3c79dbc19fd01ec0f18b09759e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116119"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="d7792-103">Servizi Desktop remoto (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="d7792-103">Remote Desktop Services (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="d7792-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="d7792-104">Affected Platforms</span></span>

<span data-ttu-id="d7792-105">**Server** : Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d7792-105">**Servers** – Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="d7792-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7792-106">Description</span></span>

<span data-ttu-id="d7792-107">Servizi Desktop remoto (precedentemente noto come Servizi terminal) consente a più utenti simultanei di accedere a Windows Server per fornire servizi di hosting di applicazioni e dati usando la tecnologia Microsoft "Presentation Virtualization".</span><span class="sxs-lookup"><span data-stu-id="d7792-107">Remote Desktop Services (formerly known as Terminal Services) allows multiple concurrent users to access Windows Server in order to provide application and data hosting services using Microsoft "Presentation Virtualization" technology.</span></span>

<span data-ttu-id="d7792-108">Mentre la maggior parte delle applicazioni a 32 bit e a 64 bit viene eseguita così come è in Windows Servizi Desktop remoto, molte altre non vengono eseguite come previsto a causa della differenza nella piattaforma (ambiente multi-utente, accesso simultaneo da parte di più utenti e così via).</span><span class="sxs-lookup"><span data-stu-id="d7792-108">While most 32-bit and 64-bit applications run as is on Windows Remote Desktop Services, several others do not perform as expected due to the difference in the platform (multi-user environment, concurrent access by multiple users, and so on).</span></span>

<span data-ttu-id="d7792-109">Per altre informazioni sulla qualità dell'applicazione, vedere *La conformità delle applicazioni per Servizi terminal* white paper.</span><span class="sxs-lookup"><span data-stu-id="d7792-109">For further information regarding application quality, please read the *Application Readiness for Terminal Services* white paper.</span></span> <span data-ttu-id="d7792-110">Visitare la pagina Servizi Desktop remoto del prodotto e i siti Web TechNet di TS per altre informazioni Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="d7792-110">Visit the Remote Desktop Services product page and the TS TechNet websites learn more about Remote Desktop Services.</span></span> <span data-ttu-id="d7792-111">Per altre informazioni sullo sviluppo di applicazioni per Servizi Desktop remoto, vedere Linee guida per la *programmazione di Servizi terminal.*</span><span class="sxs-lookup"><span data-stu-id="d7792-111">To learn more about developing applications for Remote Desktop Services, review the *Terminal Services Programming Guidelines*.</span></span> <span data-ttu-id="d7792-112">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="d7792-112">(These resources may not be available in some languages and countries/regions.)</span></span>

## <a name="manifestation-of-impacts-and-their-mitigations"></a><span data-ttu-id="d7792-113">Riduzione degli effetti e delle relative mitigazioni</span><span class="sxs-lookup"><span data-stu-id="d7792-113">Manifestation of Impacts and Their Mitigations</span></span>

<span data-ttu-id="d7792-114">Tre modifiche in Windows 7 influiscono sulle applicazioni in Servizi Desktop remoto:</span><span class="sxs-lookup"><span data-stu-id="d7792-114">Three changes in Windows 7 affect applications on Remote Desktop Services:</span></span>

-   <span data-ttu-id="d7792-115">Windows Server 2008 R2 è solo a 64 bit</span><span class="sxs-lookup"><span data-stu-id="d7792-115">Windows Server 2008 R2 is 64-bit only</span></span>
-   <span data-ttu-id="d7792-116">Virtualizzazione IP per sessione</span><span class="sxs-lookup"><span data-stu-id="d7792-116">Per-session IP Virtualization</span></span>
-   <span data-ttu-id="d7792-117">Distribuzioni basate su MSI: chiavi specifiche dell'utente</span><span class="sxs-lookup"><span data-stu-id="d7792-117">MSI-based deployments – User-specific keys</span></span>

<span data-ttu-id="d7792-118">**Solo Windows Server 2008 R2 a 64 bit**</span><span class="sxs-lookup"><span data-stu-id="d7792-118">**64-bit Only Windows Server 2008 R2**</span></span>

<span data-ttu-id="d7792-119">Le applicazioni scritte per il server a 32 bit verranno eseguite in modalità WoW e non in modo nativo in Windows Server 2008 R2 o, di conseguenza, in Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="d7792-119">Applications written for 32-bit server will run in WoW mode and not natively on the Windows Server 2008 R2 or, hence, on Remote Desktop Services.</span></span> <span data-ttu-id="d7792-120">Per informazioni dettagliate, vedere l'argomento Solo Windows 7 a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="d7792-120">See the Windows 7 64-Bit Only topic for details.</span></span>

<span data-ttu-id="d7792-121">*Mitigazioni solo per Windows Server 2008 R2 a 64 bit*</span><span class="sxs-lookup"><span data-stu-id="d7792-121">*Mitigations for 64-bit only Windows Server 2008 R2*</span></span>

<span data-ttu-id="d7792-122">La maggior parte delle applicazioni scritte a 32 bit continuerà a funzionare normalmente in modalità WoW.</span><span class="sxs-lookup"><span data-stu-id="d7792-122">Most applications written for 32-bit will continue to work as normal in WoW mode.</span></span> <span data-ttu-id="d7792-123">Le nuove applicazioni scritte per Windows 7 Servizi Desktop remoto devono essere sviluppate e testate per la distribuzione in piattaforme a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="d7792-123">Any new applications written for Windows 7 Remote Desktop Services should be developed and tested for deployment on 64-bit platforms.</span></span>

<span data-ttu-id="d7792-124">**Virtualizzazione IP**</span><span class="sxs-lookup"><span data-stu-id="d7792-124">**IP Virtualization**</span></span>

<span data-ttu-id="d7792-125">Virtualizzazione IP di Desktop remoto consente all'utente di assegnare indirizzi IP alle connessioni desktop remoto per sessione o per programma:</span><span class="sxs-lookup"><span data-stu-id="d7792-125">Remote Desktop IP Virtualization allows the user to assign IP addresses to remote desktop connections on a per-session or per-program basis:</span></span>

-   <span data-ttu-id="d7792-126">Se si assegnano indirizzi IP per sessione, tutte le applicazioni useranno l'indirizzo IP della sessione.</span><span class="sxs-lookup"><span data-stu-id="d7792-126">If you assign IP addresses on a per-session basis, all of the applications will use the session IP address.</span></span>
-   <span data-ttu-id="d7792-127">Se si assegnano indirizzi IP in base al programma, solo le applicazioni specificate useranno l'indirizzo IP della sessione e le applicazioni rimanenti nella sessione non saranno interessate.</span><span class="sxs-lookup"><span data-stu-id="d7792-127">If you assign IP addresses on a per-program basis, only the specified applications will use the session IP address and the remaining applications in the session will not be affected.</span></span>
-   <span data-ttu-id="d7792-128">Se si assegnano indirizzi IP per più programmi, questi condivideranno un indirizzo IP di sessione.</span><span class="sxs-lookup"><span data-stu-id="d7792-128">If you assign IP addresses for multiple programs, they will share a session IP address.</span></span>
-   <span data-ttu-id="d7792-129">Se nel computer sono disponibili più schede di rete, è necessario sceglierne una anche per Virtualizzazione IP di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="d7792-129">If you have more than one network adapter on the computer, you must also choose one of them for Remote Desktop IP Virtualization.</span></span>

<span data-ttu-id="d7792-130">*Mitigazioni per la virtualizzazione IP*</span><span class="sxs-lookup"><span data-stu-id="d7792-130">*Mitigations for IP Virtualization*</span></span>

<span data-ttu-id="d7792-131">Alcuni programmi richiedono un indirizzo IP univoco per ogni istanza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7792-131">Some programs require a unique IP address for each instance of the application.</span></span> <span data-ttu-id="d7792-132">Prima di Windows Server 2008 R2, ogni sessione in un server Desktop remoto condivideva lo stesso indirizzo IP, causando problemi di compatibilità per queste applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d7792-132">Prior to Windows Server 2008 R2, every session on a remote desktop server shared the same IP address, resulting in compatibility issues for these applications.</span></span> <span data-ttu-id="d7792-133">Virtualizzazione IP di Desktop remoto consente l'esecuzione di queste applicazioni in un Desktop remoto Server.</span><span class="sxs-lookup"><span data-stu-id="d7792-133">Remote Desktop IP Virtualization allows these applications to run on a Remote Desktop Server.</span></span>

<span data-ttu-id="d7792-134">**Distribuzioni basate su MSI**</span><span class="sxs-lookup"><span data-stu-id="d7792-134">**MSI-based Deployments**</span></span>

<span data-ttu-id="d7792-135">Microsoft Installer RDS Compatibility è una nuova funzionalità inclusa in Servizi Desktop remoto in Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="d7792-135">Microsoft Installer RDS Compatibility is a new feature included with Remote Desktop Services in Windows Server 2008 R2.</span></span> <span data-ttu-id="d7792-136">Con Servizi Desktop remoto in Windows Server 2008 R2, le installazioni di applicazioni per utente vengono accodati da Desktop remoto Server e quindi gestite da Microsoft Installer.</span><span class="sxs-lookup"><span data-stu-id="d7792-136">With Remote Desktop Services in Windows Server 2008 R2, per-user application installations are queued by the Remote Desktop Server and then handled by the Microsoft Installer.</span></span>

<span data-ttu-id="d7792-137">In Windows Server 2008 R2 è possibile installare un programma in Desktop remoto Server esattamente come si farebbe per installare il programma in un desktop locale.</span><span class="sxs-lookup"><span data-stu-id="d7792-137">In Windows Server 2008 R2, you can install a program on the Remote Desktop Server just as you would install the program on a local desktop.</span></span> <span data-ttu-id="d7792-138">Assicurarsi tuttavia di installare il programma per tutti gli utenti e di installare tutti i componenti del programma in locale nel Desktop remoto Server.</span><span class="sxs-lookup"><span data-stu-id="d7792-138">Ensure, however, that you install the program for all users and install all components of the program locally on the Remote Desktop Server.</span></span>

<span data-ttu-id="d7792-139">*Mitigazioni per le distribuzioni basate su MSI*</span><span class="sxs-lookup"><span data-stu-id="d7792-139">*Mitigations for MSI based Deployments*</span></span>

<span data-ttu-id="d7792-140">Prima della versione di Windows Server 2008 R2 di Servizi Desktop remoto, Windows supportava una sola Windows Installer alla volta.</span><span class="sxs-lookup"><span data-stu-id="d7792-140">Prior to the Windows Server 2008 R2 version of Remote Desktop Services, Windows supported only one Windows Installer installation at a time.</span></span> <span data-ttu-id="d7792-141">Per le applicazioni che richiedevano configurazioni per utente, ad esempio Microsoft Office Word, un amministratore doveva preinstallare l'applicazione e gli sviluppatori di applicazioni dovevano testare queste applicazioni sia nel client desktop remoto che nell'host di sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="d7792-141">For applications that required per-user configurations, such as Microsoft Office Word, an administrator needed to pre-install the application, and application developers needed to test these applications on both the remote desktop client and the Remote Desktop Session Host.</span></span> <span data-ttu-id="d7792-142">Windows Installer funzionalità Compatibilità Servizi Desktop remoto consente di identificare e installare configurazioni per utente mancanti per più utenti contemporaneamente e rende l'esperienza di installazione dell'applicazione in Desktop remoto Server simile a quella in un desktop locale.</span><span class="sxs-lookup"><span data-stu-id="d7792-142">Windows Installer RDS Compatibility feature allows identifying and installing missing per-user configurations for multiple users simultaneously and makes the application installation experience on Remote Desktop Server similar to that on a local desktop.</span></span>

<span data-ttu-id="d7792-143">**Windows Server 2008 R2 con il ruolo [Servizi Desktop remoto](../termserv/terminal-services-portal.md) abilitato:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="d7792-143">**Windows Server 2008 R2 with the [Remote Desktop Services](../termserv/terminal-services-portal.md) role enabled:** Not supported.</span></span> <span data-ttu-id="d7792-144">L'installazione di più pacchetti [tramite la tabella MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) ha esito negativo [se il](../termserv/terminal-services-portal.md) Servizi Desktop remoto è abilitato.</span><span class="sxs-lookup"><span data-stu-id="d7792-144">A multiple package installation using the [MsiEmbeddedChainer table](../msi/msiembeddedchainer-table.md) fails if the [Remote Desktop Services](../termserv/terminal-services-portal.md) role is enabled.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="d7792-145">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="d7792-145">Links to Other Resources</span></span>

-   [<span data-ttu-id="d7792-146">Linee guida per la programmazione di Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="d7792-146">Terminal Services Programming Guidelines</span></span>](../termserv/terminal-services-programming-guidelines.md)
-   [<span data-ttu-id="d7792-147">Prodotti di Servizi terminal home page</span><span class="sxs-lookup"><span data-stu-id="d7792-147">Terminal Services product home page</span></span>](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [<span data-ttu-id="d7792-148">Conformità dell'applicazione per Servizi terminal white paper</span><span class="sxs-lookup"><span data-stu-id="d7792-148">Application Readiness for Terminal Services white paper</span></span>](/collaborate/connect-redirect)

> [!Note]  
> <span data-ttu-id="d7792-149">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="d7792-149">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
