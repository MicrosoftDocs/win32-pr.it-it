---
description: In questo documento vengono fornite informazioni sulle considerazioni relative alla sicurezza relative all'acquisizione di immagini Windows (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Considerazioni sulla sicurezza: acquisizione di immagini Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307336"
---
# <a name="security-considerations-windows-image-acquisition"></a><span data-ttu-id="ca700-103">Considerazioni sulla sicurezza: acquisizione di immagini Windows</span><span class="sxs-lookup"><span data-stu-id="ca700-103">Security Considerations: Windows Image Acquisition</span></span>

<span data-ttu-id="ca700-104">In questo documento vengono fornite informazioni sulle considerazioni relative alla sicurezza relative all'acquisizione di immagini Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="ca700-104">This document provides information about security considerations related to Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="ca700-105">Questo documento non fornisce tutte le informazioni necessarie per i problemi di sicurezza, ma è possibile usarlo come punto di partenza e come riferimento per questa area tecnologica.</span><span class="sxs-lookup"><span data-stu-id="ca700-105">This document doesn't provide all you need to know about security issues - instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="ca700-106">Racchiudere tra virgolette i nomi di percorso</span><span class="sxs-lookup"><span data-stu-id="ca700-106">Use quotation marks around path names</span></span>](#use-quotation-marks-around-path-names)
-   [<span data-ttu-id="ca700-107">Inserire applicazioni registrate in posizioni sicure</span><span class="sxs-lookup"><span data-stu-id="ca700-107">Place registered applications in secure locations</span></span>](#place-registered-applications-in-secure-locations)
-   [<span data-ttu-id="ca700-108">Non usare directory sottostanti o chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ca700-108">Do not use underlying directories or registry keys</span></span>](#do-not-use-underlying-directories-or-registry-keys)
-   [<span data-ttu-id="ca700-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca700-109">Related Topics</span></span>](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a><span data-ttu-id="ca700-110">Racchiudere tra virgolette i nomi di percorso</span><span class="sxs-lookup"><span data-stu-id="ca700-110">Use quotation marks around path names</span></span>

<span data-ttu-id="ca700-111">Quando si usa [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) per registrare un'applicazione per la ricezione di eventi del dispositivo, assicurarsi di racchiudere il percorso e il nome file dell'applicazione con virgolette.</span><span class="sxs-lookup"><span data-stu-id="ca700-111">When using [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register an application to receive device events, be sure to surround the path and filename of the application with quotation marks.</span></span> <span data-ttu-id="ca700-112">In questo modo si evita la possibilità che il percorso venga interpretato erroneamente e venga eseguita un'applicazione non autorizzata.</span><span class="sxs-lookup"><span data-stu-id="ca700-112">This avoids the possibility that the path is misinterpreted and an unauthorized application is run.</span></span>

## <a name="place-registered-applications-in-secure-locations"></a><span data-ttu-id="ca700-113">Inserire applicazioni registrate in posizioni sicure</span><span class="sxs-lookup"><span data-stu-id="ca700-113">Place registered applications in secure locations</span></span>

<span data-ttu-id="ca700-114">Quando un'applicazione viene registrata per ricevere un evento del dispositivo, l'applicazione può essere eseguita da qualsiasi utente che abbia accesso a tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca700-114">When an application is registered to receive a device event, that application can be run by any user that has access to that device.</span></span> <span data-ttu-id="ca700-115">Se, ad esempio, un'applicazione è registrata per un evento di analisi, quando si preme il pulsante "analizza" su uno scanner verrà eseguita l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ca700-115">For example, if an application is registered for a scan event, pressing the "scan" button on a scanner will cause that application to run.</span></span> <span data-ttu-id="ca700-116">Se l'applicazione viene eseguita con un privilegio più elevato rispetto a quello dell'utente, questo causa un potenziale problema di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ca700-116">If the application runs with a higher privilege than the user has, this causes a potential security issue.</span></span>

## <a name="do-not-use-underlying-directories-or-registry-keys"></a><span data-ttu-id="ca700-117">Non usare directory sottostanti o chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ca700-117">Do not use underlying directories or registry keys</span></span>

<span data-ttu-id="ca700-118">WIA utilizza internamente più directory e chiavi del registro di sistema per archiviare dati o informazioni.</span><span class="sxs-lookup"><span data-stu-id="ca700-118">WIA uses several directories and registry keys internally to store data or information.</span></span> <span data-ttu-id="ca700-119">Non accedere direttamente a tali directory o chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ca700-119">Do not access these directories or registry keys directly.</span></span> <span data-ttu-id="ca700-120">Usare invece i metodi di interfaccia esposti per specificare le directory per le immagini acquisite.</span><span class="sxs-lookup"><span data-stu-id="ca700-120">Instead, use the exposed interface methods to specify directories for acquired images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca700-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca700-121">Related Topics</span></span>

-   [<span data-ttu-id="ca700-122">Microsoft Security</span><span class="sxs-lookup"><span data-stu-id="ca700-122">Microsoft Security</span></span>](https://www.microsoft.com/security/)
-   [<span data-ttu-id="ca700-123">Home page di sicurezza MSDN Library</span><span class="sxs-lookup"><span data-stu-id="ca700-123">MSDN Library Security Home Page</span></span>](https://msdn.microsoft.com/security/default.aspx)
-   [<span data-ttu-id="ca700-124">Risorse sulle procedure di sicurezza</span><span class="sxs-lookup"><span data-stu-id="ca700-124">Security How-to Resources</span></span>](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [<span data-ttu-id="ca700-125">Risorse di sicurezza TechNet</span><span class="sxs-lookup"><span data-stu-id="ca700-125">TechNet Security Resources</span></span>](https://technet.microsoft.com/security/default.aspx)
-   <span data-ttu-id="ca700-126">[Considerazioni sulla sicurezza per gli sviluppatori di Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ca700-126">[Security Considerations for Windows XP Embedded Developers](/previous-versions/ms838345(v=msdn.10))</span></span>
-   [<span data-ttu-id="ca700-127">Procedure di sicurezza consigliate</span><span class="sxs-lookup"><span data-stu-id="ca700-127">Security Best Practices</span></span>](../secbp/best-practices-for-the-security-apis.md)

 

 
