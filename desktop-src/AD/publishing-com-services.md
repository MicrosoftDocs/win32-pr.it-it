---
title: Pubblicazione di servizi COM+
description: I servizi basati su COM forniscono un proxy di applicazione sotto forma di pacchetto di Windows Installer (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Pubblicazione di servizi COM+
- Active Directory, utilizzo, pubblicazione di un servizio, servizi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044100"
---
# <a name="publishing-com-services"></a><span data-ttu-id="d23e7-105">Pubblicazione di servizi COM+</span><span class="sxs-lookup"><span data-stu-id="d23e7-105">Publishing COM+ Services</span></span>

<span data-ttu-id="d23e7-106">I servizi basati su COM forniscono un proxy di applicazione sotto forma di pacchetto di Windows Installer (MSI).</span><span class="sxs-lookup"><span data-stu-id="d23e7-106">COM-based services provide an application-proxy in the form of a Windows installer (MSI) package.</span></span> <span data-ttu-id="d23e7-107">Il file con estensione msi contiene il nome del server da utilizzare e altri elementi necessari, ad esempio proxy/stub e librerie dei tipi necessari per il marshalling.</span><span class="sxs-lookup"><span data-stu-id="d23e7-107">This .msi file contains the server name to be used and other required elements, such as proxy/stubs and type libraries required for marshalling.</span></span> <span data-ttu-id="d23e7-108">Lo snap-in Servizi componenti genera automaticamente questi proxy di applicazione per le applicazioni server COM+.</span><span class="sxs-lookup"><span data-stu-id="d23e7-108">The Component Services snap-in auto-generate these application proxies for COM+ Server applications.</span></span>

<span data-ttu-id="d23e7-109">I proxy dell'applicazione vengono pubblicati in oggetti criteri in Active Directory usando l'editor di Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d23e7-109">The application proxies are published into policy objects in Active Directory using the Group Policy Editor.</span></span> <span data-ttu-id="d23e7-110">Nell'applicazione client non è richiesto alcun intervento specifico.</span><span class="sxs-lookup"><span data-stu-id="d23e7-110">No special intervention is required in the client application.</span></span> <span data-ttu-id="d23e7-111">L'account computer/utente nel computer client deve trovarsi in un'unità organizzativa configurata per l'utilizzo dell'oggetto criterio in cui vengono pubblicati i proxy dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d23e7-111">The computer/user account on the client computer must be in an OU configured to use the policy object in which the application proxies are published.</span></span> <span data-ttu-id="d23e7-112">Il Binder COM individua automaticamente il server per mezzo della directory quando il client stabilisce un'istanza degli oggetti interessati.</span><span class="sxs-lookup"><span data-stu-id="d23e7-112">The COM binder automatically locates the server by means of the directory when the client establishes an instance of the objects concerned.</span></span>

 

 




