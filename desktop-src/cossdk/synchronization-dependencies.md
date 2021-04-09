---
description: I valori di sincronizzazione possono essere determinati o vincolati automaticamente dalla configurazione di altre proprietà, ad esempio i requisiti transazionali e l'attivazione JIT (just-in-Time).
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Dipendenze di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877613"
---
# <a name="synchronization-dependencies"></a><span data-ttu-id="5355c-103">Dipendenze di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="5355c-103">Synchronization Dependencies</span></span>

<span data-ttu-id="5355c-104">I valori di sincronizzazione possono essere determinati o vincolati automaticamente dalla configurazione di altre proprietà, ad esempio i requisiti transazionali e l'attivazione JIT (just-in-Time).</span><span class="sxs-lookup"><span data-stu-id="5355c-104">Synchronization values can be automatically determined or constrained by the configuration of other properties, such as transactional requirements and just-in-time (JIT) activation.</span></span> <span data-ttu-id="5355c-105">COM+, ad esempio, impone la sincronizzazione sia per i componenti transazionali che per quelli attivati da JIT.</span><span class="sxs-lookup"><span data-stu-id="5355c-105">For example, COM+ enforces synchronization both for transactional and for JIT-activated components.</span></span>

<span data-ttu-id="5355c-106">Queste dipendenze sono dovute al fatto che i componenti che sono attivati tramite JIT o che partecipano alle transazioni devono avere un comportamento di isolamento e concorrenza appropriato.</span><span class="sxs-lookup"><span data-stu-id="5355c-106">These dependencies exist because components that are JIT-activated or participating in transactions must have proper isolation and concurrency behavior.</span></span> <span data-ttu-id="5355c-107">Per questo motivo, COM+ richiede che l'accesso a questi componenti venga serializzato tramite l'applicazione della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5355c-107">Therefore, COM+ requires that access to these components be serialized by enforcing synchronization.</span></span> <span data-ttu-id="5355c-108">Per informazioni dettagliate su queste dipendenze, vedere [attivazione JIT (just-in-Time](com--just-in-time-activation.md)) di com+.</span><span class="sxs-lookup"><span data-stu-id="5355c-108">(For details on these dependencies, see [COM+ Just-in-Time Activation](com--just-in-time-activation.md).)</span></span>

<span data-ttu-id="5355c-109">Nelle tabelle seguenti sono illustrate le caratteristiche dei valori degli attributi di sincronizzazione COM+.</span><span class="sxs-lookup"><span data-stu-id="5355c-109">The following tables show the characteristics of the COM+ synchronization attribute values.</span></span>

### <a name="transactional-requirement"></a><span data-ttu-id="5355c-110">Requisito transazionale</span><span class="sxs-lookup"><span data-stu-id="5355c-110">Transactional requirement</span></span>



| <span data-ttu-id="5355c-111">Quando le transazioni sono impostate su</span><span class="sxs-lookup"><span data-stu-id="5355c-111">When transactions are set to</span></span> | <span data-ttu-id="5355c-112">La sincronizzazione può essere impostata su</span><span class="sxs-lookup"><span data-stu-id="5355c-112">Synchronization can be set to</span></span>                    |
|------------------------------|--------------------------------------------------|
| <span data-ttu-id="5355c-113">Disabled</span><span class="sxs-lookup"><span data-stu-id="5355c-113">Disabled</span></span><br/>          | <span data-ttu-id="5355c-114">Qualsiasi elemento, a seconda dell'attivazione JIT</span><span class="sxs-lookup"><span data-stu-id="5355c-114">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="5355c-115">Non supportato</span><span class="sxs-lookup"><span data-stu-id="5355c-115">Not Supported</span></span><br/>     | <span data-ttu-id="5355c-116">Qualsiasi elemento, a seconda dell'attivazione JIT</span><span class="sxs-lookup"><span data-stu-id="5355c-116">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="5355c-117">Supportato</span><span class="sxs-lookup"><span data-stu-id="5355c-117">Supported</span></span><br/>         | <span data-ttu-id="5355c-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="5355c-118">Required</span></span><br/>                              |
| <span data-ttu-id="5355c-119">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="5355c-119">Required</span></span><br/>          | <span data-ttu-id="5355c-120">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="5355c-120">Required</span></span><br/>                              |
| <span data-ttu-id="5355c-121">RequiresNew</span><span class="sxs-lookup"><span data-stu-id="5355c-121">Requires New</span></span><br/>      | <span data-ttu-id="5355c-122">Obbligatorio o richiede nuovo</span><span class="sxs-lookup"><span data-stu-id="5355c-122">Required or Requires New</span></span><br/>              |



 

### <a name="jit-activation"></a><span data-ttu-id="5355c-123">Attivazione JIT</span><span class="sxs-lookup"><span data-stu-id="5355c-123">JIT Activation</span></span>



| <span data-ttu-id="5355c-124">Quando l'attivazione JIT è impostata su</span><span class="sxs-lookup"><span data-stu-id="5355c-124">When JIT Activation is set to</span></span> | <span data-ttu-id="5355c-125">La sincronizzazione può essere impostata su</span><span class="sxs-lookup"><span data-stu-id="5355c-125">Synchronization can be set to</span></span>       |
|-------------------------------|-------------------------------------|
| <span data-ttu-id="5355c-126">Abilitato</span><span class="sxs-lookup"><span data-stu-id="5355c-126">Enabled</span></span><br/>            | <span data-ttu-id="5355c-127">Obbligatorio o richiede nuovo</span><span class="sxs-lookup"><span data-stu-id="5355c-127">Required or Requires New</span></span><br/> |
| <span data-ttu-id="5355c-128">Disabled</span><span class="sxs-lookup"><span data-stu-id="5355c-128">Disabled</span></span><br/>           | <span data-ttu-id="5355c-129">Nulla</span><span class="sxs-lookup"><span data-stu-id="5355c-129">Anything</span></span><br/>                 |



 

<span data-ttu-id="5355c-130">Per informazioni più dettagliate sul comportamento delle transazioni, dell'attivazione JIT e degli attributi di sincronizzazione, vedere [Configuring Transactions](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="5355c-130">For more detail about how transaction, JIT Activation, and Synchronization attributes behave together, see [Configuring Transactions](configuring-transactions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5355c-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5355c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5355c-132">Impostazione dell'attributo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="5355c-132">Setting the Synchronization Attribute</span></span>](setting-the-synchronization-attribute.md)
</dt> <dt>

[<span data-ttu-id="5355c-133">Valori degli attributi di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="5355c-133">Synchronization Attribute Values</span></span>](synchronization-attribute-values.md)
</dt> </dl>

 

 




