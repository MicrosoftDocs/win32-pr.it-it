---
title: Estensione dell'interfaccia utente per gli oggetti directory
description: Con Microsoft Windows 2000 e versioni successive, gli snap-in di Microsoft Management Console (MMC), ad esempio lo snap-in Active Directory utenti e computer, per l'amministrazione di Active Directory Domain Services sono disponibili.
ms.assetid: 758ec25d-42ab-46ba-aa58-416d7ac8fd68
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, estensione dell'interfaccia utente
- oggetti AD, estensione dell'interfaccia utente per gli oggetti directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d635132a26e80a63fddb35f779211308779f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707621"
---
# <a name="extending-the-user-interface-for-directory-objects"></a><span data-ttu-id="4139d-105">Estensione dell'interfaccia utente per gli oggetti directory</span><span class="sxs-lookup"><span data-stu-id="4139d-105">Extending the User Interface for Directory Objects</span></span>

<span data-ttu-id="4139d-106">Con Microsoft Windows 2000 e versioni successive, gli snap-in di Microsoft Management Console (MMC), ad esempio lo snap-in Active Directory utenti e computer, per l'amministrazione di Active Directory Domain Services sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="4139d-106">With Microsoft Windows 2000 and later, Microsoft Management Console (MMC) snap-ins, such as the Active Directory Users and Computers snap-in, for administration of Active Directory Domain Services, are available.</span></span> <span data-ttu-id="4139d-107">Inoltre, la shell di Windows 2000 include le interfacce utente (UI) per individuare gli oggetti che risiedono nella directory e le proprietà di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="4139d-107">In addition, the Windows 2000 shell includes user interfaces (UIs) for finding objects that reside in the directory and reading and writing properties.</span></span> <span data-ttu-id="4139d-108">In questa sezione viene illustrato come estendere l'interfaccia utente per la visualizzazione e la gestione di oggetti Active Directory Domain Services nella shell di Windows e Active Directory snap-in amministrativi. Questa sezione descrive anche gli elementi necessari per distribuire le estensioni dell'interfaccia utente sui desktop dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4139d-108">This section explains how to extend the UI for viewing and managing Active Directory Domain Services objects in the Windows shell and Active Directory administrative snap-ins. This section also covers what is required to deploy the UI extensions to the user's desktops.</span></span>

<span data-ttu-id="4139d-109">In particolare, in questa sezione vengono descritte le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4139d-109">Specifically, this section discusses the following:</span></span>

-   [<span data-ttu-id="4139d-110">Informazioni sulle interfacce utente Active Directory</span><span class="sxs-lookup"><span data-stu-id="4139d-110">About Active Directory User Interfaces</span></span>](about-the-user-interfaces-of-active-directory-domain-services.md)
-   [<span data-ttu-id="4139d-111">Identificatori di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="4139d-111">Display Specifiers</span></span>](display-specifiers.md)
-   [<span data-ttu-id="4139d-112">Nomi visualizzati della classe e dell'attributo</span><span class="sxs-lookup"><span data-stu-id="4139d-112">Class and Attribute Display Names</span></span>](class-and-attribute-display-names.md)
-   [<span data-ttu-id="4139d-113">Icone della classe</span><span class="sxs-lookup"><span data-stu-id="4139d-113">Class Icons</span></span>](class-icons.md)
-   [<span data-ttu-id="4139d-114">Visualizzazione di contenitori come nodi foglia</span><span class="sxs-lookup"><span data-stu-id="4139d-114">Viewing Containers as Leaf Nodes</span></span>](viewing-containers-as-leaf-nodes.md)
-   [<span data-ttu-id="4139d-115">Modifica di interfacce utente esistenti</span><span class="sxs-lookup"><span data-stu-id="4139d-115">Modifying Existing User Interfaces</span></span>](modifying-existing-user-interfaces.md)
-   [<span data-ttu-id="4139d-116">Estensione dell'interfaccia utente per le nuove classi di oggetti</span><span class="sxs-lookup"><span data-stu-id="4139d-116">User Interface Extension for New Object Classes</span></span>](user-interface-extension-for-new-object-classes.md)
-   [<span data-ttu-id="4139d-117">Pagine delle proprietà da usare con gli identificatori di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="4139d-117">Property Pages for Use with Display Specifiers</span></span>](property-pages-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="4139d-118">Menu di scelta rapida da usare con gli identificatori di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="4139d-118">Context Menus for Use with Display Specifiers</span></span>](context-menus-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="4139d-119">Creazione guidata oggetto</span><span class="sxs-lookup"><span data-stu-id="4139d-119">Object Creation Wizards</span></span>](object-creation-wizards.md)
-   [<span data-ttu-id="4139d-120">Utilizzo delle finestre di dialogo standard per la gestione di oggetti in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="4139d-120">Using Standard Dialog Boxes for Handling Objects in Active Directory Domain Services</span></span>](using-standard-dialog-boxes-to-handle-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="4139d-121">Gestori di notifiche amministrative</span><span class="sxs-lookup"><span data-stu-id="4139d-121">Administrative Notification Handlers</span></span>](administrative-notification-handlers.md)
-   [<span data-ttu-id="4139d-122">Distribuzione dei componenti dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4139d-122">Distributing User Interface Components</span></span>](distributing-user-interface-components.md)
-   [<span data-ttu-id="4139d-123">Come le applicazioni devono usare gli identificatori di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="4139d-123">How Applications Should Use Display Specifiers</span></span>](how-applications-should-use-display-specifiers.md)
-   [<span data-ttu-id="4139d-124">Debug di un'estensione Active Directory</span><span class="sxs-lookup"><span data-stu-id="4139d-124">Debugging an Active Directory Extension</span></span>](debugging-an-active-directory-extension.md)

 

 




