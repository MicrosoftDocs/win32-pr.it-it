---
description: Registrazione e annullamento della registrazione delle chiavi
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrazione e annullamento della registrazione delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315443"
---
# <a name="registering-and-deregistering-keys"></a><span data-ttu-id="e3e31-103">Registrazione e annullamento della registrazione delle chiavi</span><span class="sxs-lookup"><span data-stu-id="e3e31-103">Registering and Deregistering Keys</span></span>

## <a name="registering-keys"></a><span data-ttu-id="e3e31-104">Registrazione di chiavi</span><span class="sxs-lookup"><span data-stu-id="e3e31-104">Registering Keys</span></span>

<span data-ttu-id="e3e31-105">Un nodo può registrare le chiavi con [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) in qualsiasi momento mentre si trovino in **DRT \_ Active**, **DRT \_ alone** e **DRT senza stati di \_ \_ rete** .</span><span class="sxs-lookup"><span data-stu-id="e3e31-105">A node can register keys with [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) at anytime while in the **DRT\_ACTIVE**, **DRT\_ALONE**, and **DRT\_NO\_NETWORK** states.</span></span> <span data-ttu-id="e3e31-106">Le chiavi registrate **solo \_ in DRT** e **DRT nessun stato di \_ \_ rete** possono essere riconosciute solo da altri DRTS dopo che il nodo locale è passato a **DRT \_ attivo**.</span><span class="sxs-lookup"><span data-stu-id="e3e31-106">Keys registered in **DRT\_ALONE** and **DRT\_NO\_NETWORK** states can only be recognized by other DRTs after the local node has transitioned to **DRT\_ACTIVE**.</span></span>

<span data-ttu-id="e3e31-107">Non è possibile registrare chiavi identiche all'interno della stessa istanza di DRT quando si usa [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span><span class="sxs-lookup"><span data-stu-id="e3e31-107">Identical keys cannot be registered within the same DRT instance when using [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span></span> <span data-ttu-id="e3e31-108">Se viene tentata la registrazione di chiavi identiche, la registrazione della seconda chiave avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e3e31-108">If the registration of identical keys is attempted, the registration of the second key will fail.</span></span> <span data-ttu-id="e3e31-109">Anche l'uso di chiavi identiche deve essere evitato tra istanze DRT diverse.</span><span class="sxs-lookup"><span data-stu-id="e3e31-109">The use of identical keys should also be avoided between different DRT instances.</span></span> <span data-ttu-id="e3e31-110">Esegue una ricerca in base alla designazione di chiave univoca. questa condivisione di chiavi identica può restituire una qualsiasi delle chiavi, indipendentemente dai dati associati alla chiave.</span><span class="sxs-lookup"><span data-stu-id="e3e31-110">Searches against the unique key designation these identical keys share could return any one of the keys, regardless of what data is associated to the key.</span></span>

> [!Note]  
> <span data-ttu-id="e3e31-111">Se è necessario un comportamento diverso per l'implementazione, è possibile creare un provider di sicurezza al posto di [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) .</span><span class="sxs-lookup"><span data-stu-id="e3e31-111">If different behavior is required for implementation, a security provider can be created in place of [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) to accommodate.</span></span>

 

## <a name="deregistering-keys"></a><span data-ttu-id="e3e31-112">Annullamento della registrazione delle chiavi</span><span class="sxs-lookup"><span data-stu-id="e3e31-112">Deregistering Keys</span></span>

<span data-ttu-id="e3e31-113">Un nodo può annullare la registrazione di una chiave in qualsiasi momento dopo che è stata registrata.</span><span class="sxs-lookup"><span data-stu-id="e3e31-113">A node can deregister a key anytime after it has been registered.</span></span> <span data-ttu-id="e3e31-114">Tuttavia, solo l'applicazione che ha registrato la chiave può annullarne la registrazione.</span><span class="sxs-lookup"><span data-stu-id="e3e31-114">However, only the application that registered the key can deregister it.</span></span> <span data-ttu-id="e3e31-115">Un'applicazione può annullare la registrazione di una chiave dal nodo locale usando la funzione [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) .</span><span class="sxs-lookup"><span data-stu-id="e3e31-115">An application can deregister a key from the local node using the [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) function.</span></span> <span data-ttu-id="e3e31-116">Al termine, la funzione attiva un evento di **\_ \_ \_ \_ modifica della chiave LEAFSET di un evento DRT** ; informa l'applicazione e gli altri nodi che partecipano alla rete DRT.</span><span class="sxs-lookup"><span data-stu-id="e3e31-116">Upon completion the function triggers a **DRT\_EVENT\_LEAFSET\_KEY\_CHANGE** event; informing the application as well as other nodes participating in the DRT mesh.</span></span>

<span data-ttu-id="e3e31-117">Durante lo stato **di \_ errore DRT** , la chiamata obbligatoria di [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) comporterà l'annullamento della registrazione di tutte le chiavi da parte dell'infrastruttura DRT.</span><span class="sxs-lookup"><span data-stu-id="e3e31-117">While in the **DRT\_FAULTED** state, the required call of [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) will result in the DRT infrastructure deregistering all keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3e31-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3e31-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3e31-119">Ricerca in una tabella di routing distribuita</span><span class="sxs-lookup"><span data-stu-id="e3e31-119">Searching a Distributed Routing Table</span></span>](searching-a-distributed-routing-table.md)
</dt> <dt>

[<span data-ttu-id="e3e31-120">Informazioni sulle tabelle di routing distribuite</span><span class="sxs-lookup"><span data-stu-id="e3e31-120">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)
</dt> <dt>

[<span data-ttu-id="e3e31-121">Riferimento API Tabella routing distribuito</span><span class="sxs-lookup"><span data-stu-id="e3e31-121">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



