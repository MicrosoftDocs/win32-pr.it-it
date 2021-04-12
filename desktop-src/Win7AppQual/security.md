---
description: .
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sicurezza (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbaaa6b34463e04f5870082e5c693462f4e19fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234330"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="fe74e-103">Sicurezza (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="fe74e-103">Security (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="fe74e-104">A partire da Windows Internet Explorer 7, Windows Internet Explorer viene eseguito in un contesto di sicurezza denominato *modalità protetta* quando gli utenti eseguono il sistema operativo Windows Vista o una versione successiva.</span><span class="sxs-lookup"><span data-stu-id="fe74e-104">Starting with Windows Internet Explorer 7, Windows Internet Explorer runs in a security context called *Protected Mode* when users run it on the Windows Vista operating system or a later version.</span></span> <span data-ttu-id="fe74e-105">Questa modalità esegue Internet Explorer in un'impostazione con privilegi inferiori rispetto a un'applicazione utente standard, in modo che alcune funzionalità siano limitate, in particolare i controlli ActiveX e determinati tipi di plug-in. Per ulteriori informazioni sulla modalità protetta in Internet Explorer e sul relativo effetto sulla compatibilità, vedere [informazioni e utilizzo in modalità protetta di Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="fe74e-105">This mode runs Internet Explorer in a lower-privilege setting than a standard user application so certain functionality is limited, especially ActiveX controls and certain types of plug-ins. For more information about Protected Mode in Internet Explorer and its impact on compatibility, see [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the MSDN Library.</span></span>

<span data-ttu-id="fe74e-106">Per impostazione predefinita, Windows Internet Explorer 8 Abilita anche protezione esecuzione programmi, che consente alle applicazioni di evitare l'esecuzione di codice arbitrario negli attacchi online.</span><span class="sxs-lookup"><span data-stu-id="fe74e-106">By default, Windows Internet Explorer 8 also enables Data Execution Prevention (DEP), which helps applications avoid running arbitrary code in online attacks.</span></span> <span data-ttu-id="fe74e-107">Tuttavia, alcuni componenti aggiuntivi potrebbero non utilizzare questa funzionalità di sicurezza (ad esempio, eventuali componenti aggiuntivi non progettati per eseguire solo codice che si trova in memoria che è stato contrassegnato come eseguibile, ad esempio le applicazioni compilate utilizzando una versione precedente del framework ATL (ActiveX Template Library).</span><span class="sxs-lookup"><span data-stu-id="fe74e-107">However, some add-ons might not use this security feature (for example, any add-ons that are not designed to run only code that is located in memory that has been specifically marked as executable, such as applications that are built by using an older version of the ActiveX Template Library (ATL) framework).</span></span>

<span data-ttu-id="fe74e-108">Internet Explorer 8 protegge anche gli utenti da potenziali vulnerabilità della sicurezza che usano gli script.</span><span class="sxs-lookup"><span data-stu-id="fe74e-108">Internet Explorer 8 also protects users against potential security vulnerabilities that use scripts.</span></span> <span data-ttu-id="fe74e-109">Ad esempio, non è possibile passare da un URL in una zona meno attendibile a un URL in una zona più attendibile, ad eccezione dell'interazione esplicita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fe74e-109">For example, you cannot navigate from a URL in a less trusted zone to a URL in a more trusted zone except through explicit user interaction.</span></span> <span data-ttu-id="fe74e-110">Non è inoltre possibile nascondere alcuni elementi dell'interfaccia utente del browser (ad esempio la barra degli indirizzi) in una zona non attendibile (Internet).</span><span class="sxs-lookup"><span data-stu-id="fe74e-110">You also cannot hide certain elements of the browser’s user interface (such as the address bar) in an un-trusted (Internet) zone.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe74e-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe74e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe74e-112">Aggiornamenti della progettazione che incidono sulla compatibilità tra browser</span><span class="sxs-lookup"><span data-stu-id="fe74e-112">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
