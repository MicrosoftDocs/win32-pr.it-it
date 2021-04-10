---
description: Il pool di applicazioni COM+ consente la scalabilità dei processi a thread singolo, analogamente al modo in cui il pool di thread consente la scalabilità degli oggetti a thread singolo.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Concetti relativi al pool di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877518"
---
# <a name="com-application-pooling-concepts"></a><span data-ttu-id="0defb-103">Concetti relativi al pool di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="0defb-103">COM+ Application Pooling Concepts</span></span>

<span data-ttu-id="0defb-104">Il pool di applicazioni COM+ consente la scalabilità dei processi a thread singolo, analogamente al modo in cui il pool di thread consente la scalabilità degli oggetti a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="0defb-104">COM+ application pooling allows single-threaded processes to scale, similar to the way that thread pooling allows single-threaded objects to scale.</span></span> <span data-ttu-id="0defb-105">Il pool di applicazioni consente inoltre di risolvere gli errori nei singoli processi, fornendo altri processi in esecuzione in grado di gestire le attivazioni.</span><span class="sxs-lookup"><span data-stu-id="0defb-105">Application pooling can also help recover from failures in single processes by providing other running processes able to handle activations.</span></span>

> [!Note]  
> <span data-ttu-id="0defb-106">Le applicazioni di libreria hanno le proprietà di riciclo e pool del processo host.</span><span class="sxs-lookup"><span data-stu-id="0defb-106">Library applications have the recycling and pooling properties of their host process.</span></span>

 

<span data-ttu-id="0defb-107">Tutti i metodi dell'interfaccia [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) supportano il pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0defb-107">All methods of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface support application pooling.</span></span>

<span data-ttu-id="0defb-108">Il pool di applicazioni COM+ è configurabile per applicazione tramite la proprietà ConcurrentApps dell'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) nella raccolta di [**applicazioni**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="0defb-108">COM+ application pooling is configurable per application by using the ConcurrentApps property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="0defb-109">ConcurrentApps è un valore intero che specifica il numero massimo di processi Dllhost simultanei che devono essere avviati per attivare il servizio per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0defb-109">ConcurrentApps is an integer value that specifies the maximum number of simultaneous Dllhost processes that should be started to service activations for an application.</span></span> <span data-ttu-id="0defb-110">Questa proprietà può essere impostata utilizzando lo strumento di amministrazione Servizi componenti o a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="0defb-110">This property can be set by using the Component Services administration tool or programmatically.</span></span>

<span data-ttu-id="0defb-111">Se la proprietà ConcurrentApps è impostata su 1, ovvero sul valore predefinito, il servizio pool di applicazioni COM+ è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0defb-111">If the ConcurrentApps property is set to 1, which is the default value, the COM+ Application Pooling service is disabled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0defb-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0defb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0defb-113">Attività del pool di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="0defb-113">COM+ Application Pooling Tasks</span></span>](com--application-pooling-tasks.md)
</dt> <dt>

[<span data-ttu-id="0defb-114">Concetti relativi al riciclo delle applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="0defb-114">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



