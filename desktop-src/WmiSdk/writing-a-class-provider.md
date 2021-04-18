---
description: Un provider di classi gestisce una classe o una serie di classi per WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Scrittura di un provider di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313154"
---
# <a name="writing-a-class-provider"></a><span data-ttu-id="83444-103">Scrittura di un provider di classi</span><span class="sxs-lookup"><span data-stu-id="83444-103">Writing a Class Provider</span></span>

<span data-ttu-id="83444-104">Un provider di classi gestisce una classe o una serie di classi per WMI.</span><span class="sxs-lookup"><span data-stu-id="83444-104">A class provider manages a class or series of classes for WMI.</span></span> <span data-ttu-id="83444-105">Un provider di classi può essere push o pull; ovvero può archiviare i propri dati o consentire a WMI di archiviare i dati nel servizio di gestione Windows.</span><span class="sxs-lookup"><span data-stu-id="83444-105">A class provider can either be push or pull; that is, it can either store its own data or allow WMI to store data for it in the Windows Management Service.</span></span> <span data-ttu-id="83444-106">Anche se un provider di classi è installato in un computer specifico, può modificare le definizioni delle classi in un'intera azienda.</span><span class="sxs-lookup"><span data-stu-id="83444-106">Although a class provider is installed on a specific machine, it can change the class definitions across an entire enterprise.</span></span> <span data-ttu-id="83444-107">Pertanto, la maggior parte degli sviluppatori spesso non crea provider di classi.</span><span class="sxs-lookup"><span data-stu-id="83444-107">Therefore, most developers do not often create class providers.</span></span>

<span data-ttu-id="83444-108">Prima di creare un provider di classi, verificare che le classi supportate siano effettivamente generate dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="83444-108">Before constructing a class provider, verify that the supported classes truly must be generated dynamically.</span></span> <span data-ttu-id="83444-109">Nella maggior parte dei casi, l'elenco delle classi è a modifica lenta e finito.</span><span class="sxs-lookup"><span data-stu-id="83444-109">In most cases, the list of classes is slow-changing and finite.</span></span> <span data-ttu-id="83444-110">In tal caso, non è necessario creare un provider di classi.</span><span class="sxs-lookup"><span data-stu-id="83444-110">If this is the case, you should not have to create a class provider.</span></span> <span data-ttu-id="83444-111">In alternativa, è possibile inserire le definizioni delle classi nel repository WMI utilizzando l'API WMI o un file MOF.</span><span class="sxs-lookup"><span data-stu-id="83444-111">Instead, you can place your class definitions in the WMI repository using the WMI API or a MOF file.</span></span>

<span data-ttu-id="83444-112">Nella procedura seguente viene descritto come implementare un provider di classi.</span><span class="sxs-lookup"><span data-stu-id="83444-112">The following procedure describes how to implement a class provider.</span></span>

<span data-ttu-id="83444-113">**Per implementare un provider di classi**</span><span class="sxs-lookup"><span data-stu-id="83444-113">**To implement a class provider**</span></span>

1.  <span data-ttu-id="83444-114">Determinare se il provider è un provider push o pull.</span><span class="sxs-lookup"><span data-stu-id="83444-114">Determine if your provider is a push or pull provider.</span></span>

    <span data-ttu-id="83444-115">Un provider di pull fornisce i dati in modo dinamico in risposta a una richiesta dell'applicazione, mentre i provider di push memorizzano i dati una volta nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="83444-115">A pull provider supplies data dynamically in response to an application request, whereas push providers store their data once in the WMI repository.</span></span> <span data-ttu-id="83444-116">Per ulteriori informazioni, vedere [determinare lo stato di push o pull](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="83444-116">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

2.  <span data-ttu-id="83444-117">Progettare e registrare il provider di classi con WMI.</span><span class="sxs-lookup"><span data-stu-id="83444-117">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="83444-118">I provider di classi si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e un'istanza di [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="83444-118">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_ClassProviderRegistration**](--classproviderregistration.md) instance.</span></span> <span data-ttu-id="83444-119">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di classi](registering-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="83444-119">For more information, see [Registering a Class Provider](registering-a-class-provider.md).</span></span>

3.  <span data-ttu-id="83444-120">Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.</span><span class="sxs-lookup"><span data-stu-id="83444-120">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="83444-121">WMI utilizza [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider.</span><span class="sxs-lookup"><span data-stu-id="83444-121">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="83444-122">Se si progetta un provider di push, **IWbemProviderInit** è l'unica interfaccia che verrà implementata.</span><span class="sxs-lookup"><span data-stu-id="83444-122">If you are designing a push provider, **IWbemProviderInit** is the only interface you will implement.</span></span> <span data-ttu-id="83444-123">Per ulteriori informazioni, vedere [inizializzazione di un provider](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="83444-123">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="83444-124">I provider di classi sono vivamente invitati a usare il modello di multithreading "both".</span><span class="sxs-lookup"><span data-stu-id="83444-124">Class providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

4.  <span data-ttu-id="83444-125">Aggiungere il codice aggiuntivo necessario per il provider.</span><span class="sxs-lookup"><span data-stu-id="83444-125">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="83444-126">Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI.</span><span class="sxs-lookup"><span data-stu-id="83444-126">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="83444-127">Per ulteriori informazioni, vedere [chiamata di un metodo](calling-a-method.md) e [gestione dei livelli di sicurezza in un provider](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="83444-127">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="83444-128">Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per il client.</span><span class="sxs-lookup"><span data-stu-id="83444-128">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="83444-129">Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="83444-129">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="83444-130">Implementare l'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per il provider.</span><span class="sxs-lookup"><span data-stu-id="83444-130">Implement the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface for your provider.</span></span>

    <span data-ttu-id="83444-131">L'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è l'interfaccia principale per un provider di classi pull.</span><span class="sxs-lookup"><span data-stu-id="83444-131">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a pull class provider.</span></span> <span data-ttu-id="83444-132">Per ulteriori informazioni, vedere [Implementing the primary interface for a class provider](implementing-the-primary-interface-for-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="83444-132">For more information, see [Implementing the Primary Interface for a Class Provider](implementing-the-primary-interface-for-a-class-provider.md).</span></span>

6.  <span data-ttu-id="83444-133">Sostituire il provider preesistente con il nuovo codice.</span><span class="sxs-lookup"><span data-stu-id="83444-133">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="83444-134">Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente per la copia.</span><span class="sxs-lookup"><span data-stu-id="83444-134">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="83444-135">Per ulteriori informazioni, vedere [aggiornamento di un provider](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="83444-135">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



