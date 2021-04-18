---
description: La resilienza è la capacità di un'applicazione di eseguire il ripristino normalmente da situazioni in cui manca un componente essenziale oppure è stato sostituito da una versione incompatibile.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resilienza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316743"
---
# <a name="resiliency"></a><span data-ttu-id="df7ee-103">Resilienza</span><span class="sxs-lookup"><span data-stu-id="df7ee-103">Resiliency</span></span>

<span data-ttu-id="df7ee-104">La resilienza è la capacità di un'applicazione di eseguire il ripristino normalmente da situazioni in cui manca un componente essenziale oppure è stato sostituito da una versione incompatibile.</span><span class="sxs-lookup"><span data-stu-id="df7ee-104">Resiliency is the ability of an application to recover gracefully from situations in which a vital component is missing, or has been replaced by an incompatible version.</span></span> <span data-ttu-id="df7ee-105">Con la creazione di un pacchetto di installazione e l'utilizzo delle [funzioni del programma di installazione](installer-functions.md), gli sviluppatori possono utilizzare il Windows Installer per produrre applicazioni resilienti in grado di eseguire il ripristino da tali situazioni.</span><span class="sxs-lookup"><span data-stu-id="df7ee-105">By authoring an installation package and using the [Installer Functions](installer-functions.md), developers can use the Windows Installer to produce resilient applications capable of recovering from such situations.</span></span>

-   <span data-ttu-id="df7ee-106">Usare l'elenco di origine del programma di installazione per aumentare la resilienza delle applicazioni che si basano sulle risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="df7ee-106">Use the installer's source list to increase the resiliency of applications that rely on network resources.</span></span> <span data-ttu-id="df7ee-107">Per altre informazioni, vedere [resilienza dell'origine](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="df7ee-107">For more information, see [Source Resiliency](source-resiliency.md).</span></span>
-   <span data-ttu-id="df7ee-108">Usare l'API del programma di installazione per verificare se è installata una funzionalità vitale, un componente, un file o una versione del file.</span><span class="sxs-lookup"><span data-stu-id="df7ee-108">Use the installer's API to check whether a vital feature, component, file, or file version is installed.</span></span>
-   <span data-ttu-id="df7ee-109">Usare l'API del programma di installazione per controllare il percorso di un componente in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="df7ee-109">Use the installer's API to check the path to a component at run time.</span></span> <span data-ttu-id="df7ee-110">In questo modo si riduce la dipendenza dell'applicazione da percorsi di file statici, che in genere differiscono tra i computer.</span><span class="sxs-lookup"><span data-stu-id="df7ee-110">This reduces your application's dependency on static file paths, which commonly differ between computers.</span></span>
-   <span data-ttu-id="df7ee-111">Utilizzare il programma di installazione per reinstallare i collegamenti danneggiati, le voci del registro di sistema e altri componenti senza dover eseguire di nuovo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="df7ee-111">Use the installer to reinstall damaged shortcuts, registry entries, and other components without having to rerun setup.</span></span>
-   <span data-ttu-id="df7ee-112">Aumentare la resilienza dell'installazione del prodotto lasciando abilitata la funzionalità di rollback del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="df7ee-112">Increase the resiliency of your product's installation by leaving the rollback capability of the installer enabled.</span></span> <span data-ttu-id="df7ee-113">Per ulteriori informazioni, vedere [rollback Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="df7ee-113">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



