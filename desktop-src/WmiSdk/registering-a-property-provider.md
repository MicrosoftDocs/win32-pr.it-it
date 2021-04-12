---
description: Per creare un provider di proprietà WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrazione di un provider di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226835"
---
# <a name="registering-a-property-provider"></a><span data-ttu-id="335ce-103">Registrazione di un provider di proprietà</span><span class="sxs-lookup"><span data-stu-id="335ce-103">Registering a Property Provider</span></span>

<span data-ttu-id="335ce-104">Per creare un [*provider di proprietà*](gloss-p.md) WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="335ce-104">To create a WMI [*property provider*](gloss-p.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span> <span data-ttu-id="335ce-105">Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI.</span><span class="sxs-lookup"><span data-stu-id="335ce-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="335ce-106">Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="335ce-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="335ce-107">Nella procedura riportata di seguito viene descritto come registrare un provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="335ce-107">The following procedure describes how to register a property provider.</span></span>

<span data-ttu-id="335ce-108">**Per registrare un provider di proprietà**</span><span class="sxs-lookup"><span data-stu-id="335ce-108">**To register a property provider**</span></span>

1.  <span data-ttu-id="335ce-109">Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="335ce-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the property provider.</span></span>

    <span data-ttu-id="335ce-110">La classe [**\_ \_ Win32Provider**](--win32provider.md) accetta i valori predefiniti per altre proprietà, ad esempio il valore **true** per la proprietà **pure** .</span><span class="sxs-lookup"><span data-stu-id="335ce-110">The [**\_\_Win32Provider**](--win32provider.md) class accepts the default values for other properties, such as the **TRUE** value for the **Pure** property.</span></span> <span data-ttu-id="335ce-111">Per ulteriori informazioni, vedere [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="335ce-111">For more information, see [**\_\_Win32Provider**](--win32provider.md).</span></span>

2.  <span data-ttu-id="335ce-112">Creare un'istanza della classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) che descrive il set di funzionalità del provider.</span><span class="sxs-lookup"><span data-stu-id="335ce-112">Create an instance of the [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="335ce-113">La classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , che fornisce valori booleani che indicano il supporto per caratteristiche specifiche e una matrice di stringhe per indicare il supporto delle query.</span><span class="sxs-lookup"><span data-stu-id="335ce-113">The [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="335ce-114">Assicurarsi di contrassegnare la classe con i qualificatori [**dinamici**](dynamic-qualifier.md) e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="335ce-114">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="335ce-115">Il qualificatore **dinamico** segnala che WMI deve usare un provider dinamico per recuperare le istanze della classe che contengono le proprietà supportate.</span><span class="sxs-lookup"><span data-stu-id="335ce-115">The **Dynamic** qualifier signals that WMI should use a dynamic provider to retrieve the class instances that contain the supported properties.</span></span> <span data-ttu-id="335ce-116">Il qualificatore del **provider** specifica il nome del provider che WMI deve utilizzare.</span><span class="sxs-lookup"><span data-stu-id="335ce-116">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="335ce-117">WMI chiama NewQuery su un provider di eventi quando un consumer client registra una query del filtro eventi che contiene riferimenti a eventi supportati da tale provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="335ce-117">WMI calls NewQuery on an event provider when a client consumer registers an event filter query that contains references to events supported by that event provider.</span></span> <span data-ttu-id="335ce-118">Il provider di eventi responsabile degli eventi di modifica dell'istanza per la classe EmailClass può quindi essere configurato per generare notifiche solo per il mittente.</span><span class="sxs-lookup"><span data-stu-id="335ce-118">So the event provider responsible for instance modification events for the EmailClass class can be set up to generate notifications only for sender.</span></span> <span data-ttu-id="335ce-119">Quando il provider riceve una query che richiede la notifica delle modifiche apportate alla proprietà Subject, il provider può iniziare a generare tali notifiche.</span><span class="sxs-lookup"><span data-stu-id="335ce-119">When the provider receives a query requesting notification of changes to the subject property, the provider can start generating those notifications.</span></span> <span data-ttu-id="335ce-120">In questo scenario non è necessario che WMI elimini le notifiche che segnalano solo le modifiche del destinatario.</span><span class="sxs-lookup"><span data-stu-id="335ce-120">In this scenario, WMI is not required to discard the notifications that report recipient changes only.</span></span>

<span data-ttu-id="335ce-121">Nell'esempio di codice MOF seguente vengono descritte le istanze di che possono essere utilizzate per registrare un provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="335ce-121">The following MOF code example describes instances that can be used to register a property provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> <span data-ttu-id="335ce-122">Solo gli amministratori possono registrare o eliminare un provider di proprietà creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="335ce-122">Only administrators can register or delete a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span>

 

 

 



