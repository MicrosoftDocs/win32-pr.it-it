---
description: Per creare un provider di istanze WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ InstanceProviderRegistration.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Registrazione di un provider di istanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528501"
---
# <a name="registering-an-instance-provider"></a><span data-ttu-id="568ad-103">Registrazione di un provider di istanze</span><span class="sxs-lookup"><span data-stu-id="568ad-103">Registering an Instance Provider</span></span>

<span data-ttu-id="568ad-104">Per creare un [*provider di istanze*](gloss-i.md) WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="568ad-104">To create a WMI [*instance provider*](gloss-i.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="568ad-105">Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI.</span><span class="sxs-lookup"><span data-stu-id="568ad-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="568ad-106">Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="568ad-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="568ad-107">Nella procedura riportata di seguito viene descritto come registrare un provider di istanze.</span><span class="sxs-lookup"><span data-stu-id="568ad-107">The following procedure describes how to register an instance provider.</span></span>

<span data-ttu-id="568ad-108">**Per registrare un provider di istanze**</span><span class="sxs-lookup"><span data-stu-id="568ad-108">**To register an instance provider**</span></span>

1.  <span data-ttu-id="568ad-109">Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.</span><span class="sxs-lookup"><span data-stu-id="568ad-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="568ad-110">Creare un'istanza della classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) che descrive il set di funzionalità del provider.</span><span class="sxs-lookup"><span data-stu-id="568ad-110">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="568ad-111">La classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , che fornisce valori booleani che indicano il supporto per caratteristiche specifiche e una matrice di stringhe per indicare il supporto delle query.</span><span class="sxs-lookup"><span data-stu-id="568ad-111">The [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="568ad-112">Assicurarsi di contrassegnare la classe con i qualificatori [**dinamici**](standard-wmi-qualifiers.md) e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="568ad-112">Be sure to tag the class with both the [**Dynamic**](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="568ad-113">Il qualificatore segnala che WMI deve usare un provider **dinamico** per recuperare le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="568ad-113">The qualifier signals that WMI should use a **Dynamic** provider to retrieve the class instances.</span></span> <span data-ttu-id="568ad-114">Il qualificatore del **provider** specifica il nome del provider che WMI deve utilizzare.</span><span class="sxs-lookup"><span data-stu-id="568ad-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="568ad-115">Nell'esempio di codice seguente viene descritto come registrare un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="568ad-115">The following code example describes how to register a [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) instance.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



