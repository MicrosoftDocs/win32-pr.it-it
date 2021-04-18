---
title: Uso del controllo ActiveX Desktop remoto
description: Come è possibile utilizzare il controllo ActiveX Desktop remoto per personalizzare l'esperienza utente Servizi Desktop remoto.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto utilizzando il controllo ActiveX Desktop remoto
- Connessione Web Desktop remoto Servizi Desktop remoto utilizzando
- Remote Desktop Protocol Servizi Desktop remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297923"
---
# <a name="using-the-remote-desktop-activex-control"></a><span data-ttu-id="5c82c-106">Uso del controllo ActiveX Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="5c82c-106">Using the Remote Desktop ActiveX control</span></span>

<span data-ttu-id="5c82c-107">Negli argomenti seguenti sono contenute informazioni su come utilizzare il controllo ActiveX Desktop remoto per personalizzare l'esperienza utente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5c82c-107">The following topics contain information about how you can use the Remote Desktop ActiveX control to customize the Remote Desktop Services user experience.</span></span>

<span data-ttu-id="5c82c-108">Il controllo ActiveX Desktop remoto è disponibile nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c82c-108">The Remote Desktop ActiveX control is available in the following forms:</span></span>

-   <span data-ttu-id="5c82c-109">**Il controllo eseguibile tramite script**, implementa interfacce sicure per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="5c82c-109">**The scriptable control**—implements interfaces that are safe for scripting.</span></span> <span data-ttu-id="5c82c-110">Questo formato del controllo può essere utilizzato da client Web o script (ad esempio VBScript).</span><span class="sxs-lookup"><span data-stu-id="5c82c-110">This form of the control can be used by web clients or scripting (such as VBScript) hosts.</span></span>
-   <span data-ttu-id="5c82c-111">**Il controllo** non utilizzabile per gli script: offre funzionalità aggiuntive che non sono sicure per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="5c82c-111">**The nonscriptable control**—offers additional functionality that is not safe for scripting.</span></span> <span data-ttu-id="5c82c-112">Questo formato del controllo può essere utilizzato da codice nativo o gestito, ma non può essere utilizzato dai client Web o dagli host solo script.</span><span class="sxs-lookup"><span data-stu-id="5c82c-112">This form of the control can be used from native or managed code, but this form cannot be used by web clients or scripting-only hosts.</span></span>

<span data-ttu-id="5c82c-113">Nell'elenco seguente sono inclusi i **CLSID** per i diversi controlli per diverse versioni del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5c82c-113">The following list contains the **CLSID** s for the different controls for different operating system versions.</span></span> <span data-ttu-id="5c82c-114">Ogni **CLSID** è compatibile con versioni di sistema successive.</span><span class="sxs-lookup"><span data-stu-id="5c82c-114">Each of the **CLSID** s is compatible with later system versions.</span></span> <span data-ttu-id="5c82c-115">Il **CLSID** per il controllo di scripting in Windows Vista, ad esempio, funzionerà con versioni di sistema successive, ad esempio Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c82c-115">For example, the **CLSID** for the scriptable control on Windows Vista will work on later system versions, such as Windows 7.</span></span>



