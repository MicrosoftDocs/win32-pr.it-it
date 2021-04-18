---
description: Un provider di istanze fornisce istanze di una o più classi specificate.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Scrittura di un provider di istanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313677"
---
# <a name="writing-an-instance-provider"></a><span data-ttu-id="c4a30-103">Scrittura di un provider di istanze</span><span class="sxs-lookup"><span data-stu-id="c4a30-103">Writing an Instance Provider</span></span>

<span data-ttu-id="c4a30-104">Un provider di istanze fornisce istanze di una o più classi specificate.</span><span class="sxs-lookup"><span data-stu-id="c4a30-104">An instance provider supplies instances of one or more given classes.</span></span> <span data-ttu-id="c4a30-105">Un provider di istanze, ad esempio, può fornire informazioni riguardanti una CPU o un altro tipo di hardware.</span><span class="sxs-lookup"><span data-stu-id="c4a30-105">For example, an instance provider can supply information regarding a CPU or other type of hardware.</span></span> <span data-ttu-id="c4a30-106">Poiché gli oggetti gestiti da un provider di istanze tendono a essere modificati a intervalli regolari, tutti i provider di istanze sono considerati provider di pull. ovvero un provider che recupera dinamicamente le informazioni relative a un oggetto gestito ogni volta che WMI esegue una richiesta di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c4a30-106">Because the objects managed by an instance provider tend to change on a regular basis, all instance providers are considered pull providers; that is, a provider that dynamically retrieves information regarding a managed object whenever WMI makes a request for the information.</span></span> <span data-ttu-id="c4a30-107">Il nome deriva dal concetto che WMI estrae le informazioni dal provider per conto di una richiesta client.</span><span class="sxs-lookup"><span data-stu-id="c4a30-107">The name comes from the idea that WMI "pulls" the information from the provider on behalf of a client request.</span></span> <span data-ttu-id="c4a30-108">Grazie alla tecnologia pull, un provider di istanze può supportare il recupero, l'enumerazione, la modifica, l'eliminazione e l'elaborazione di query di un'istanza specifica.</span><span class="sxs-lookup"><span data-stu-id="c4a30-108">Using pull technology, an instance provider can support retrieval, enumeration, modification, deletion, and query processing of a specific instance.</span></span>

<span data-ttu-id="c4a30-109">I provider a prestazioni elevate possono aumentare l'efficienza di un provider di istanze o accedere a livello di codice ai dati visualizzati in Monitor di sistema.</span><span class="sxs-lookup"><span data-stu-id="c4a30-109">High-performance providers can increase the efficiency of an instance provider or programmatically access the data that appears in System Monitor.</span></span> <span data-ttu-id="c4a30-110">Per ulteriori informazioni, vedere [creazione di un provider di istanze in un provider di High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c4a30-110">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

<span data-ttu-id="c4a30-111">Nella procedura riportata di seguito viene descritto come scrivere un provider di istanze.</span><span class="sxs-lookup"><span data-stu-id="c4a30-111">The following procedure describes how to write an instance provider.</span></span>

<span data-ttu-id="c4a30-112">**Per scrivere un provider di istanze**</span><span class="sxs-lookup"><span data-stu-id="c4a30-112">**To write an instance provider**</span></span>

1.  <span data-ttu-id="c4a30-113">[Registrare il provider con WMI](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c4a30-113">[Register your provider with WMI](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="c4a30-114">I provider di istanze si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e una classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a30-114">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

2.  <span data-ttu-id="c4a30-115">[Inizializzare il provider](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c4a30-115">[Initialize your provider](initializing-a-provider.md).</span></span>

    <span data-ttu-id="c4a30-116">WMI utilizza [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider.</span><span class="sxs-lookup"><span data-stu-id="c4a30-116">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="c4a30-117">Si tratta di un'attività comune a tutti i provider.</span><span class="sxs-lookup"><span data-stu-id="c4a30-117">This is a task common to all providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="c4a30-118">I provider di istanze sono vivamente invitati a usare il modello di multithreading "both".</span><span class="sxs-lookup"><span data-stu-id="c4a30-118">Instance providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="c4a30-119">[Implementare l'interfaccia IWbemServices per il provider](implementing-the-primary-interface-for-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c4a30-119">[Implement the IWbemServices interface for your provider](implementing-the-primary-interface-for-an-instance-provider.md).</span></span>

    <span data-ttu-id="c4a30-120">L'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è l'interfaccia principale per un provider di istanze.</span><span class="sxs-lookup"><span data-stu-id="c4a30-120">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for an instance provider.</span></span>

4.  <span data-ttu-id="c4a30-121">Aggiungere il codice aggiuntivo necessario per il provider.</span><span class="sxs-lookup"><span data-stu-id="c4a30-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="c4a30-122">Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI.</span><span class="sxs-lookup"><span data-stu-id="c4a30-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="c4a30-123">Per ulteriori informazioni, vedere [effettuare chiamate a WMI](making-calls-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c4a30-123">For more information, see [Making Calls to WMI](making-calls-to-wmi.md).</span></span>

    <span data-ttu-id="c4a30-124">Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per il client.</span><span class="sxs-lookup"><span data-stu-id="c4a30-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="c4a30-125">Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="c4a30-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="c4a30-126">Se necessario, [implementare l'interfaccia a prestazioni elevate](improving-the-efficiency-of-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c4a30-126">If necessary, [implement the high-performance interface](improving-the-efficiency-of-an-instance-provider.md).</span></span>

    <span data-ttu-id="c4a30-127">L'interfaccia a prestazioni elevate aumenta la velocità con cui il provider può rispondere alle richieste provenienti da WMI.</span><span class="sxs-lookup"><span data-stu-id="c4a30-127">The high-performance interface increases the speed at which the provider can react to requests from WMI.</span></span>

6.  <span data-ttu-id="c4a30-128">Se necessario, [implementare il supporto per gli aggiornamenti parziali dell'istanza](supporting-partial-instance-operations.md).</span><span class="sxs-lookup"><span data-stu-id="c4a30-128">If necessary, [implement support for partial-instance updates](supporting-partial-instance-operations.md).</span></span>

    <span data-ttu-id="c4a30-129">Come suggerisce il nome, un aggiornamento parziale dell'istanza è una tecnica utilizzata per aggiornare solo parte di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="c4a30-129">As the name implies, a partial-instance update is a technique use to update only part of an instance.</span></span> <span data-ttu-id="c4a30-130">Per ulteriori informazioni sulla chiamata di un'istanza parziale da un client, vedere [aggiornamento di una parte di un'istanza](updating-part-of-an-instance.md) e [recupero di parte di un'istanza di WMI](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="c4a30-130">For more information about calling a partial instance from a client, see [Updating Part of an Instance](updating-part-of-an-instance.md) and [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

7.  <span data-ttu-id="c4a30-131">Sostituire il provider preesistente con il nuovo codice.</span><span class="sxs-lookup"><span data-stu-id="c4a30-131">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="c4a30-132">Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente per la copia.</span><span class="sxs-lookup"><span data-stu-id="c4a30-132">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="c4a30-133">Per ulteriori informazioni, vedere [aggiornamento di un provider](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c4a30-133">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



