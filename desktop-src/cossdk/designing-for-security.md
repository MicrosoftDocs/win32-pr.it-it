---
description: Progettazione per la sicurezza
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Progettazione per la sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304952"
---
# <a name="designing-for-security"></a><span data-ttu-id="0efb8-103">Progettazione per la sicurezza</span><span class="sxs-lookup"><span data-stu-id="0efb8-103">Designing for Security</span></span>

<span data-ttu-id="0efb8-104">La strategia end-to-end per la sicurezza dipende ovviamente dal tipo di applicazione distribuita che si sta sviluppando.</span><span class="sxs-lookup"><span data-stu-id="0efb8-104">Your end-to-end strategy for security obviously depends on the type of distributed application you are developing.</span></span> <span data-ttu-id="0efb8-105">Di seguito sono riportati alcuni suggerimenti per risolvere i problemi di sicurezza rispetto alla logica dell'applicazione di livello intermedio:</span><span class="sxs-lookup"><span data-stu-id="0efb8-105">Following are several suggestions for addressing security with respect to middle-tier application logic:</span></span>

-   <span data-ttu-id="0efb8-106">Per migliorare l'efficienza e le prestazioni, è possibile eseguire l'autenticazione più vicina all'utente.</span><span class="sxs-lookup"><span data-stu-id="0efb8-106">For efficiency and performance, authenticate as close to the user as you can.</span></span> <span data-ttu-id="0efb8-107">Se l'applicazione prevede un'architettura da browser a business da logica a database, provare a eseguire il mapping dei client browser alle identità di dominio, eseguire l'applicazione COM+ in identità specifiche per ogni applicazione e configurare le tabelle nel livello dati in modo che siano accessibili solo da una particolare identità di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0efb8-107">If your application involves a browser-to-business-logic-to-database architecture, consider mapping the browser clients to domain identities, run the COM+ application under identities specific to each application, and configure tables in the data tier to be accessible only by a particular application identity.</span></span> <span data-ttu-id="0efb8-108">Questo scenario server attendibile è più scalabile e meno problematico rispetto all'uso del sistema DBMS per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0efb8-108">This trusted server scenario is more scalable and less problematic than using the DBMS for authenticating.</span></span>
-   <span data-ttu-id="0efb8-109">Se si progetta un componente che verrà utilizzato in un'applicazione distribuita mediante la sicurezza basata sui ruoli, è possibile utilizzare la funzionalità di [sicurezza com+](com--security.md) .</span><span class="sxs-lookup"><span data-stu-id="0efb8-109">If you are designing a component that will be used in a distributed application using role-based security, you can use the [COM+ security](com--security.md) functionality.</span></span> <span data-ttu-id="0efb8-110">Questa funzionalità consente di chiamare metodi quali [**IObjectContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) e [**IObjectContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) per proteggere i blocchi di codice da accessi non autorizzati.</span><span class="sxs-lookup"><span data-stu-id="0efb8-110">This functionality allows you to call methods such as [**IObjectContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) and [**IObjectContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) to help protect blocks of code from unauthorized access.</span></span> <span data-ttu-id="0efb8-111">È anche possibile usare il contesto di chiamata di sicurezza per ottenere informazioni sui chiamanti di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="0efb8-111">You can also use the security call context to get information about an object's callers.</span></span>
-   <span data-ttu-id="0efb8-112">Se si progetta un componente che verrà utilizzato in un'applicazione distribuita senza utilizzare la protezione basata sui ruoli, la sicurezza viene controllata automaticamente solo a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="0efb8-112">If you are designing a component that will be used in a distributed application without using role-based security, security is automatically checked only at the process level.</span></span> <span data-ttu-id="0efb8-113">Le autorizzazioni di accesso al processo determinano a chi viene concesso l'accesso all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0efb8-113">Process access permissions determine who is given access to the application.</span></span> <span data-ttu-id="0efb8-114">Se è necessario un controllo più granulare sulle impostazioni di sicurezza a livello di processo o di interfaccia, utilizzare la funzionalità di sicurezza a livello di codice fornita da COM.</span><span class="sxs-lookup"><span data-stu-id="0efb8-114">If you need finer grain control over security settings at the process or at the interface level, use the programmatic security functionality provided by COM.</span></span>
-   <span data-ttu-id="0efb8-115">Se un componente che utilizza la sicurezza a livello di codice COM+ viene eseguito senza essere integrato in un'applicazione COM+, verranno generate eccezioni.</span><span class="sxs-lookup"><span data-stu-id="0efb8-115">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="0efb8-116">Pertanto, se si desidera che tale componente venga integrato correttamente in un'applicazione che non fa parte dell'ambiente COM+, è necessario gestire tutte le eccezioni in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="0efb8-116">Therefore, if you want such a component to be successfully integrated into an application that is not part of the COM+ environment, you must handle all exceptions appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0efb8-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0efb8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0efb8-118">Progettazione per la disponibilità</span><span class="sxs-lookup"><span data-stu-id="0efb8-118">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="0efb8-119">Progettazione per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="0efb8-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="0efb8-120">Progettazione per la scalabilità</span><span class="sxs-lookup"><span data-stu-id="0efb8-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="0efb8-121">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="0efb8-121">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 



