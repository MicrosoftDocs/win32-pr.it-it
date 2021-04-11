---
description: Per creare un provider di metodi WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ MethodProviderRegistration.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrazione di un provider di metodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232395"
---
# <a name="registering-a-method-provider"></a><span data-ttu-id="7ba0b-103">Registrazione di un provider di metodi</span><span class="sxs-lookup"><span data-stu-id="7ba0b-103">Registering a Method Provider</span></span>

<span data-ttu-id="7ba0b-104">Per creare un [*provider di metodi*](gloss-m.md) WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="7ba0b-104">To create a WMI [*method provider*](gloss-m.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_MethodProviderRegistration**](--methodproviderregistration.md).</span></span> <span data-ttu-id="7ba0b-105">Dopo aver creato un'istanza di [**\_ \_ Win32Provider**](--win32provider.md), è necessario registrare il provider con WMI.</span><span class="sxs-lookup"><span data-stu-id="7ba0b-105">After creating an instance of [**\_\_Win32Provider**](--win32provider.md), you must register that provider with WMI.</span></span> <span data-ttu-id="7ba0b-106">Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI.</span><span class="sxs-lookup"><span data-stu-id="7ba0b-106">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="7ba0b-107">Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7ba0b-107">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="7ba0b-108">Nella procedura riportata di seguito viene descritto come registrare un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="7ba0b-108">The following procedure describes how to register a method provider.</span></span>

<span data-ttu-id="7ba0b-109">**Per registrare un provider di metodi**</span><span class="sxs-lookup"><span data-stu-id="7ba0b-109">**To register a method provider**</span></span>

1.  <span data-ttu-id="7ba0b-110">Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.</span><span class="sxs-lookup"><span data-stu-id="7ba0b-110">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>

    <span data-ttu-id="7ba0b-111">La classe di sistema [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) . Tuttavia, l'unica proprietà pertinente per un provider di metodi è il percorso dell'oggetto per l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="7ba0b-111">The [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) system class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, However, the only property relevant for a method provider is the object path to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span>

2.  <span data-ttu-id="7ba0b-112">Creare un'istanza della classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) che descrive il set di funzionalità del provider.</span><span class="sxs-lookup"><span data-stu-id="7ba0b-112">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="7ba0b-113">Assicurarsi di contrassegnare la classe con i qualificatori [**dinamici**](dynamic-qualifier.md) e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="7ba0b-113">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="7ba0b-114">Il qualificatore **dinamico** segnala che WMI deve usare un provider per recuperare le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="7ba0b-114">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="7ba0b-115">Il qualificatore del **provider** specifica il nome del provider che WMI deve utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7ba0b-115">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="7ba0b-116">Nell'esempio di codice seguente viene illustrato come registrare un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="7ba0b-116">The following code example describes how to register a method provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



