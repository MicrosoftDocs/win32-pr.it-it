---
description: Un provider di consumer di eventi è un componente dell'architettura del consumer permanente che determina il consumer di eventi permanente che gestisce un determinato evento.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Scrittura di un provider di consumer di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313676"
---
# <a name="writing-an-event-consumer-provider"></a><span data-ttu-id="15018-103">Scrittura di un provider di consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="15018-103">Writing an Event Consumer Provider</span></span>

<span data-ttu-id="15018-104">Un provider di consumer di eventi è un componente dell'architettura del consumer permanente che determina il consumer di eventi permanente che gestisce un determinato evento.</span><span class="sxs-lookup"><span data-stu-id="15018-104">An event consumer provider is a component of the permanent consumer architecture that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="15018-105">È necessario creare un provider di consumer di eventi insieme ai consumer di eventi permanenti per indirizzare correttamente gli eventi da WMI.</span><span class="sxs-lookup"><span data-stu-id="15018-105">You should create an event consumer provider along with your permanent event consumers to route events properly from WMI.</span></span>

<span data-ttu-id="15018-106">Un provider di consumer di eventi collega un provider di eventi a un elenco di classi consumer.</span><span class="sxs-lookup"><span data-stu-id="15018-106">An event consumer provider links an event provider with a list of consumer classes.</span></span> <span data-ttu-id="15018-107">Le istanze di queste classi consumer ricevono quindi gli eventi da tale provider.</span><span class="sxs-lookup"><span data-stu-id="15018-107">Instances of these consumer classes then receive events from that provider.</span></span> <span data-ttu-id="15018-108">WMI identifica il provider di consumer a cui vengono recapitati gli eventi, in base all'istanza di [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , che associa l'istanza [**\_ \_ Win32Provider**](--win32provider.md) del provider consumer a una classe consumer logica.</span><span class="sxs-lookup"><span data-stu-id="15018-108">WMI identifies which consumer provider the events are delivered to, based on the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) instance, which associates the consumer provider [**\_\_Win32Provider**](--win32provider.md) instance with a logical consumer class.</span></span> <span data-ttu-id="15018-109">Gli utenti creano istanze della classe consumer come parte di una sottoscrizione permanente.</span><span class="sxs-lookup"><span data-stu-id="15018-109">Users create instances of the consumer class as part of a permanent subscription.</span></span> <span data-ttu-id="15018-110">Se il provider di eventi non è in esecuzione quando si verifica un evento, WMI avvia il provider quando è necessario recapitare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="15018-110">If the event provider is not running when an event occurs, then WMI starts the provider when it needs to deliver events.</span></span>

<span data-ttu-id="15018-111">Nella procedura seguente viene descritto come implementare un provider di consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="15018-111">The following procedure describes how to implement an event consumer provider.</span></span>

<span data-ttu-id="15018-112">**Per implementare un provider di consumer di eventi**</span><span class="sxs-lookup"><span data-stu-id="15018-112">**To implement an event consumer provider**</span></span>

1.  <span data-ttu-id="15018-113">Progettare le classi consumer in Managed Object Format (MOF) e registrarle con WMI.</span><span class="sxs-lookup"><span data-stu-id="15018-113">Design consumer classes in Managed Object Format (MOF) and register them with WMI.</span></span> <span data-ttu-id="15018-114">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="15018-114">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

    <span data-ttu-id="15018-115">I provider di classi si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e una classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="15018-115">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class.</span></span> <span data-ttu-id="15018-116">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di consumer di eventi](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="15018-116">For more information, see [Registering an Event Consumer Provider](registering-an-event-consumer-provider.md).</span></span>

2.  <span data-ttu-id="15018-117">Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.</span><span class="sxs-lookup"><span data-stu-id="15018-117">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="15018-118">WMI utilizza [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider.</span><span class="sxs-lookup"><span data-stu-id="15018-118">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="15018-119">Per ulteriori informazioni, vedere [inizializzazione di un provider](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="15018-119">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="15018-120">I provider di consumer di eventi sono vivamente invitati a usare il modello di multithreading "both".</span><span class="sxs-lookup"><span data-stu-id="15018-120">Event consumer providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="15018-121">Implementare l'interfaccia [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) per il provider.</span><span class="sxs-lookup"><span data-stu-id="15018-121">Implement the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface for your provider.</span></span>

    <span data-ttu-id="15018-122">L'interfaccia [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) è l'interfaccia principale per un provider di consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="15018-122">The [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface is the primary interface for an event consumer provider.</span></span>

4.  <span data-ttu-id="15018-123">Fornire uno o più consumer fisici per ricevere i messaggi di evento da WMI.</span><span class="sxs-lookup"><span data-stu-id="15018-123">Supply one or more physical consumers to receive the event messages from WMI.</span></span>

    <span data-ttu-id="15018-124">Un consumer fisico è un oggetto COM che rappresenta un consumer di eventi permanenti.</span><span class="sxs-lookup"><span data-stu-id="15018-124">A physical consumer is a COM object that represents a permanent event consumer.</span></span> <span data-ttu-id="15018-125">Tutti i consumer fisici devono implementare l'interfaccia [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) .</span><span class="sxs-lookup"><span data-stu-id="15018-125">All physical consumers must implement the [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) interface.</span></span> <span data-ttu-id="15018-126">Per ulteriori informazioni, vedere [implementazione di un consumer fisico](implementing-a-physical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="15018-126">For more information, see [Implementing a Physical Consumer](implementing-a-physical-consumer.md).</span></span>

 

 