| <span data-ttu-id="5c82c-116">Versione sistema</span><span class="sxs-lookup"><span data-stu-id="5c82c-116">System version</span></span>                          | <span data-ttu-id="5c82c-117">CLSID controllo con script</span><span class="sxs-lookup"><span data-stu-id="5c82c-117">Scriptable control CLSID</span></span>             | <span data-ttu-id="5c82c-118">CLSID di controllo non conscriptbile</span><span class="sxs-lookup"><span data-stu-id="5c82c-118">Nonscriptable control CLSID</span></span>          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| <span data-ttu-id="5c82c-119">Windows 8.1, Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5c82c-119">Windows 8.1, Windows Server 2012 R2</span></span>     | <span data-ttu-id="5c82c-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="5c82c-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span> | <span data-ttu-id="5c82c-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="5c82c-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span> |
| <span data-ttu-id="5c82c-122">Windows 8, Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c82c-122">Windows 8, Windows Server 2012</span></span>          | <span data-ttu-id="5c82c-123">5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="5c82c-123">5F681803-2900-4C43-A1CC-CF405404A676</span></span> | <span data-ttu-id="5c82c-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="5c82c-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span> |
| <span data-ttu-id="5c82c-125">Windows 7, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c82c-125">Windows 7, Windows Server 2008</span></span>          | <span data-ttu-id="5c82c-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="5c82c-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span> | <span data-ttu-id="5c82c-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="5c82c-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span> |
| <span data-ttu-id="5c82c-128">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="5c82c-128">Windows Vista with Service Pack 1 (SP1)</span></span> | <span data-ttu-id="5c82c-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span><span class="sxs-lookup"><span data-stu-id="5c82c-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span></span> | <span data-ttu-id="5c82c-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span><span class="sxs-lookup"><span data-stu-id="5c82c-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span></span> |
| <span data-ttu-id="5c82c-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c82c-131">Windows Vista</span></span>                           | <span data-ttu-id="5c82c-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span><span class="sxs-lookup"><span data-stu-id="5c82c-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span></span> | <span data-ttu-id="5c82c-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span><span class="sxs-lookup"><span data-stu-id="5c82c-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="5c82c-134">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="5c82c-134">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="5c82c-135">Incorporamento del controllo ActiveX Desktop remoto in una pagina Web</span><span class="sxs-lookup"><span data-stu-id="5c82c-135">Embedding the Remote Desktop ActiveX control in a webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

<span data-ttu-id="5c82c-136">Esempio che illustra l'uso delle interfacce di scripting.</span><span class="sxs-lookup"><span data-stu-id="5c82c-136">Example that demonstrates the use of the scriptable interfaces.</span></span>

</dd> <dt>

[<span data-ttu-id="5c82c-137">Implementazione di canali virtuali tramite script tramite Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="5c82c-137">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="5c82c-138">Esempi di codice che illustrano i passaggi per l'implementazione di canali virtuali utilizzabili tramite script con Connessione Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5c82c-138">Code examples that show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="5c82c-139">Uso del controllo ActiveX Desktop remoto con i canali virtuali</span><span class="sxs-lookup"><span data-stu-id="5c82c-139">Using the Remote Desktop ActiveX control with virtual channels</span></span>](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="5c82c-140">Se è stata abilitata un'applicazione per i canali virtuali nella distribuzione di Servizi Desktop remoto, è possibile rendere disponibile questa applicazione per i computer client.</span><span class="sxs-lookup"><span data-stu-id="5c82c-140">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers.</span></span>

</dd> <dt>

[<span data-ttu-id="5c82c-141">Pagina Web di esempio inclusa con il controllo ActiveX Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="5c82c-141">Sample webpage included with the Remote Desktop ActiveX control</span></span>](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="5c82c-142">Una pagina Web di esempio (Default.htm) si trova nella directory in cui è installato Connessione Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5c82c-142">A sample webpage (Default.htm) is in the directory where Remote Desktop Web Connection is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="5c82c-143">Fornire la sicurezza del client RDP</span><span class="sxs-lookup"><span data-stu-id="5c82c-143">Providing for RDP client security</span></span>](providing-for-rdp-client-security.md)
</dt> <dd>

<span data-ttu-id="5c82c-144">Alcune proprietà dell'oggetto Desktop remoto controllo ActiveX sono limitate a specifiche aree di sicurezza URL di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5c82c-144">Some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span>

</dd> <dt>

[<span data-ttu-id="5c82c-145">Disabilitazione delle funzionalità di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="5c82c-145">Disabling Remote Desktop Services features</span></span>](disabling-terminal-services-features.md)
</dt> <dd>

<span data-ttu-id="5c82c-146">Per una maggiore sicurezza, è possibile scegliere di disabilitare Servizi Desktop remoto funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5c82c-146">For enhanced security, you might choose to disable Remote Desktop Services features.</span></span>

</dd> </dl>

<span data-ttu-id="5c82c-147">Per ulteriori informazioni sulla pagina Web di esempio inclusa nell'installazione del controllo ActiveX Desktop remoto, vedere [la pagina Web di esempio inclusa nel controllo activex desktop remoto](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span><span class="sxs-lookup"><span data-stu-id="5c82c-147">For more information about the sample webpage that is included with the installation of the Remote Desktop ActiveX control, see [Sample webpage included with the Remote Desktop ActiveX control](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span></span>

 

 




