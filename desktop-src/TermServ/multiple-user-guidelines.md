---
title: Linee guida per più utenti
description: Linee guida per lo sviluppo di applicazioni per più utenti in un ambiente Servizi Desktop remoto.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298885"
---
# <a name="multiple-user-guidelines"></a><span data-ttu-id="43df9-103">Linee guida per più utenti</span><span class="sxs-lookup"><span data-stu-id="43df9-103">Multiple-user guidelines</span></span>

<span data-ttu-id="43df9-104">Nelle sezioni seguenti vengono fornite le linee guida per lo sviluppo di applicazioni per più utenti in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="43df9-104">The following sections provide guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="43df9-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="43df9-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="43df9-106">Configurazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="43df9-106">Application setup</span></span>](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="43df9-107">L'installazione di un'applicazione per un singolo utente può creare problemi in un ambiente multiutente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="43df9-107">Installing an application for a single user can create problems in a multiuser Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="43df9-108">Archiviazione di informazioni specifiche dell'utente</span><span class="sxs-lookup"><span data-stu-id="43df9-108">Storing user-specific information</span></span>](storing-user-specific-information.md)
</dt> <dd>

<span data-ttu-id="43df9-109">Le applicazioni devono archiviare le informazioni specifiche dell'utente in percorsi specifici dell'utente, separatamente da informazioni globali che si applicano a tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="43df9-109">Applications should store user-specific information in user-specific locations, separately from global information that applies to all users.</span></span>

</dd> <dt>

[<span data-ttu-id="43df9-110">Spazi dei nomi dell'oggetto kernel</span><span class="sxs-lookup"><span data-stu-id="43df9-110">Kernel object namespaces</span></span>](kernel-object-namespaces.md)
</dt> <dd>

<span data-ttu-id="43df9-111">Servizi Desktop remoto usa più spazi dei nomi per gli oggetti kernel; uno spazio dei nomi globale viene utilizzato principalmente dai servizi nelle applicazioni client/server.</span><span class="sxs-lookup"><span data-stu-id="43df9-111">Remote Desktop Services uses multiple namespaces for kernel objects; a global namespace is used primarily by services in client/server applications.</span></span>

</dd> <dt>

[<span data-ttu-id="43df9-112">Indirizzi IP e nomi di computer</span><span class="sxs-lookup"><span data-stu-id="43df9-112">IP addresses and computer names</span></span>](ip-addresses-and-computer-names.md)
</dt> <dd>

<span data-ttu-id="43df9-113">Non è opportuno presupporre che il nome del computer o l' indirizzo IP assegnato al computer sia associato a un singolo utente poiché più utenti possono accedere contemporaneamente a un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="43df9-113">It is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user because multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> </dl>

<span data-ttu-id="43df9-114">Come sempre, bloccare i file e i database durante le modifiche per evitare la perdita accidentale di dati.</span><span class="sxs-lookup"><span data-stu-id="43df9-114">As always, lock files and databases while making changes to prevent inadvertent loss of data.</span></span>

<span data-ttu-id="43df9-115">L'applicazione non deve bloccare i file dell'applicazione in fase di esecuzione che non sono file per utente.</span><span class="sxs-lookup"><span data-stu-id="43df9-115">Your application must not lock any run-time application files that are not per-user files.</span></span> <span data-ttu-id="43df9-116">I file di runtime bloccati possono impedire l'esecuzione di più istanze dell'applicazione o di processi nell'applicazione, ad esempio procedure guidate.</span><span class="sxs-lookup"><span data-stu-id="43df9-116">Locked run-time files can keep multiple instances of the application, or processes under the application such as wizards, from running.</span></span> <span data-ttu-id="43df9-117">Un modo efficace per verificare quali file sono i file dell'applicazione in fase di esecuzione consiste nel tenere traccia dei file installati dall'installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="43df9-117">A good way to test which files are run-time application files is to track which files are installed by the application setup.</span></span> <span data-ttu-id="43df9-118">I file per utente vengono raramente installati dal programma di installazione di; Pertanto, la maggior parte dei file installati dal programma di installazione sono file dell'applicazione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="43df9-118">Per-user files are rarely installed by setup; therefore, most files installed by setup are run-time application files.</span></span>

 

 




