---
description: Per creare un provider di consumer di eventi WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ EventConsumerProviderRegistration.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registrazione di un provider di consumer di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755047"
---
# <a name="registering-an-event-consumer-provider"></a><span data-ttu-id="16ee6-103">Registrazione di un provider di consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="16ee6-103">Registering an Event Consumer Provider</span></span>

<span data-ttu-id="16ee6-104">Per creare un [*provider di consumer di eventi*](gloss-e.md) WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="16ee6-104">To create a WMI [*event consumer provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="16ee6-105">Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI.</span><span class="sxs-lookup"><span data-stu-id="16ee6-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="16ee6-106">Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="16ee6-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="16ee6-107">Nella procedura seguente viene descritto come registrare un provider di consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="16ee6-107">The following procedure describes how to register an event consumer provider.</span></span>

<span data-ttu-id="16ee6-108">**Per registrare un provider di consumer di eventi**</span><span class="sxs-lookup"><span data-stu-id="16ee6-108">**To register an event consumer provider**</span></span>

1.  <span data-ttu-id="16ee6-109">Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.</span><span class="sxs-lookup"><span data-stu-id="16ee6-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="16ee6-110">Creare un'istanza della classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) che descrive il set di funzionalità del provider.</span><span class="sxs-lookup"><span data-stu-id="16ee6-110">Create an instance of the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="16ee6-111">Le proprietà definite da [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) includono il percorso dell'oggetto per il provider e i nomi delle classi di consumer logiche supportate dal provider di consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="16ee6-111">The properties that are defined by [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) include the object path to the provider and the names of the logical consumer classes that the event consumer provider supports.</span></span>

    <span data-ttu-id="16ee6-112">Assicurarsi di contrassegnare la classe con i qualificatori **dinamici** e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="16ee6-112">Be sure to tag the class with both the **Dynamic** and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="16ee6-113">Il qualificatore **dinamico** segnala che WMI deve usare un provider per recuperare le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="16ee6-113">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="16ee6-114">Il qualificatore del **provider** specifica il nome del provider che WMI deve utilizzare.</span><span class="sxs-lookup"><span data-stu-id="16ee6-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="16ee6-115">Nell'esempio di codice seguente viene illustrato come registrare un provider di consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="16ee6-115">The following code example shows how to register an event consumer provider.</span></span>

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



