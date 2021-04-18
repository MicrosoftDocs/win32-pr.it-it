---
description: Utilizzando la classe SMTPEventConsumer, è possibile inviare un messaggio di posta elettronica a un utente designato quando si verifica un evento specifico. Questa classe è un consumer di eventi standard fornito da WMI.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Invio di messaggi di posta elettronica in base a un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313179"
---
# <a name="sending-email-based-on-an-event"></a><span data-ttu-id="97862-104">Invio di messaggi di posta elettronica in base a un evento</span><span class="sxs-lookup"><span data-stu-id="97862-104">Sending Email Based on an Event</span></span>

<span data-ttu-id="97862-105">Utilizzando la classe [SMTPEventConsumer](smtpeventconsumer.md) , è possibile inviare un messaggio di posta elettronica a un utente designato quando si verifica un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="97862-105">By using the [SMTPEventConsumer](smtpeventconsumer.md) class, you can send email to a designated user when a specified event occurs.</span></span> <span data-ttu-id="97862-106">Questa classe è un [consumer di eventi standard](standard-consumer-classes.md) fornito da WMI.</span><span class="sxs-lookup"><span data-stu-id="97862-106">This class is a [standard event consumer](standard-consumer-classes.md) that WMI provides.</span></span>

<span data-ttu-id="97862-107">Per inviare un messaggio di posta elettronica in risposta a un evento, la classe [SMTPEventConsumer](smtpeventconsumer.md) richiede le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="97862-107">The [SMTPEventConsumer](smtpeventconsumer.md) class requires the following conditions to send an email message in response to an event:</span></span>

-   <span data-ttu-id="97862-108">La classe [SMTPEventConsumer](smtpeventconsumer.md) deve essere compilata nello spazio dei nomi corretto.</span><span class="sxs-lookup"><span data-stu-id="97862-108">The [SMTPEventConsumer](smtpeventconsumer.md) class must be compiled into the correct namespace.</span></span> <span data-ttu-id="97862-109">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="97862-109">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>
-   <span data-ttu-id="97862-110">Un server SMTP deve esistere sulla rete.</span><span class="sxs-lookup"><span data-stu-id="97862-110">An SMTP server must exist on the network.</span></span>
-   <span data-ttu-id="97862-111">Il messaggio di posta elettronica non può contenere un allegato.</span><span class="sxs-lookup"><span data-stu-id="97862-111">The email message cannot have an attachment.</span></span>
-   <span data-ttu-id="97862-112">Il messaggio di posta elettronica deve essere codificato in US-ASCII.</span><span class="sxs-lookup"><span data-stu-id="97862-112">The email message must be encoded in US-ASCII.</span></span>

<span data-ttu-id="97862-113">La procedura di base per l'utilizzo di consumer standard è sempre la stessa ed è disponibile per il [monitoraggio e la risposta a eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="97862-113">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="97862-114">La procedura seguente consente di aggiungere alla procedura di base. è specifico della classe [SMTPEventConsumer](smtpeventconsumer.md) . e descrive come creare un consumer di eventi che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="97862-114">The following procedure adds to the basic procedure; is specific to the [SMTPEventConsumer](smtpeventconsumer.md) class; and describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="97862-115">Nella procedura seguente viene descritto come creare un consumer di eventi che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="97862-115">The following procedure describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="97862-116">**Per creare un consumer di eventi che invii un messaggio di posta elettronica**</span><span class="sxs-lookup"><span data-stu-id="97862-116">**To create an event consumer that sends email**</span></span>

1.  <span data-ttu-id="97862-117">Installare e registrare la classe [SMTPEventConsumer](smtpeventconsumer.md) , se necessario.</span><span class="sxs-lookup"><span data-stu-id="97862-117">Install and register the [SMTPEventConsumer](smtpeventconsumer.md) class, if necessary.</span></span>

    <span data-ttu-id="97862-118">La classe [SMTPEventConsumer](smtpeventconsumer.md) viene compilata nello \\ spazio dei nomi della sottoscrizione radice dal programma di installazione di WMI.</span><span class="sxs-lookup"><span data-stu-id="97862-118">The [SMTPEventConsumer](smtpeventconsumer.md) class is compiled into the root\\subscription namespace by the WMI setup program.</span></span>

