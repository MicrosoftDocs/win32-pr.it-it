---
description: Abilitazione dell'autenticazione per un'applicazione di libreria
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Abilitazione dell'autenticazione per un'applicazione di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305012"
---
# <a name="enabling-authentication-for-a-library-application"></a><span data-ttu-id="5d801-103">Abilitazione dell'autenticazione per un'applicazione di libreria</span><span class="sxs-lookup"><span data-stu-id="5d801-103">Enabling Authentication for a Library Application</span></span>

<span data-ttu-id="5d801-104">Poiché le applicazioni di libreria COM+ sono ospitate da altri processi, i requisiti di sicurezza possono essere diversi da quelli delle applicazioni server.</span><span class="sxs-lookup"><span data-stu-id="5d801-104">Because COM+ library applications are hosted by other processes, their security requirements may be different from those of server applications.</span></span> <span data-ttu-id="5d801-105">Se l'applicazione di libreria sarà ospitata da un browser, potrebbe essere necessario ricevere callback non autenticati.</span><span class="sxs-lookup"><span data-stu-id="5d801-105">If the library application will be hosted by a browser, it might need to receive unauthenticated callbacks.</span></span>

<span data-ttu-id="5d801-106">Per rispondere a questa esigenza, è possibile disabilitare l'autenticazione in modo che il processo di hosting non esegua controlli di sicurezza per i chiamanti dell'applicazione della libreria.</span><span class="sxs-lookup"><span data-stu-id="5d801-106">To address this need, you can disable authentication so that the hosting process does not perform security checks for callers of the library application.</span></span> <span data-ttu-id="5d801-107">Quando si disabilita l'autenticazione, le chiamate all'applicazione di libreria vengono eseguite in modo non autenticato. tutte le chiamate ad essa verranno eseguite correttamente.</span><span class="sxs-lookup"><span data-stu-id="5d801-107">When you disable authentication, calls to the library application effectively go unauthenticated—all calls to it will succeed.</span></span> <span data-ttu-id="5d801-108">Per ulteriori informazioni, vedere la pagina relativa alla [sicurezza delle applicazioni di libreria](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="5d801-108">For more information, see [Library Application Security](library-application-security.md).</span></span>

<span data-ttu-id="5d801-109">**Per abilitare o disabilitare l'autenticazione per un'applicazione di libreria**</span><span class="sxs-lookup"><span data-stu-id="5d801-109">**To enable (or disable) authentication for a library application**</span></span>

1.  <span data-ttu-id="5d801-110">Fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si sta abilitando o disabilitando l'autenticazione, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="5d801-110">Right-click the COM+ application for which you are enabling or disabling authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="5d801-111">Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="5d801-111">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="5d801-112">In **autenticazione** selezionare la casella di controllo **Abilita autenticazione** per abilitare l'autenticazione. Se si deseleziona la casella di controllo, l'autenticazione viene disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5d801-112">Under **Authentication**, select the **Enable authentication** check box to enable authentication; clearing the check box will disable authentication.</span></span>

4.  <span data-ttu-id="5d801-113">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d801-113">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d801-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d801-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d801-115">Impostazione di un livello di autenticazione per un'applicazione server</span><span class="sxs-lookup"><span data-stu-id="5d801-115">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



