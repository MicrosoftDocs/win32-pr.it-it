---
title: Fornire la sicurezza del client RDP
description: Alcune proprietà dell'oggetto Desktop remoto controllo ActiveX sono limitate a specifiche aree di sicurezza URL di Internet Explorer.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710186"
---
# <a name="providing-for-rdp-client-security"></a><span data-ttu-id="4a228-103">Fornire la sicurezza del client RDP</span><span class="sxs-lookup"><span data-stu-id="4a228-103">Providing for RDP client security</span></span>

<span data-ttu-id="4a228-104">Per consentire ai client di proteggersi da server potenzialmente non attendibili, alcune proprietà dell'oggetto controllo Desktop remoto ActiveX sono limitate a aree di sicurezza URL Internet Explorer specifiche.</span><span class="sxs-lookup"><span data-stu-id="4a228-104">To allow clients to protect themselves from potentially untrustworthy servers, some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="4a228-105">Ciò significa che, quando un utente che visita il Web accede alla pagina e la pagina si trova in un'area di sicurezza con URL superiore rispetto al computer con cui si sta esplorando il Web, queste proprietà sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="4a228-105">This means that, when a user browsing the web accesses the page and the page is in a higher URL security zone than the computer they are browsing the web with, these properties are disabled.</span></span> <span data-ttu-id="4a228-106">Queste proprietà limitate sono accessibili tramite l'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) e l'interfaccia [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) e sono disponibili nelle aree di sicurezza URL Internet Explorer seguenti:</span><span class="sxs-lookup"><span data-stu-id="4a228-106">These restricted properties are accessed using the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface and the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and are available in the following Internet Explorer URL security zones:</span></span>

-   <span data-ttu-id="4a228-107">Risorse del computer</span><span class="sxs-lookup"><span data-stu-id="4a228-107">My computer</span></span>
-   <span data-ttu-id="4a228-108">Intranet locale</span><span class="sxs-lookup"><span data-stu-id="4a228-108">Local intranet</span></span>
-   <span data-ttu-id="4a228-109">Siti attendibili</span><span class="sxs-lookup"><span data-stu-id="4a228-109">Trusted sites</span></span>

<span data-ttu-id="4a228-110">Sono disabilitate in queste zone:</span><span class="sxs-lookup"><span data-stu-id="4a228-110">They are disabled in these zones:</span></span>

-   <span data-ttu-id="4a228-111">Internet</span><span class="sxs-lookup"><span data-stu-id="4a228-111">Internet</span></span>
-   <span data-ttu-id="4a228-112">Siti con restrizioni</span><span class="sxs-lookup"><span data-stu-id="4a228-112">Restricted sites</span></span>

<span data-ttu-id="4a228-113">Se si chiamano queste proprietà limitate all'interno dell'applicazione Servizi Desktop remoto Web, è necessario chiamare [**IMsTscAx:: Get \_ SecuredSettings**](imstscax-securedsettings.md) e [**IMsTscAx:: Get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) per accedere alle proprietà delle impostazioni protette.</span><span class="sxs-lookup"><span data-stu-id="4a228-113">If you call these restricted properties within your Remote Desktop Services web application, you should call [**IMsTscAx::get\_SecuredSettings**](imstscax-securedsettings.md) and [**IMsTscAx::get\_SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) to access the Secured Settings properties.</span></span>

<span data-ttu-id="4a228-114">Di seguito sono riportate le proprietà limitate a cui accede l'interfaccia **IMsTscSecuredSettings** :</span><span class="sxs-lookup"><span data-stu-id="4a228-114">The restricted properties that the **IMsTscSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="4a228-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="4a228-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span> <span data-ttu-id="4a228-116">Questa proprietà specifica il programma che verrà avviato alla connessione.</span><span class="sxs-lookup"><span data-stu-id="4a228-116">This property specifies the program that will be started upon connection.</span></span>
-   <span data-ttu-id="4a228-117">[**Workdir**](imstscsecuredsettings-workdir.md).</span><span class="sxs-lookup"><span data-stu-id="4a228-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span></span> <span data-ttu-id="4a228-118">Questa proprietà specifica la directory di lavoro del programma specificato in [**StartProgram**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="4a228-118">This property specifies the working directory of the program specified in [**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span>
-   <span data-ttu-id="4a228-119">A [**schermo intero**](imstscsecuredsettings-fullscreen.md).</span><span class="sxs-lookup"><span data-stu-id="4a228-119">[**FullScreen**](imstscsecuredsettings-fullscreen.md).</span></span> <span data-ttu-id="4a228-120">Questa proprietà specifica se lo stato del controllo alla connessione sarà in modalità schermo intero o finestra.</span><span class="sxs-lookup"><span data-stu-id="4a228-120">This property specifies whether the state of the control upon connection will be in full-screen or window mode.</span></span> <span data-ttu-id="4a228-121">Se il valore di questa proprietà è **true**, la connessione verrà aperta in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="4a228-121">If the value of this property is **TRUE**, the connection will be opened in full-screen mode.</span></span> <span data-ttu-id="4a228-122">Sebbene l'utilizzo della proprietà **FullScreen** sia limitato alle zone di sicurezza URL di Internet Explorer elencate in precedenza, un utente può sempre passare alla modalità schermo intero dopo la connessione premendo la combinazione di tasti di [scelta rapida](terminal-services-shortcut-keys.md) per la modalità schermo intero (CTRL + ALT + INTERR).</span><span class="sxs-lookup"><span data-stu-id="4a228-122">Although the use of the **FullScreen** property is restricted to the Internet Explorer URL security zones listed earlier, a user can always change to full-screen mode after connection by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="4a228-123">Di seguito sono riportate le proprietà a cui accede l'interfaccia **IMsRdpClientSecuredSettings** :</span><span class="sxs-lookup"><span data-stu-id="4a228-123">The properties that the **IMsRdpClientSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="4a228-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span><span class="sxs-lookup"><span data-stu-id="4a228-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span></span> <span data-ttu-id="4a228-125">Questa proprietà specifica se reindirizzare i suoni o riprodurre suoni nel server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="4a228-125">This property specifies whether to redirect sounds, or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>
-   <span data-ttu-id="4a228-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span><span class="sxs-lookup"><span data-stu-id="4a228-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span></span> <span data-ttu-id="4a228-127">Questa proprietà specifica come e quando applicare le combinazioni di tasti di Windows; ad esempio ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="4a228-127">This property specifies how and when to apply Windows key combinations; for example, ALT+TAB.</span></span>

<span data-ttu-id="4a228-128">Lo script seguente avvia Microsoft Notepad.exe al momento della connessione.</span><span class="sxs-lookup"><span data-stu-id="4a228-128">The following script launches Microsoft Notepad.exe upon connection.</span></span> <span data-ttu-id="4a228-129">Eseguire questo script prima di chiamare il metodo [**IMsTscAx:: Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="4a228-129">Run this script before calling the [**IMsTscAx::Connect**](imstscax-connect.md) method.</span></span>

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




