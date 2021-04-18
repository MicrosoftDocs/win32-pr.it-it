---
description: Per aggiungere Windows Installer funzionalità all'applicazione, usare le funzioni del servizio del programma di installazione.
ms.assetid: 1cb0fd3e-5f39-4a3f-8348-93e74496903d
title: Uso delle funzioni del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4718c462119ac0e5bef018a595d17551561684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307245"
---
# <a name="using-installer-functions"></a><span data-ttu-id="18c74-103">Uso delle funzioni del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="18c74-103">Using Installer Functions</span></span>

<span data-ttu-id="18c74-104">Per aggiungere Windows Installer funzionalità all'applicazione, usare le funzioni del servizio del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="18c74-104">To add Windows Installer functionality to your application, use the installer service functions.</span></span> <span data-ttu-id="18c74-105">Poiché il programma di installazione è un'utilità di installazione e un sistema di gestione dei componenti, un'applicazione che utilizza il programma di installazione deve incorporare le funzioni del servizio del programma di installazione come parte del normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="18c74-105">Because the installer is a setup utility and component management system, an application that uses the installer must incorporate the installer service functions as part of normal operation.</span></span>

<span data-ttu-id="18c74-106">Negli argomenti e nelle procedure seguenti viene illustrato come implementare la funzionalità di installazione nell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="18c74-106">The following topics and procedures explain how to implement installer functionality in your application:</span></span>

-   [<span data-ttu-id="18c74-107">Inizializzazione di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="18c74-107">Initializing an Application</span></span>](initializing-an-application.md)
-   [<span data-ttu-id="18c74-108">Recupero delle informazioni sull'applicazione</span><span class="sxs-lookup"><span data-stu-id="18c74-108">Getting Application Information</span></span>](getting-application-information.md)
-   [<span data-ttu-id="18c74-109">Richiesta di una funzionalità</span><span class="sxs-lookup"><span data-stu-id="18c74-109">Requesting a Feature</span></span>](requesting-a-feature.md)
-   [<span data-ttu-id="18c74-110">Installazione di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="18c74-110">Installing an Application</span></span>](installing-an-application.md)
-   [<span data-ttu-id="18c74-111">Reinstallazione di una funzionalità o di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="18c74-111">Reinstalling a Feature or Application</span></span>](reinstalling-a-feature-or-application.md)
-   [<span data-ttu-id="18c74-112">Rimozione di un'applicazione annunciata</span><span class="sxs-lookup"><span data-stu-id="18c74-112">Removing an Advertised Application</span></span>](removing-an-advertised-application.md)
-   [<span data-ttu-id="18c74-113">Utilizzo delle funzionalità e dei componenti</span><span class="sxs-lookup"><span data-stu-id="18c74-113">Working with Features and Components</span></span>](working-with-features-and-components.md)
-   [<span data-ttu-id="18c74-114">Installazione di un componente mancante</span><span class="sxs-lookup"><span data-stu-id="18c74-114">Installing a Missing Component</span></span>](installing-a-missing-component.md)
-   [<span data-ttu-id="18c74-115">Inventario di prodotti e patch</span><span class="sxs-lookup"><span data-stu-id="18c74-115">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
-   [<span data-ttu-id="18c74-116">Gestione delle origini di installazione</span><span class="sxs-lookup"><span data-stu-id="18c74-116">Managing Installation Sources</span></span>](managing-installation-sources.md)

 

 



