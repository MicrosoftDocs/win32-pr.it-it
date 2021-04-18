---
description: Abilitazione dei controlli di accesso a livello di componente
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Abilitazione dei controlli di accesso a livello di componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304620"
---
# <a name="enabling-access-checks-at-the-component-level"></a><span data-ttu-id="dde71-103">Abilitazione dei controlli di accesso a livello di componente</span><span class="sxs-lookup"><span data-stu-id="dde71-103">Enabling Access Checks at the Component Level</span></span>

<span data-ttu-id="dde71-104">Se l'applicazione include un componente che non necessita di controlli di sicurezza, è possibile decidere di disabilitare i controlli dei ruoli per il componente per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="dde71-104">If your application includes a component that does not need security checks, you might decide to disable role checks for that component to improve performance.</span></span> <span data-ttu-id="dde71-105">O durante il debug, potrebbe essere utile disabilitare la sicurezza in modo da potersi concentrare su altri aspetti della funzionalità del programma.</span><span class="sxs-lookup"><span data-stu-id="dde71-105">Or when debugging, it might be helpful to disable security so that you can concentrate on other aspects of program functionality.</span></span>

<span data-ttu-id="dde71-106">Per impostazione predefinita, quando si installa un componente sono abilitati i controlli di accesso a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="dde71-106">By default, when you install a component, component-level access checks are enabled.</span></span> <span data-ttu-id="dde71-107">Questa operazione ha tuttavia effetto solo quando sono abilitati i [controlli di accesso a livello di applicazione](enabling-access-checks-for-an-application.md) e quando il livello di [sicurezza](setting-a-security-level-for-access-checks.md) è impostato in modo da eseguire i **controlli di accesso a livello di processo e di componente**.</span><span class="sxs-lookup"><span data-stu-id="dde71-107">However, this takes effect only when [application-level access checks](enabling-access-checks-for-an-application.md) are enabled and when the [security level](setting-a-security-level-for-access-checks.md) is set to **Perform access checks at the process and component level**.</span></span>

<span data-ttu-id="dde71-108">**Per abilitare o disabilitare i controlli di accesso a livello di componente**</span><span class="sxs-lookup"><span data-stu-id="dde71-108">**To enable or disable access checks at the component level**</span></span>

1.  <span data-ttu-id="dde71-109">Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il componente per il quale si desidera disabilitare o abilitare i controlli dei ruoli.</span><span class="sxs-lookup"><span data-stu-id="dde71-109">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the component for which you want to disable (or enable) role checks.</span></span> <span data-ttu-id="dde71-110">Espandere la visualizzazione nell'albero per visualizzare i componenti nella cartella **Components** .</span><span class="sxs-lookup"><span data-stu-id="dde71-110">Expand the view in the tree to view the components in the **Components** folder.</span></span>

2.  <span data-ttu-id="dde71-111">Fare clic con il pulsante destro del mouse sul componente per il quale si desidera abilitare i controlli dei ruoli, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="dde71-111">Right-click the component for which you want to enable role checks, and then click **Properties**.</span></span>

3.  <span data-ttu-id="dde71-112">Nella finestra di dialogo Proprietà componente fare clic sulla scheda **sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="dde71-112">In the component properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="dde71-113">Selezionare **Applica controlli di accesso a livello di componente** per applicare i controlli a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="dde71-113">Select **Enforce component level access checks** to enforce component-level checks.</span></span>

5.  <span data-ttu-id="dde71-114">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="dde71-114">Click **OK**.</span></span>

<span data-ttu-id="dde71-115">La nuova impostazione diverrà effettiva al successivo avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dde71-115">The new setting will take effect the next time the application is started.</span></span>

> [!Note]  
> <span data-ttu-id="dde71-116">A partire da Windows Server 2003, i controlli di accesso a livello di componente sono disabilitati per impostazione predefinita durante la creazione di un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="dde71-116">As of Windows Server 2003, component-level access checks are disabled by default when creating a COM+ application.</span></span> <span data-ttu-id="dde71-117">I controlli di accesso sono abilitati per impostazione predefinita a livello di applicazione e disabilitati per impostazione predefinita a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="dde71-117">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="dde71-118">In precedenza, i controlli di accesso erano disabilitati per impostazione predefinita a livello di applicazione e abilitati per impostazione predefinita a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="dde71-118">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dde71-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dde71-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dde71-120">Assegnazione di ruoli a componenti, interfacce o metodi</span><span class="sxs-lookup"><span data-stu-id="dde71-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="dde71-121">Configurazione della sicurezza Role-Based</span><span class="sxs-lookup"><span data-stu-id="dde71-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="dde71-122">Definizione dei ruoli per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="dde71-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="dde71-123">Abilitazione dei controlli di accesso per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="dde71-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="dde71-124">Impostazione di un livello di sicurezza per i controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="dde71-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



