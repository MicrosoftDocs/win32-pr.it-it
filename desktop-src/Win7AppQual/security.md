---
description: Sicurezza (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sicurezza (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f320f4cb561079380e19a969eba95f3f6b321fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116229"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="1e9e6-103">Sicurezza (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="1e9e6-103">Security (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="1e9e6-104">A partire da Windows Internet Explorer 7, Windows Internet Explorer viene eseguito  in un contesto di sicurezza denominato Modalità protetta quando gli utenti la eseguono nel sistema operativo Windows Vista o in una versione successiva.</span><span class="sxs-lookup"><span data-stu-id="1e9e6-104">Starting with Windows Internet Explorer 7, Windows Internet Explorer runs in a security context called *Protected Mode* when users run it on the Windows Vista operating system or a later version.</span></span> <span data-ttu-id="1e9e6-105">Questa modalità viene Internet Explorer in un'impostazione con privilegi inferiori rispetto a un'applicazione utente standard, quindi alcune funzionalità sono limitate, in particolare i controlli ActiveX e alcuni tipi di plug-in. Per altre informazioni sulla modalità protetta in Internet Explorer e sul relativo impatto sulla compatibilità, vedere Understanding [and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="1e9e6-105">This mode runs Internet Explorer in a lower-privilege setting than a standard user application so certain functionality is limited, especially ActiveX controls and certain types of plug-ins. For more information about Protected Mode in Internet Explorer and its impact on compatibility, see [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the MSDN Library.</span></span>

<span data-ttu-id="1e9e6-106">Per impostazione predefinita, Windows Internet Explorer 8 abilita anche Protezione esecuzione programmi, che consente alle applicazioni di evitare l'esecuzione di codice arbitrario negli attacchi online.</span><span class="sxs-lookup"><span data-stu-id="1e9e6-106">By default, Windows Internet Explorer 8 also enables Data Execution Prevention (DEP), which helps applications avoid running arbitrary code in online attacks.</span></span> <span data-ttu-id="1e9e6-107">Tuttavia, alcuni componenti aggiuntivi potrebbero non usare questa funzionalità di sicurezza( ad esempio, tutti i componenti aggiuntivi che non sono progettati per eseguire solo il codice che si trova in memoria che è stato contrassegnato in modo specifico come eseguibile, ad esempio le applicazioni compilate usando una versione precedente del framework ATL (ActiveX Template Library).</span><span class="sxs-lookup"><span data-stu-id="1e9e6-107">However, some add-ons might not use this security feature (for example, any add-ons that are not designed to run only code that is located in memory that has been specifically marked as executable, such as applications that are built by using an older version of the ActiveX Template Library (ATL) framework).</span></span>

<span data-ttu-id="1e9e6-108">Internet Explorer 8 protegge anche gli utenti da potenziali vulnerabilità della sicurezza che usano script.</span><span class="sxs-lookup"><span data-stu-id="1e9e6-108">Internet Explorer 8 also protects users against potential security vulnerabilities that use scripts.</span></span> <span data-ttu-id="1e9e6-109">Ad esempio, non è possibile passare da un URL in un'area meno attendibile a un URL in un'area più attendibile, tranne tramite l'interazione esplicita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1e9e6-109">For example, you cannot navigate from a URL in a less trusted zone to a URL in a more trusted zone except through explicit user interaction.</span></span> <span data-ttu-id="1e9e6-110">Non è inoltre possibile nascondere determinati elementi dell'interfaccia utente del browser, ad esempio la barra degli indirizzi, in un'area non attendibile (Internet).</span><span class="sxs-lookup"><span data-stu-id="1e9e6-110">You also cannot hide certain elements of the browser’s user interface (such as the address bar) in an un-trusted (Internet) zone.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e9e6-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e9e6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e9e6-112">Progettare aggiornamenti che influiscono sulla compatibilità tra browser</span><span class="sxs-lookup"><span data-stu-id="1e9e6-112">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
