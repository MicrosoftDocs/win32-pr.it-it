---
title: Verifica automazione interfaccia utente (verifica UIA)
description: Verifica di automazione interfaccia utente (UIA Verify) è un Framework di test per test manuali e automatizzati dell'implementazione di un'applicazione o di un controllo dell'automazione interfaccia utente Microsoft.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- Strumento di verifica dell'automazione interfaccia utente
- Verifica di UIA
- Implementazione di automazione interfaccia utente, test
- test di automazione interfaccia utente
- Strumenti di test di UIA
- Strumenti di test di automazione interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398660"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a><span data-ttu-id="285f3-109">Strumenti di accessibilità-verifica automazione interfaccia utente (verifica UIA)</span><span class="sxs-lookup"><span data-stu-id="285f3-109">Accessibility tools - UI Automation Verify (UIA Verify)</span></span>

<span data-ttu-id="285f3-110">Verifica di **automazione interfaccia utente (UIA Verify)** è un Framework di test per test manuali e automatizzati dell'implementazione di un'applicazione o di un controllo dell'automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="285f3-110">**UI Automation Verify (UIA Verify)** is a testing framework for manual and automated testing of a control's or application's implementation of Microsoft UI Automation.</span></span> <span data-ttu-id="285f3-111">La maggior parte delle funzionalità del Framework di testing deriva da una DLL denominata WUIATestLibrary.dll.</span><span class="sxs-lookup"><span data-stu-id="285f3-111">Most of the testing framework's functionality comes from a DLL called WUIATestLibrary.dll.</span></span> <span data-ttu-id="285f3-112">Questa DLL contiene il codice per il test delle funzionalità specifiche di automazione interfaccia utente e supporta anche la registrazione dei risultati del test.</span><span class="sxs-lookup"><span data-stu-id="285f3-112">This DLL contains the code for testing specific UI Automation functionality, and it also supports logging of the test results.</span></span> <span data-ttu-id="285f3-113">È possibile integrare l'applicazione nel codice di test ed eseguire verifiche regolari e automatizzate dei test o degli scenari di automazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="285f3-113">You can integrate your application into the test code and conduct regular, automated testing or spot checks of your UI Automation scenarios.</span></span>

<span data-ttu-id="285f3-114">La **Verifica di UIA** viene installata con Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="285f3-114">**UIA Verify** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="285f3-115">Si trova nella \\ cartella bin \\ < *versione* > \\ <  > \\ della piattaforma UIAVerify del percorso di installazione SDK (VisualUIAVerifyNative.exe).</span><span class="sxs-lookup"><span data-stu-id="285f3-115">It is located in the \\bin\\<*version*>\\<*platform*>\\UIAVerify folder of the SDK installation path (VisualUIAVerifyNative.exe).</span></span>

<span data-ttu-id="285f3-116">Il metodo di **Verifica** dell'interfaccia utente è costituito da un'API denominata libreria di test di automazione interfaccia utente e da un'interfaccia GUI denominata **Verifica di automazione interfaccia utente**.</span><span class="sxs-lookup"><span data-stu-id="285f3-116">**UIA Verify** consists of an API called the UI Automation Test Library, and a GUI interface called Visual **UI Automation Verify**.</span></span> <span data-ttu-id="285f3-117">Questi argomenti sono descritti negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="285f3-117">These are described in the following topics.</span></span>

> [!NOTE]
> <span data-ttu-id="285f3-118">La **Verifica di automazione interfaccia utente** è uno strumento legacy.</span><span class="sxs-lookup"><span data-stu-id="285f3-118">**UI Automation Verify** is a legacy tool.</span></span> <span data-ttu-id="285f3-119">È invece consigliabile usare [informazioni dettagliate sull'accessibilità](https://accessibilityinsights.io/) .</span><span class="sxs-lookup"><span data-stu-id="285f3-119">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="285f3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="285f3-120">Requirements</span></span>

<span data-ttu-id="285f3-121">Automazione interfaccia utente deve essere presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="285f3-121">UI Automation must be present on the system.</span></span> <span data-ttu-id="285f3-122">Per ulteriori informazioni, vedere la sezione "requisiti" di [automazione interfaccia utente](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="285f3-122">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="285f3-123">La **Verifica di UIA** viene installata come parte del set complessivo di strumenti nel Windows SDK, non viene distribuita come download separato.</span><span class="sxs-lookup"><span data-stu-id="285f3-123">**UIA Verify** is installed as part of the overall set of tools in the Windows SDK, it is not distributed as a separate download.</span></span> <span data-ttu-id="285f3-124">Il Windows SDK include tutti gli strumenti correlati all'accessibilità descritti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="285f3-124">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="285f3-125">Ottenere il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="285f3-125">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="285f3-126">È anche disponibile un archivio di download dell'SDK collegato da tale pagina, se è necessaria una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="285f3-126">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

<span data-ttu-id="285f3-127">Per eseguire la **Verifica di UIA** come strumento visivo, trovare VisualUIAVerifyNative.exe nella \\ cartella bin \\ < *Platform* > \\ UIAVerify ed eseguirlo (in genere non è necessario eseguirlo come amministratore).</span><span class="sxs-lookup"><span data-stu-id="285f3-127">To run **UIA Verify** as a visual tool, find VisualUIAVerifyNative.exe in the \\bin\\<*platform*>\\UIAVerify folder and run it (you don't typically have to run as administrator).</span></span> <span data-ttu-id="285f3-128">Per altre informazioni, vedere [Visual UI Automation Verify](visual-ui-automation-verify.md).</span><span class="sxs-lookup"><span data-stu-id="285f3-128">For more information, see [Visual UI Automation Verify](visual-ui-automation-verify.md).</span></span> <span data-ttu-id="285f3-129">Per usare le librerie, vedere [libreria di test di automazione interfaccia utente](ui-automation-test-library.md).</span><span class="sxs-lookup"><span data-stu-id="285f3-129">To use the libraries, see [UI Automation Test Library](ui-automation-test-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="285f3-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="285f3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="285f3-131">Accessible Event Watcher</span><span class="sxs-lookup"><span data-stu-id="285f3-131">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
</dt> <dt>

[<span data-ttu-id="285f3-132">Controllare</span><span class="sxs-lookup"><span data-stu-id="285f3-132">Inspect</span></span>](inspect-objects.md)
</dt> <dt>

[<span data-ttu-id="285f3-133">Strumenti di test</span><span class="sxs-lookup"><span data-stu-id="285f3-133">Testing Tools</span></span>](testing-tools.md)
</dt> <dt>

[<span data-ttu-id="285f3-134">Verifica dell'accessibilità dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="285f3-134">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




