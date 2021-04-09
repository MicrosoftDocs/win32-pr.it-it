---
description: Decisioni di progettazione principali dei controlli padre
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Decisioni di progettazione principali dei controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058248"
---
# <a name="parental-controls-key-design-decisions"></a><span data-ttu-id="113de-103">Decisioni di progettazione principali dei controlli padre</span><span class="sxs-lookup"><span data-stu-id="113de-103">Parental Controls Key Design Decisions</span></span>

<span data-ttu-id="113de-104">Le principali decisioni di progettazione per lo sviluppo di controlli padre di Windows Vista sono:</span><span class="sxs-lookup"><span data-stu-id="113de-104">Major design decisions in the development of Windows Vista Parental Controls are:</span></span>

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a><span data-ttu-id="113de-105">Dipendenza essenziale dalla funzionalità controllo dell'account utente di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="113de-105">Essential Dependency on Windows Vista User Account Control (UAC) Feature</span></span>

<span data-ttu-id="113de-106">Una decisione chiave per i controlli padre di Windows Vista consiste nel basarsi sulla nuova funzionalità di controllo dell'account utente per implementare le identità degli account con diritti ridotti, specialmente necessaria per le restrizioni offline sugli utenti controllati.</span><span class="sxs-lookup"><span data-stu-id="113de-106">A key decision for Windows Vista Parental Controls is to rely on the new User Account Control (UAC) feature to implement the reduced rights account identities especially needed for offline restrictions on controlled users.</span></span> <span data-ttu-id="113de-107">Per ulteriori informazioni su UAC, vedere [la storia per sviluppatori di Windows Vista e Windows Server 2008: requisiti per lo sviluppo di applicazioni Windows Vista per il controllo dell'account utente (UAC)](/previous-versions/aa905330(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="113de-107">For more information about UAC, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)).</span></span> <span data-ttu-id="113de-108">In breve, ogni account con diritti di amministratore dispone di privilegi sufficienti per eseguire il ruolo padre o tutore della visualizzazione dei dati di log e dell'impostazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="113de-108">In summary, every account with administrator rights effectively has privileges to perform the parent or guardian role of viewing log data and setting policies.</span></span> <span data-ttu-id="113de-109">I controlli padre possono essere impostati solo su utenti con diritti standard (in precedenza denominati account utente con privilegi minimi o LUAs), perché solo non possono modificare i registri e le impostazioni con elenchi di controllo di accesso (ACL) configurati solo per la scrittura da parte degli amministratori.</span><span class="sxs-lookup"><span data-stu-id="113de-109">Parental controls may only be set on standard-rights users (formerly called Least-privileged User Accounts, or LUAs), as only they cannot alter logs and settings with Access Control Lists (ACLs) configured only for administrators to write.</span></span> <span data-ttu-id="113de-110">In altre parole:</span><span class="sxs-lookup"><span data-stu-id="113de-110">In other words:</span></span>

-   <span data-ttu-id="113de-111">Un'identità padre o tutore è implicitamente uguale a un account con diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="113de-111">A parent or guardian identity implicitly equals an account that has rights of an administrator.</span></span>
-   <span data-ttu-id="113de-112">Gli utenti controllati dal padre devono essere utenti standard.</span><span class="sxs-lookup"><span data-stu-id="113de-112">Parentally controlled users must be standard users.</span></span>

## <a name="nearly-all-settings-are-available-by-apis"></a><span data-ttu-id="113de-113">Quasi tutte le impostazioni sono disponibili dalle API</span><span class="sxs-lookup"><span data-stu-id="113de-113">Nearly All Settings Are Available by APIs</span></span>

<span data-ttu-id="113de-114">Ad eccezione di elementi come le definizioni di sistema di classificazione, le impostazioni disponibili per la manipolazione dall'interfaccia utente dei controlli padre possono essere modificate anche dalle API esposte.</span><span class="sxs-lookup"><span data-stu-id="113de-114">With the exception of items such as ratings system definitions, settings available for manipulation by the Parental Controls User Interface may also be modified by exposed APIs.</span></span> <span data-ttu-id="113de-115">È necessario che i programmi implementino l'elevazione dei diritti amministrativi per modificare le impostazioni, come indicato in precedenza per UAC.</span><span class="sxs-lookup"><span data-stu-id="113de-115">It is necessary for programs to implement elevation to administrative rights in order to alter settings, as noted above for UAC.</span></span>

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a><span data-ttu-id="113de-116">Windows Vista Parental Controls è una tecnologia di solo consumo</span><span class="sxs-lookup"><span data-stu-id="113de-116">Windows Vista Parental Controls Is a Consumer-only Technology</span></span>

<span data-ttu-id="113de-117">I controlli padre di Windows Vista non sono destinati all'utilizzo con account di dominio.</span><span class="sxs-lookup"><span data-stu-id="113de-117">Windows Vista Parental Controls are not intended to be used with domain accounts.</span></span> <span data-ttu-id="113de-118">Come tecnologia consumer, i controlli padre non vengono distribuiti negli SKU aziendali di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="113de-118">As a consumer technology, Parental Controls is not deployed in business SKUs of Windows Vista.</span></span> <span data-ttu-id="113de-119">Se un computer è aggiunto a un dominio, i collegamenti dell'interfaccia utente per la sicurezza della famiglia verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="113de-119">If a computer is joined to a domain, the Family Safety user interface links will be suppressed.</span></span>

<span data-ttu-id="113de-120">Verrà fornito un meccanismo per esporre la funzionalità per il case aggiunto al dominio, ma solo gli account utente non di dominio possono essere configurati con i controlli padre.</span><span class="sxs-lookup"><span data-stu-id="113de-120">A mechanism will be provided to expose the functionality for the domain-joined case, but only non-domain user accounts may be configured with Parental Controls.</span></span>

 

 
