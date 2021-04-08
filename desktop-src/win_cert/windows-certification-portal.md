---
title: Certificare l'applicazione desktop
description: Seguire questa procedura per ottenere la certificazione dell'app desktop per Windows 7, Windows 8, Windows 8.1 e Windows 10. Se si vuole convertire l'app desktop in modo che sia compatibile con i piattaforma UWP (Universal Windows Platform) e Windows Store, si userà Windows Desktop Bridge. in questo caso, è necessario seguire le indicazioni sul Bridge per la procedura di certificazione. Se si sta sviluppando e certificando un'app UWP dall'inizio, vedere linee guida per la certificazione delle app Windows in UWP per informazioni sulla certificazione.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734559"
---
# <a name="certify-your-desktop-application"></a><span data-ttu-id="7a587-103">Certificare l'applicazione desktop</span><span class="sxs-lookup"><span data-stu-id="7a587-103">Certify your desktop application</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a587-104">La certificazione per le applicazioni desktop Win32 è [deprecata](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span><span class="sxs-lookup"><span data-stu-id="7a587-104">Certification for Win32 desktop apps is [deprecated](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span></span> <span data-ttu-id="7a587-105">Inviare invece [i file qui](https://www.microsoft.com/wdsi/filesubmission/).</span><span class="sxs-lookup"><span data-stu-id="7a587-105">Instead, [submit files here](https://www.microsoft.com/wdsi/filesubmission/).</span></span>

<span data-ttu-id="7a587-106">Seguire questa procedura per ottenere la certificazione dell'app desktop per Windows 7, Windows 8, Windows 8.1 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7a587-106">Follow these steps to get your desktop app certified for Windows 7, Windows 8, Windows 8.1, and Windows 10.</span></span>

<span data-ttu-id="7a587-107">Se si vuole convertire l'app desktop in modo che sia compatibile con il piattaforma UWP (Universal Windows Platform) e Windows Store, si userà [Windows Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop). in questo caso, è necessario seguire le indicazioni sul Bridge per i [Desktop](/windows/uwp/porting/desktop-to-uwp-root) per le procedure di certificazione.</span><span class="sxs-lookup"><span data-stu-id="7a587-107">If you wish to convert your desktop app to be compatible with the Universal Windows Platform and Windows Store, you will use the [Windows Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop), in which case you should follow the [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) guidance for certification steps.</span></span>

<span data-ttu-id="7a587-108">Se si sta sviluppando e certificando un'app UWP dall'inizio, vedere [linee guida per la certificazione delle app Windows in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) per informazioni sulla certificazione.</span><span class="sxs-lookup"><span data-stu-id="7a587-108">If you are developing and certifying a UWP app from the start, see [Guidance for Windows App Certification in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) for info on certification.</span></span>

## <a name="step-1-prepare-for-certification"></a><span data-ttu-id="7a587-109">Passaggio 1: preparare la certificazione</span><span class="sxs-lookup"><span data-stu-id="7a587-109">Step 1: Prepare for certification</span></span>



| <span data-ttu-id="7a587-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="7a587-110">Topic</span></span>                                                                                       | <span data-ttu-id="7a587-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a587-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a587-112">Quali sono i vantaggi?</span><span class="sxs-lookup"><span data-stu-id="7a587-112">What are the benefits?</span></span>](what-are-the-benefits-.md)<br/>                             | <span data-ttu-id="7a587-113">La certificazione dell'app desktop offre diversi vantaggi per l'utente e i clienti.</span><span class="sxs-lookup"><span data-stu-id="7a587-113">Certifying your desktop app provides several benefits for you and your customers.</span></span>              |
| [<span data-ttu-id="7a587-114">Leggere i requisiti</span><span class="sxs-lookup"><span data-stu-id="7a587-114">Read the requirements</span></span>](certification-requirements-for-windows-desktop-apps.md)<br/> | <span data-ttu-id="7a587-115">Esaminare i requisiti tecnici e le qualifiche di idoneità che devono essere soddisfatte da un'applicazione desktop.</span><span class="sxs-lookup"><span data-stu-id="7a587-115">Review the technical requirements and eligibility qualifications that a desktop app must meet.</span></span> |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a><span data-ttu-id="7a587-116">Passaggio 2: testare l'app con il kit di certificazione app Windows</span><span class="sxs-lookup"><span data-stu-id="7a587-116">Step 2: Test your app with the Windows App Certification Kit</span></span>



