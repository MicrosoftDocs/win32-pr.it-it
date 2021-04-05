---
description: Per creare un provider di eventi WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ EventProviderRegistration.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Registrazione di un provider di eventi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131918"
---
# <a name="registering-an-event-provider"></a><span data-ttu-id="a045d-103">Registrazione di un provider di eventi</span><span class="sxs-lookup"><span data-stu-id="a045d-103">Registering an Event Provider</span></span>

<span data-ttu-id="a045d-104">Per creare un [*provider di eventi*](gloss-e.md) WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="a045d-104">To create a WMI [*event provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventProviderRegistration**](--eventproviderregistration.md).</span></span> <span data-ttu-id="a045d-105">Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI.</span><span class="sxs-lookup"><span data-stu-id="a045d-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="a045d-106">Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a045d-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="a045d-107">Nella procedura riportata di seguito viene descritto come registrare un provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="a045d-107">The following procedure describes how to register an event provider.</span></span>

<span data-ttu-id="a045d-108">**Per registrare un provider di eventi**</span><span class="sxs-lookup"><span data-stu-id="a045d-108">**To register an event provider**</span></span>

1.  <span data-ttu-id="a045d-109">Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.</span><span class="sxs-lookup"><span data-stu-id="a045d-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="a045d-110">Creare un'istanza della classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) che descrive il set di funzionalità del provider.</span><span class="sxs-lookup"><span data-stu-id="a045d-110">Create an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="a045d-111">La classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="a045d-111">The [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class.</span></span> <span data-ttu-id="a045d-112">Le proprietà locali della classe **\_ \_ EventProviderRegistration** sono il percorso dell'oggetto per il provider e un elenco di query che descrivono gli eventi supportati dal provider.</span><span class="sxs-lookup"><span data-stu-id="a045d-112">The properties local to the **\_\_EventProviderRegistration** class are the object path to the provider and a list of queries that describe the events that the provider supports.</span></span> <span data-ttu-id="a045d-113">Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a045d-113">For more information, see [Querying WMI](querying-wmi.md).</span></span>

3.  <span data-ttu-id="a045d-114">Caricare l'implementazione delle classi [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="a045d-114">Load your implementation of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) classes into the WMI repository.</span></span>

    <span data-ttu-id="a045d-115">WMI utilizza la definizione della classe per registrare e accedere al provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="a045d-115">WMI uses your class definition to register and access your event provider.</span></span> <span data-ttu-id="a045d-116">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a045d-116">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="a045d-117">Nell'esempio di codice seguente viene descritta un'implementazione di una classe [**\_ \_ Win32Provider**](--win32provider.md) e di una classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="a045d-117">The following code example describes an implementation of a [**\_\_Win32Provider**](--win32provider.md) class and a [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

<span data-ttu-id="a045d-118">La prima query indica che il provider genera tutte le notifiche degli eventi per la classe di evento estrinseca FaxEvent.</span><span class="sxs-lookup"><span data-stu-id="a045d-118">The first query indicates that the provider generates all event notifications for the extrinsic event class FaxEvent.</span></span> <span data-ttu-id="a045d-119">Poiché usa l'operatore ISA, la seconda query implica che il provider genera notifiche per tutti gli eventi di creazione dell'istanza per la classe [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e per tutte le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a045d-119">Because it uses the ISA operator, the second query implies that the provider generates notifications for all instance creation events for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and all of its subclasses.</span></span>

<span data-ttu-id="a045d-120">Quando un provider viene registrato per fornire un evento intrinseco, l'evento deve essere applicato a tutte le istanze di una classe.</span><span class="sxs-lookup"><span data-stu-id="a045d-120">When a provider registers to provide an intrinsic event, the event must apply to all instances of a class.</span></span> <span data-ttu-id="a045d-121">In altre parole, non è possibile scrivere una query per fornire eventi di creazione di istanze solo per alcune unità disco che appartengono alla classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="a045d-121">In other words, a query cannot be written to provide instance creation events for only some of the disk drives that belong to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

 

 
