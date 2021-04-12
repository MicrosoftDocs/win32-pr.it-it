---
description: Active Directory è il servizio directory per Windows ed è la base di reti distribuite di Windows.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Accesso a Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233473"
---
# <a name="accessing-active-directory"></a><span data-ttu-id="070f3-103">Accesso a Active Directory</span><span class="sxs-lookup"><span data-stu-id="070f3-103">Accessing Active Directory</span></span>

<span data-ttu-id="070f3-104">Active Directory è il servizio directory per Windows ed è la base di reti distribuite di Windows.</span><span class="sxs-lookup"><span data-stu-id="070f3-104">Active Directory is the directory service for Windows and is the foundation of Windows distributed networks.</span></span> <span data-ttu-id="070f3-105">È possibile utilizzare Active Directory per individuare gli oggetti in un dominio di rete del computer, ad esempio utenti, criteri di sicurezza, stampanti, componenti distribuiti e altre risorse.</span><span class="sxs-lookup"><span data-stu-id="070f3-105">You can use Active Directory to locate objects in a computer network domain, such as users, security policies, printers, distributed components, and other resources.</span></span> <span data-ttu-id="070f3-106">Il nome Active Directory si riferisce sia al servizio directory che alla directory stessa.</span><span class="sxs-lookup"><span data-stu-id="070f3-106">The name Active Directory refers both to the directory service and the directory itself.</span></span>

> [!Note]  
> <span data-ttu-id="070f3-107">Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="070f3-107">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="070f3-108">Windows rende Active Directory accessibili tramite WMI creando un set di riferimenti a ogni classe e oggetto contenuto in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="070f3-108">Windows makes Active Directory accessible through WMI by creating a set of references to every class and object contained in Active Directory.</span></span> <span data-ttu-id="070f3-109">Accedendo al provider di servizi directory tramite WMI, è possibile creare applicazioni abilitate per WMI in grado di accedere alle numerose informazioni contenute in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="070f3-109">By accessing the Directory Services provider through WMI, you can create WMI-enabled applications that can access the wealth of information contained in Active Directory.</span></span>

<span data-ttu-id="070f3-110">Con queste interfacce è possibile:</span><span class="sxs-lookup"><span data-stu-id="070f3-110">With these interfaces, you can:</span></span>

-   <span data-ttu-id="070f3-111">Recuperare classi e istanze.</span><span class="sxs-lookup"><span data-stu-id="070f3-111">Retrieve classes and instances.</span></span>
-   <span data-ttu-id="070f3-112">Enumerare classi e istanze.</span><span class="sxs-lookup"><span data-stu-id="070f3-112">Enumerate classes and instances.</span></span>
-   <span data-ttu-id="070f3-113">Creare nuove istanze.</span><span class="sxs-lookup"><span data-stu-id="070f3-113">Create new instances.</span></span>
-   <span data-ttu-id="070f3-114">Modificare le istanze esistenti.</span><span class="sxs-lookup"><span data-stu-id="070f3-114">Modify existing instances.</span></span>
-   <span data-ttu-id="070f3-115">Elimina le istanze esistenti.</span><span class="sxs-lookup"><span data-stu-id="070f3-115">Delete existing instances.</span></span>
-   <span data-ttu-id="070f3-116">Active Directory query.</span><span class="sxs-lookup"><span data-stu-id="070f3-116">Query Active Directory.</span></span>

<span data-ttu-id="070f3-117">Gli argomenti seguenti possono risultare utili per l'utilizzo di Active Directory con WMI:</span><span class="sxs-lookup"><span data-stu-id="070f3-117">The following topics can assist you in using Active Directory with WMI:</span></span>

-   [<span data-ttu-id="070f3-118">Uso della sintassi di Active Directory appropriata</span><span class="sxs-lookup"><span data-stu-id="070f3-118">Using the Proper Active Directory Syntax</span></span>](using-the-proper-active-directory-syntax.md)
-   [<span data-ttu-id="070f3-119">Mapping di Active Directory a WMI</span><span class="sxs-lookup"><span data-stu-id="070f3-119">Mapping Active Directory to WMI</span></span>](mapping-active-directory-to-wmi.md)

 

 



