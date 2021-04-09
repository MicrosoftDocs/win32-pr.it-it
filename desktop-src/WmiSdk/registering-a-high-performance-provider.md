---
description: Analogamente ad altri provider di istanze, è possibile registrare un provider a prestazioni elevate con Microsoft Windows&\# 160; Strumentazione gestione (WMI) creando un'istanza delle \_ \_ classi Win32Provider e \_ \_ InstanceProviderRegistration.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Registrazione di un provider di High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049759"
---
# <a name="registering-a-high-performance-provider"></a><span data-ttu-id="367e5-103">Registrazione di un provider di High-Performance</span><span class="sxs-lookup"><span data-stu-id="367e5-103">Registering a High-Performance Provider</span></span>

<span data-ttu-id="367e5-104">Analogamente ad altri provider di istanze, è possibile registrare un provider a prestazioni elevate con Microsoft Strumentazione gestione Windows (WMI) creando un'istanza delle classi [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="367e5-104">Like other instance providers, you register a high-performance provider with Microsoft Windows Management Instrumentation (WMI) by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes.</span></span> <span data-ttu-id="367e5-105">L'istanza **\_ \_ Win32Provider** definisce l'implementazione fisica del provider e l'istanza di **\_ \_ InstanceProviderRegistration** definisce il set di funzionalità del provider.</span><span class="sxs-lookup"><span data-stu-id="367e5-105">The **\_\_Win32Provider** instance defines the provider's physical implementation, and the **\_\_InstanceProviderRegistration** instance defines the provider's feature set.</span></span> <span data-ttu-id="367e5-106">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="367e5-106">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="367e5-107">Nella procedura riportata di seguito viene descritto come registrare un provider di istanze a prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="367e5-107">The following procedure describes how to register a high-performance instance provider.</span></span>

<span data-ttu-id="367e5-108">**Per registrare un provider di istanze a prestazioni elevate**</span><span class="sxs-lookup"><span data-stu-id="367e5-108">**To register a high-performance instance provider**</span></span>

1.  <span data-ttu-id="367e5-109">Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.</span><span class="sxs-lookup"><span data-stu-id="367e5-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class describing the provider.</span></span>

    <span data-ttu-id="367e5-110">Assicurarsi di aggiungere una proprietà **ClientLoadableCLSID** all'istanza di [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="367e5-110">Be sure to add a **ClientLoadableCLSID** property to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span> <span data-ttu-id="367e5-111">Se il provider e il client si trovano nello stesso computer, WMI carica il provider in-process nel client usando **ClientLoadableCLSID** come identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="367e5-111">If both the provider and client reside on the same computer, WMI loads the provider in-process to the client using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="367e5-112">Quando il provider e il client si trovano in computer diversi, WMI carica il provider in-process in WMI.</span><span class="sxs-lookup"><span data-stu-id="367e5-112">When the provider and client reside on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="367e5-113">WMI inoltre utilizza **ClientLoadableCLSID** per supportare le operazioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="367e5-113">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

2.  <span data-ttu-id="367e5-114">Creare un'istanza della classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) che descrive il set di funzionalità del provider.</span><span class="sxs-lookup"><span data-stu-id="367e5-114">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="367e5-115">Assicurarsi di contrassegnare la classe con i qualificatori [**dinamici**](dynamic-qualifier.md) e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="367e5-115">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="367e5-116">Il qualificatore **dinamico** segnala che WMI deve usare un provider per recuperare le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="367e5-116">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="367e5-117">Il qualificatore del **provider** specifica il nome del provider che WMI deve utilizzare.</span><span class="sxs-lookup"><span data-stu-id="367e5-117">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

    <span data-ttu-id="367e5-118">Un provider a prestazioni elevate deve inoltre supportare lo stato del supporto per operazioni, operazioni di enumerazione o entrambi.</span><span class="sxs-lookup"><span data-stu-id="367e5-118">A high-performance provider also needs to state support for operations, enumeration operations, or both.</span></span> <span data-ttu-id="367e5-119">Assicurarsi di usare le proprietà **SupportsGet** e **SupportsEnumeration** nell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="367e5-119">Make sure you use the **SupportsGet** and **SupportsEnumeration** properties in your implementation.</span></span>

<span data-ttu-id="367e5-120">Nell'esempio di codice seguente viene illustrato come implementare le classi [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) per un provider a prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="367e5-120">The following code example shows you how to implement the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes for a high-performance provider.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a><span data-ttu-id="367e5-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="367e5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="367e5-122">Creazione di un provider di istanze in un provider di High-Performance</span><span class="sxs-lookup"><span data-stu-id="367e5-122">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



