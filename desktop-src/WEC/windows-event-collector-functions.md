---
title: Funzioni dell'agente di raccolta eventi di Windows
description: Nell'elenco seguente vengono descritte brevemente le funzioni utilizzate nell'agente di raccolta eventi di Windows.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328300"
---
# <a name="windows-event-collector-functions"></a><span data-ttu-id="06b34-103">Funzioni dell'agente di raccolta eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="06b34-103">Windows Event Collector Functions</span></span>

<span data-ttu-id="06b34-104">Nell'elenco seguente vengono descritte brevemente le funzioni utilizzate nell'agente di raccolta eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="06b34-104">The following list briefly describes the functions that are used in Windows Event Collector.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="06b34-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="06b34-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="06b34-106">**EcClose**</span><span class="sxs-lookup"><span data-stu-id="06b34-106">**EcClose**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

<span data-ttu-id="06b34-107">Chiude un handle ricevuto da altre funzioni dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="06b34-107">Closes a handle received from other Event Collector functions.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-108">**EcDeleteSubscription**</span><span class="sxs-lookup"><span data-stu-id="06b34-108">**EcDeleteSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

<span data-ttu-id="06b34-109">Elimina una sottoscrizione esistente.</span><span class="sxs-lookup"><span data-stu-id="06b34-109">Deletes an existing subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-110">**EcEnumNextSubscription**</span><span class="sxs-lookup"><span data-stu-id="06b34-110">**EcEnumNextSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

<span data-ttu-id="06b34-111">Continua l'enumerazione delle sottoscrizioni registrate nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="06b34-111">Continues the enumeration of the subscriptions registered on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-112">**EcGetObjectArrayProperty**</span><span class="sxs-lookup"><span data-stu-id="06b34-112">**EcGetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="06b34-113">Recupera i valori delle proprietà per le origini eventi di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="06b34-113">Retrieves property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-114">**EcGetObjectArraySize**</span><span class="sxs-lookup"><span data-stu-id="06b34-114">**EcGetObjectArraySize**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

<span data-ttu-id="06b34-115">Recupera il numero di indici della matrice di valori di proprietà per le origini eventi di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="06b34-115">Retrieves the number of indexes of the array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-116">**EcGetSubscriptionProperty**</span><span class="sxs-lookup"><span data-stu-id="06b34-116">**EcGetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="06b34-117">Recupera un valore di proprietà da un oggetto sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="06b34-117">Retrieves a property value from a subscription object.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-118">**EcGetSubscriptionRunTimeStatus**</span><span class="sxs-lookup"><span data-stu-id="06b34-118">**EcGetSubscriptionRunTimeStatus**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

<span data-ttu-id="06b34-119">Recupera le informazioni sullo stato della fase di esecuzione per un'origine evento di una sottoscrizione o la sottoscrizione stessa.</span><span class="sxs-lookup"><span data-stu-id="06b34-119">Retrieves the run time status information for an event source of a subscription or the subscription itself.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-120">**EcInsertObjectArrayElement**</span><span class="sxs-lookup"><span data-stu-id="06b34-120">**EcInsertObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

<span data-ttu-id="06b34-121">Inserisce un oggetto vuoto in una matrice di valori di proprietà per le origini eventi di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="06b34-121">Inserts an empty object into an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-122">**EcOpenSubscriptionEnum**</span><span class="sxs-lookup"><span data-stu-id="06b34-122">**EcOpenSubscriptionEnum**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

<span data-ttu-id="06b34-123">Crea un enumeratore di sottoscrizioni per enumerare tutte le sottoscrizioni registrate nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="06b34-123">Creates a subscription enumerator to enumerate all registered subscriptions on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-124">**EcOpenSubscription**</span><span class="sxs-lookup"><span data-stu-id="06b34-124">**EcOpenSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

<span data-ttu-id="06b34-125">Apre una sottoscrizione esistente o crea una nuova sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="06b34-125">Opens an existing subscription or creates a new subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-126">**EcSaveSubscription**</span><span class="sxs-lookup"><span data-stu-id="06b34-126">**EcSaveSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

<span data-ttu-id="06b34-127">Salva le informazioni di configurazione della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="06b34-127">Saves subscription configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-128">**EcSetObjectArrayProperty**</span><span class="sxs-lookup"><span data-stu-id="06b34-128">**EcSetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="06b34-129">Imposta un valore della proprietà in una matrice di valori di proprietà per le origini eventi di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="06b34-129">Sets a property value in an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-130">**EcSetSubscriptionProperty**</span><span class="sxs-lookup"><span data-stu-id="06b34-130">**EcSetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="06b34-131">Imposta nuovi valori o aggiorna i valori esistenti di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="06b34-131">Sets new values or updates existing values of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-132">**EcRemoveObjectArrayElement**</span><span class="sxs-lookup"><span data-stu-id="06b34-132">**EcRemoveObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

<span data-ttu-id="06b34-133">Rimuove un elemento da una matrice di oggetti che contengono valori di proprietà per le origini eventi di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="06b34-133">Removes an element from an array of objects that contain property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="06b34-134">**EcRetrySubscription**</span><span class="sxs-lookup"><span data-stu-id="06b34-134">**EcRetrySubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

<span data-ttu-id="06b34-135">Tentativi di connessione all'origine evento di una sottoscrizione non connessa.</span><span class="sxs-lookup"><span data-stu-id="06b34-135">Retries connecting to the event source of a subscription that is not connected.</span></span>

</dd> </dl>

 

 