2.  <span data-ttu-id="97862-119">Identificare l'evento che si desidera monitorare e creare la query di eventi.</span><span class="sxs-lookup"><span data-stu-id="97862-119">Identify the event that you want to monitor and create the event query.</span></span>

    <span data-ttu-id="97862-120">Potrebbe esistere un evento intrinseco esistente che usa per monitorare l'evento.</span><span class="sxs-lookup"><span data-stu-id="97862-120">There might be an existing intrinsic event that use to monitor your event.</span></span> <span data-ttu-id="97862-121">La maggior parte degli eventi intrinseci è associata alle modifiche apportate alle istanze di classe nello \\ spazio dei nomi "root cimv2".</span><span class="sxs-lookup"><span data-stu-id="97862-121">Most intrinsic events are associated with changes to class instances in the "root\\cimv2" namespace.</span></span> <span data-ttu-id="97862-122">Analizzando le classi nel riferimento alle [classi WMI](wmi-classes.md) , probabilmente è possibile trovare una classe che identifichi l'evento che si desidera monitorare.</span><span class="sxs-lookup"><span data-stu-id="97862-122">By analyzing the classes in the [WMI Classes](wmi-classes.md) reference, you can probably find a class that identifies the event you want to monitor.</span></span> <span data-ttu-id="97862-123">Ad esempio, usare la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) per monitorare le modifiche apportate a un'unità disco rigido.</span><span class="sxs-lookup"><span data-stu-id="97862-123">For example, use the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class to monitor changes to a hard disk drive.</span></span>

    <span data-ttu-id="97862-124">Se non sono presenti eventi intrinseci che usano, potrebbe essere disponibile un provider di eventi estrinseco che può funzionare.</span><span class="sxs-lookup"><span data-stu-id="97862-124">If there are no existing intrinsic events that use, there might be an extrinsic event provider that can work.</span></span> <span data-ttu-id="97862-125">Utilizzare, ad esempio, la classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) del provider del registro di sistema per monitorare le modifiche apportate al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="97862-125">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="97862-126">Se una classe non esiste che identifica l'evento che si desidera monitorare, è necessario creare un provider di eventi personalizzato e definire nuove classi di evento estrinseche.</span><span class="sxs-lookup"><span data-stu-id="97862-126">If a class does not exist that identifies the event you want to monitor, you must create your own event provider and define new extrinsic event classes.</span></span> <span data-ttu-id="97862-127">Per ulteriori informazioni, vedere [scrittura di un provider di eventi](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="97862-127">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

3.  <span data-ttu-id="97862-128">Nel file Managed Object Format (MOF) creare un'istanza di [SMTPEventConsumer](smtpeventconsumer.md) per ricevere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="97862-128">In the Managed Object Format (MOF) file, create an instance of the [SMTPEventConsumer](smtpeventconsumer.md) to receive events.</span></span>

    <span data-ttu-id="97862-129">Utilizzare le proprietà dell'istanza per definire il messaggio di posta elettronica da inviare quando si verifica un evento.</span><span class="sxs-lookup"><span data-stu-id="97862-129">Use the properties of the instance to define the email message to send when an event occurs.</span></span> <span data-ttu-id="97862-130">Ad esempio, la proprietà **ToLine** definisce l'indirizzo di posta elettronica e la proprietà **Message** definisce il testo del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="97862-130">For example, the **ToLine** property defines the email address, and the **Message** property defines the text of the email message.</span></span> <span data-ttu-id="97862-131">È necessario definire l'indirizzo di posta elettronica, l'oggetto e il testo di un messaggio, ma un messaggio di posta elettronica non può contenere un allegato.</span><span class="sxs-lookup"><span data-stu-id="97862-131">You must define the email address, subject, and text of a message, but an email message cannot have an attachment.</span></span> <span data-ttu-id="97862-132">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="97862-132">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

4.  <span data-ttu-id="97862-133">Creare una query di eventi che specifichi gli eventi che si desidera monitorare.</span><span class="sxs-lookup"><span data-stu-id="97862-133">Create an event query that specifies the events you want to monitor.</span></span>

    <span data-ttu-id="97862-134">Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="97862-134">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

5.  <span data-ttu-id="97862-135">Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) e archiviare la query nella proprietà **query** .</span><span class="sxs-lookup"><span data-stu-id="97862-135">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and store your query in the **Query** property.</span></span>

    <span data-ttu-id="97862-136">Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="97862-136">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

6.  <span data-ttu-id="97862-137">Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro e il consumer.</span><span class="sxs-lookup"><span data-stu-id="97862-137">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer.</span></span>
7.  <span data-ttu-id="97862-138">Compilare il file MOF utilizzando [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="97862-138">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>


## <a name="example"></a><span data-ttu-id="97862-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="97862-139">Example</span></span>

<span data-ttu-id="97862-140">L'esempio in questa sezione è codice MOF, ma è possibile creare le istanze a livello di programmazione usando l' [API di scripting per WMI](scripting-api-for-wmi.md) o l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="97862-140">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="97862-141">Nella procedura riportata di seguito viene descritto come utilizzare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="97862-141">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="97862-142">**Per usare l'esempio**</span><span class="sxs-lookup"><span data-stu-id="97862-142">**To use the example**</span></span>

1.  <span data-ttu-id="97862-143">Copiare il file MOF seguente in un file di testo e salvarlo con un'estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="97862-143">Copy the following MOF to a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="97862-144">In una finestra del prompt dei comandi compilare il file MOF usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="97862-144">In a command prompt window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="97862-145">**Mofcomp** *nomefile \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="97862-145">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

> [!Note]  
> <span data-ttu-id="97862-146">Quando il codice MOF viene compilato nello \\ spazio dei nomi della sottoscrizione radice, il [SMTPEventConsumer](smtpeventconsumer.md) viene compilato nello stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="97862-146">When MOF code is compiled into the root\\subscription namespace, the [SMTPEventConsumer](smtpeventconsumer.md) is compiled into the same namespace.</span></span>

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a><span data-ttu-id="97862-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97862-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97862-148">Monitoraggio e risposta agli eventi con consumer standard</span><span class="sxs-lookup"><span data-stu-id="97862-148">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
