---
description: Un provider di proprietà recupera e modifica i singoli valori delle proprietà per le istanze di una determinata classe archiviata nel repository WMI.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Scrittura di un provider di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313153"
---
# <a name="writing-a-property-provider"></a><span data-ttu-id="a8fa2-103">Scrittura di un provider di proprietà</span><span class="sxs-lookup"><span data-stu-id="a8fa2-103">Writing a Property Provider</span></span>

<span data-ttu-id="a8fa2-104">Un provider di proprietà recupera e modifica i singoli valori delle proprietà per le istanze di una determinata classe archiviata nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-104">A property provider retrieves and modifies individual property values for instances of a given class that is stored in the WMI repository.</span></span>

<span data-ttu-id="a8fa2-105">Nella procedura riportata di seguito viene descritto come creare un provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-105">The following procedure describes how to create a property provider.</span></span>

<span data-ttu-id="a8fa2-106">**Per creare un provider di proprietà**</span><span class="sxs-lookup"><span data-stu-id="a8fa2-106">**To create a property provider**</span></span>

1.  <span data-ttu-id="a8fa2-107">Progettare e registrare il provider con WMI.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-107">Design and register your provider with WMI.</span></span>

    <span data-ttu-id="a8fa2-108">I provider di istanze si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e una classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fa2-108">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class.</span></span> <span data-ttu-id="a8fa2-109">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di proprietà](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a8fa2-109">For more information, see [Registering a Property Provider](registering-a-property-provider.md).</span></span>

2.  <span data-ttu-id="a8fa2-110">Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-110">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="a8fa2-111">WMI utilizza [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-111">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="a8fa2-112">Si tratta di un'attività comune a tutti i provider.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-112">This is a task common to all providers.</span></span> <span data-ttu-id="a8fa2-113">Per ulteriori informazioni, vedere [inizializzazione di un provider](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a8fa2-113">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="a8fa2-114">Per i provider di proprietà si consiglia vivamente di utilizzare il modello di multithreading "both".</span><span class="sxs-lookup"><span data-stu-id="a8fa2-114">Property providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="a8fa2-115">Implementare l'interfaccia [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) per il provider.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-115">Implement the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface for your provider.</span></span>

    <span data-ttu-id="a8fa2-116">L'interfaccia [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) è l'interfaccia principale per un provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-116">The [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface is the primary interface for a property provider.</span></span> <span data-ttu-id="a8fa2-117">I due metodi principali sono [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) e [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span><span class="sxs-lookup"><span data-stu-id="a8fa2-117">The two main methods are [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span></span> <span data-ttu-id="a8fa2-118">Per ulteriori informazioni, vedere [implementazione dell'interfaccia principale per un provider di proprietà](implementing-the-primary-interface-for-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a8fa2-118">For more information, see [Implementing the Primary Interface for a Property Provider](implementing-the-primary-interface-for-a-property-provider.md).</span></span>

4.  <span data-ttu-id="a8fa2-119">Aggiungere il codice aggiuntivo necessario per il provider.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-119">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="a8fa2-120">Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-120">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="a8fa2-121">Per ulteriori informazioni, vedere [chiamata di un metodo](calling-a-method.md) e [gestione dei livelli di sicurezza in un provider](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="a8fa2-121">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="a8fa2-122">Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per il client.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-122">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="a8fa2-123">Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="a8fa2-123">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="a8fa2-124">Sostituire il provider preesistente con il nuovo codice.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-124">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="a8fa2-125">Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente per la copia.</span><span class="sxs-lookup"><span data-stu-id="a8fa2-125">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="a8fa2-126">Per ulteriori informazioni, vedere [aggiornamento di un provider](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a8fa2-126">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