| <span data-ttu-id="7a587-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="7a587-117">Topic</span></span>                                                          | <span data-ttu-id="7a587-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a587-118">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a587-119">Ottenere il kit</span><span class="sxs-lookup"><span data-stu-id="7a587-119">Get the Kit</span></span>](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | <span data-ttu-id="7a587-120">Per certificare l'app, è necessario installare ed eseguire il kit di certificazione applicazioni Windows (incluso nella Windows SDK).</span><span class="sxs-lookup"><span data-stu-id="7a587-120">To certify your app, you have to install and run the Windows App Certification Kit (included in the Windows SDK).</span></span>                                                                     |
| [<span data-ttu-id="7a587-121">Uso del kit</span><span class="sxs-lookup"><span data-stu-id="7a587-121">Using the Kit</span></span>](using-the-windows-app-certification-kit.md)   | <span data-ttu-id="7a587-122">Prima di poter inviare l'app, è necessario testarla per verificarne la conformità.</span><span class="sxs-lookup"><span data-stu-id="7a587-122">Before you can submit your app, you must test it for readiness.</span></span> <span data-ttu-id="7a587-123">È anche possibile scaricare una copia della [white paper di certificazione dell'app](https://www.microsoft.com/download/details.aspx?id=27414).</span><span class="sxs-lookup"><span data-stu-id="7a587-123">You can also download a copy of the [app certification white paper](https://www.microsoft.com/download/details.aspx?id=27414).</span></span> |
| [<span data-ttu-id="7a587-124">Esaminare i dettagli del test</span><span class="sxs-lookup"><span data-stu-id="7a587-124">Review test details</span></span>](windows-app-certification-kit-tests.md) | <span data-ttu-id="7a587-125">Ottenere l'elenco dei test che devono essere superati dall'app per qualificarsi per la compatibilità con il sistema operativo Windows più recente.</span><span class="sxs-lookup"><span data-stu-id="7a587-125">Get the list of the tests your app needs to pass to qualify for compatibility with the latest Windows operating system.</span></span>                                                               |



 

<span data-ttu-id="7a587-126">Nota: i driver di filtro devono anche passare il [Kit di certificazione hardware](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span><span class="sxs-lookup"><span data-stu-id="7a587-126">Note: Filter drivers must also pass the [Hardware Certification Kit](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span></span> <span data-ttu-id="7a587-127">Vedere [la sezione 6,2 relativa ai requisiti di certificazione per le app desktop di Windows](certification-requirements-for-windows-desktop-apps.md).</span><span class="sxs-lookup"><span data-stu-id="7a587-127">(See [Certification requirements for Windows desktop apps, section 6.2](certification-requirements-for-windows-desktop-apps.md).)</span></span>

## <a name="step-3-use-the-windows-certification-dashboard"></a><span data-ttu-id="7a587-128">Passaggio 3: usare il dashboard di certificazione di Windows</span><span class="sxs-lookup"><span data-stu-id="7a587-128">Step 3: Use the Windows Certification Dashboard</span></span>

<span data-ttu-id="7a587-129">Per inviare l'app per la certificazione, è necessario accedere o registrare un account aziendale nel [Dashboard certificazione Windows](/previous-versions/hh833792(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="7a587-129">To submit your app for certification, you'll need to log in or register a company account on the [Windows Certification Dashboard](/previous-versions/hh833792(v=msdn.10)).</span></span> <span data-ttu-id="7a587-130">Una volta eseguita questa operazione, non solo sarà possibile ottenere la certificazione dell'app, ma si otterrà anche l'accesso agli strumenti per rivedere e gestire l'app in tutte le fasi del processo.</span><span class="sxs-lookup"><span data-stu-id="7a587-130">Once you do, not only will you be able to get your app certified, but you'll also gain access to tools to review and manage your app at all stages of the process.</span></span>



| <span data-ttu-id="7a587-131">Argomento</span><span class="sxs-lookup"><span data-stu-id="7a587-131">Topic</span></span>                                                                                                                   | <span data-ttu-id="7a587-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a587-132">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a587-133">Configurare l'account</span><span class="sxs-lookup"><span data-stu-id="7a587-133">Set up your account</span></span>](/windows-hardware/drivers/dashboard/)                 | <span data-ttu-id="7a587-134">Se la società non è già registrata, è necessario registrarla tramite il dashboard di certificazione Windows.</span><span class="sxs-lookup"><span data-stu-id="7a587-134">If your company isn't already registered, you must register it through the Windows Certification Dashboard.</span></span>                                        |
| [<span data-ttu-id="7a587-135">Ottenere un certificato di firma del codice</span><span class="sxs-lookup"><span data-stu-id="7a587-135">Get a code signing certificate</span></span>](/windows-hardware/drivers/dashboard/)      | <span data-ttu-id="7a587-136">Prima di poter stabilire un account dashboard di certificazione Windows, è necessario ottenere un certificato di firma codice per proteggere le informazioni digitali.</span><span class="sxs-lookup"><span data-stu-id="7a587-136">Before you can establish a Windows Certification Dashboard account, you need to get a code signing certificate to secure your digital information.</span></span> |
| [<span data-ttu-id="7a587-137">Testare localmente e caricare i risultati</span><span class="sxs-lookup"><span data-stu-id="7a587-137">Test locally and upload the results</span></span>](/windows-hardware/drivers/dashboard/) | <span data-ttu-id="7a587-138">Dopo aver eseguito i test del kit di certificazione app Windows, caricare i risultati nel dashboard di certificazione Windows.</span><span class="sxs-lookup"><span data-stu-id="7a587-138">After your run the Windows App Certification Kit tests, upload the results to the Windows Certification Dashboard.</span></span>                                 |
| [<span data-ttu-id="7a587-139">Gestire l'invio</span><span class="sxs-lookup"><span data-stu-id="7a587-139">Manage your submission</span></span>](/windows-hardware/drivers/dashboard/)              | <span data-ttu-id="7a587-140">Dopo aver inviato l'app per la certificazione, è possibile esaminare l'invio tramite il dashboard di certificazione Windows.</span><span class="sxs-lookup"><span data-stu-id="7a587-140">After you submit your app for certification, you can review your submission through the Windows Certification Dashboard.</span></span>                           |



 

## <a name="step-4-promote-your-desktop-app"></a><span data-ttu-id="7a587-141">Passaggio 4: promuovere l'app desktop</span><span class="sxs-lookup"><span data-stu-id="7a587-141">Step 4: Promote your desktop app</span></span>



| <span data-ttu-id="7a587-142">Argomento</span><span class="sxs-lookup"><span data-stu-id="7a587-142">Topic</span></span>                                                                      | <span data-ttu-id="7a587-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a587-143">Description</span></span>                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a587-144">Verifica compatibilità app</span><span class="sxs-lookup"><span data-stu-id="7a587-144">Check app compatibility</span></span>](/windows/compatibility/windows-8-1-introduction) | <span data-ttu-id="7a587-145">Se si compila un'app per Windows 8.1, analizzare i problemi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="7a587-145">If you are building an app for Windows 8.1, investigate compatibility concerns.</span></span>                                           |
| [<span data-ttu-id="7a587-146">Usare il logo con l'app</span><span class="sxs-lookup"><span data-stu-id="7a587-146">Use the logo with your app</span></span>](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | <span data-ttu-id="7a587-147">Consente di visualizzare il logo nella creazione di pacchetti e negli annunci e in altri materiali promozionali in base alle linee guida.</span><span class="sxs-lookup"><span data-stu-id="7a587-147">Display the logo on packaging and in ads and other promotional materials according to the guidelines.</span></span> <span data-ttu-id="7a587-148">Solo per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a587-148">For Windows 7 only.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="7a587-149">Vedere anche la pagina relativa alla</span><span class="sxs-lookup"><span data-stu-id="7a587-149">See also:</span></span>

<span data-ttu-id="7a587-150">[Forum sulla compatibilità delle app](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): supporto della community sulla compatibilità e sulla certificazione del logo.</span><span class="sxs-lookup"><span data-stu-id="7a587-150">[App compatibility forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): Find support from the community about compatibility and logo certification.</span></span>

<span data-ttu-id="7a587-151">[Blog Windows SDK](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): suggerimenti e notizie relativi alla certificazione delle app.</span><span class="sxs-lookup"><span data-stu-id="7a587-151">[Windows SDK blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Find tips and news related to app certification.</span></span>

<span data-ttu-id="7a587-152">[Forum su Windows Server]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): visitare il forum di certificazione per ottenere risposte.</span><span class="sxs-lookup"><span data-stu-id="7a587-152">[Windows Server forum]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): Visit the Certification forum to get answers.</span></span>

<span data-ttu-id="7a587-153">[Cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)per la compatibilità: informazioni sulle novità o le modifiche apportate alla versione più recente di Windows.</span><span class="sxs-lookup"><span data-stu-id="7a587-153">[Compatibility cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Get info about what's new or changed in the latest version of Windows.</span></span>

 

