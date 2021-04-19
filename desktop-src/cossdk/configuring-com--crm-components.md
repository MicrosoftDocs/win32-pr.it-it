---
description: I componenti di CRM possono essere installati in un'applicazione server COM+ o in un'applicazione libreria COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configurazione dei componenti di COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305227"
---
# <a name="configuring-com-crm-components"></a><span data-ttu-id="28f78-103">Configurazione dei componenti di COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="28f78-103">Configuring COM+ CRM Components</span></span>

<span data-ttu-id="28f78-104">I componenti di CRM possono essere installati in un'applicazione server COM+ o in un'applicazione libreria COM+.</span><span class="sxs-lookup"><span data-stu-id="28f78-104">CRM components can be installed into either a COM+ server application or a COM+ library application.</span></span> <span data-ttu-id="28f78-105">Tuttavia, devono essere sempre eseguiti in un'applicazione server COM+.</span><span class="sxs-lookup"><span data-stu-id="28f78-105">However, they must always run in a COM+ server application.</span></span> <span data-ttu-id="28f78-106">Se sono installate in un'applicazione libreria COM+, non sono disponibili per l'utilizzo nei processi client.</span><span class="sxs-lookup"><span data-stu-id="28f78-106">If they are installed in a COM+ library application, they are not available for use in client processes.</span></span>

<span data-ttu-id="28f78-107">Se i componenti CRM installati in un'applicazione di libreria sono disponibili per più di un'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="28f78-107">If the CRM components they are installed in a library application, they are available to more than one server application.</span></span> <span data-ttu-id="28f78-108">Se installate in un'applicazione server specifica, sono disponibili solo per tale applicazione server specifica.</span><span class="sxs-lookup"><span data-stu-id="28f78-108">If installed in a specific server application, they are available only to that specific server application.</span></span>

<span data-ttu-id="28f78-109">Per abilitare l'uso di un CRM in un'applicazione server, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="28f78-109">To enable use of a CRM in a server application, use the following steps:</span></span>

1.  <span data-ttu-id="28f78-110">In Servizi componenti, nella pagina Proprietà applicazione server, fare clic sulla scheda **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="28f78-110">From Component Services, under the server application properties page, click the **Advanced** tab.</span></span>

2.  <span data-ttu-id="28f78-111">Selezionare l'opzione **Enable Compensating Resource managers** per l'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="28f78-111">Select the **Enable compensating Resource Managers** option for that server application.</span></span> <span data-ttu-id="28f78-112">Se questa opzione non è selezionata, i tentativi di usare un CRM in questa applicazione server avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="28f78-112">If this option is not selected, attempts to use a CRM within this server application will fail.</span></span>

    > [!Note]  
    > <span data-ttu-id="28f78-113">Se installato in un'applicazione libreria, non è necessario selezionare l'opzione **Abilita gestione risorse di compensazione** per l'applicazione della libreria, ma questa opzione deve essere selezionata per l'applicazione server in cui è previsto l'esecuzione del CRM.</span><span class="sxs-lookup"><span data-stu-id="28f78-113">If installed in a library application, it is not necessary to select the **Enable compensating Resource Managers** option for that library application, but this option must be selected for the server application in which the CRM is intended to run.</span></span>

     

<span data-ttu-id="28f78-114">Si consiglia di installare i componenti del ruolo di lavoro CRM e del compensatore CRM per un CRM specifico nella stessa applicazione.</span><span class="sxs-lookup"><span data-stu-id="28f78-114">It is recommended that the CRM Worker and CRM Compensator components for a specific CRM be installed in the same application.</span></span>

<span data-ttu-id="28f78-115">Di seguito sono riportate le impostazioni consigliate per i componenti di CRM.</span><span class="sxs-lookup"><span data-stu-id="28f78-115">The recommended settings for CRM components are as follows.</span></span>



| <span data-ttu-id="28f78-116">Componente</span><span class="sxs-lookup"><span data-stu-id="28f78-116">Component</span></span>           | <span data-ttu-id="28f78-117">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="28f78-117">Settings</span></span>                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28f78-118">**Ruolo di lavoro CRM**</span><span class="sxs-lookup"><span data-stu-id="28f78-118">**CRM Worker**</span></span>      | <span data-ttu-id="28f78-119">Transaction = requiredsync = yesJIT = yesthreading Model = both (o Threading Model = Apartment)</span><span class="sxs-lookup"><span data-stu-id="28f78-119">transaction = requiredsync = yesJIT = yesthreading model = Both (or threading model = Apartment)</span></span>     |
| <span data-ttu-id="28f78-120">**Compensatore CRM**</span><span class="sxs-lookup"><span data-stu-id="28f78-120">**CRM Compensator**</span></span> | <span data-ttu-id="28f78-121">Transaction = disabledsync = disabledJIT = nothreading Model = both (o Threading Model = Apartment)</span><span class="sxs-lookup"><span data-stu-id="28f78-121">transaction = disabledsync = disabledJIT = nothreading model = Both (or threading model = Apartment)</span></span> |



 

> [!Note]  
> <span data-ttu-id="28f78-122">I componenti che utilizzano CRM devono specificare in modo esplicito un modello di threading quando vengono registrati.</span><span class="sxs-lookup"><span data-stu-id="28f78-122">Components that use the CRM must explicitly specify a threading model when they are registered.</span></span> <span data-ttu-id="28f78-123">Il valore predefinito ' Apartment thread principale ' non è supportato.</span><span class="sxs-lookup"><span data-stu-id="28f78-123">The default, 'Main Thread Apartment,' is not supported.</span></span> <span data-ttu-id="28f78-124">Gli unici due modelli di threading supportati sono Apartment e both.</span><span class="sxs-lookup"><span data-stu-id="28f78-124">The only two threading models supported are Apartment and Both.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="28f78-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28f78-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f78-126">Concetti Gestione risorse di compensazione COM+</span><span class="sxs-lookup"><span data-stu-id="28f78-126">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



