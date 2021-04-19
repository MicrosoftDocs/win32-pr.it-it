---
description: Uso di .NET Framework 4 con applicazioni compilate in versioni precedenti
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Uso di .NET Framework 4 con applicazioni compilate in versioni precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef252d128ae5d3c8f5b85ef486828fb82e152d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319824"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a><span data-ttu-id="483f9-103">Uso di .NET Framework 4 con applicazioni compilate in versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="483f9-103">Using .NET Framework 4 with Applications Built on Earlier Versions</span></span>

## <a name="platform"></a><span data-ttu-id="483f9-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="483f9-104">Platform</span></span>

 <span data-ttu-id="483f9-105">**Client** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="483f9-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="483f9-106">**Server** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="483f9-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="483f9-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="483f9-107">Feature Impact</span></span>

 <span data-ttu-id="483f9-108">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="483f9-108">**Severity** - Low</span></span>  
<span data-ttu-id="483f9-109">**Frequenza** -alta</span><span class="sxs-lookup"><span data-stu-id="483f9-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="483f9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="483f9-110">Description</span></span>

<span data-ttu-id="483f9-111">Il .NET Framework 4 è altamente compatibile con le applicazioni compilate utilizzando versioni di .NET Framework precedenti.</span><span class="sxs-lookup"><span data-stu-id="483f9-111">The .NET Framework 4 is highly compatible with applications that are built by using earlier .NET Framework versions.</span></span> <span data-ttu-id="483f9-112">Le principali modifiche apportate al .NET Framework 4 sono migliorare la sicurezza, la conformità agli standard, la correttezza, l'affidabilità e le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="483f9-112">The primary changes in .NET Framework 4 are to improve security, standards compliance, correctness, reliability, and performance.</span></span>

<span data-ttu-id="483f9-113">Tuttavia, .NET Framework 4 non utilizza automaticamente la versione del Common Language Runtime (CLR) per eseguire le applicazioni compilate utilizzando versioni precedenti del .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="483f9-113">However, .NET Framework 4 does not automatically use its version of the common language runtime (CLR) to run applications that are built by using earlier versions of the .NET Framework.</span></span>

## <a name="manifestation"></a><span data-ttu-id="483f9-114">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="483f9-114">Manifestation</span></span>

<span data-ttu-id="483f9-115">Se un'applicazione è stata compilata utilizzando una .NET Framework precedente e un utente apre tale applicazione in un computer in cui sono presenti sia .NET Framework 4 che la versione precedente del .NET Framework installata, l'applicazione utilizzerà la versione CLR precedente.</span><span class="sxs-lookup"><span data-stu-id="483f9-115">If you built an application by using an earlier .NET Framework and a user opens that application on a computer that has both .NET Framework 4 and the earlier version of the .NET Framework installed, the application uses the earlier CLR version.</span></span>

<span data-ttu-id="483f9-116">Tuttavia, se il .NET Framework 4 è l'unica versione runtime installata nel computer, l'applicazione genera un'eccezione e chiede all'utente di installare la versione di runtime in cui è stata compilata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="483f9-116">However, if the .NET Framework 4 is the only runtime version that is installed on the computer, the application throws an exception and asks the user to install the runtime version that you built the application against.</span></span>

## <a name="solution"></a><span data-ttu-id="483f9-117">Soluzione</span><span class="sxs-lookup"><span data-stu-id="483f9-117">Solution</span></span>

<span data-ttu-id="483f9-118">Per eseguire applicazioni compilate con versioni precedenti di .NET Framework con .NET Framework 4, è necessario compilare l'applicazione in modo che abbia come destinazione la versione .NET Framework 4 specificando il valore nelle proprietà del progetto in Microsoft Visual Studio oppure è possibile specificare .NET Framework 4 nell' [**<supportedRuntime> elemento**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in un file di configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="483f9-118">To run applications that are built with earlier .NET Framework versions with .NET Framework 4, you must compile your application to target the .NET Framework 4 version by specifying it in the properties for your project in Microsoft Visual Studio, or you can specify .NET Framework 4 in the [**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in an application configuration file.</span></span>

<span data-ttu-id="483f9-119">Per ulteriori informazioni su come eseguire la migrazione a .NET Framework 4, vedere la [Guida alla migrazione per la .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) e la [compatibilità tra le versioni nella .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="483f9-119">For more information about how to migrate to the .NET Framework 4, see [Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) and [Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="483f9-120">Test di compatibilità</span><span class="sxs-lookup"><span data-stu-id="483f9-120">Compatibility Tests</span></span>

<span data-ttu-id="483f9-121">Dopo avere apportato le modifiche, testare l'applicazione per assicurarsi che venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="483f9-121">After you make the changes, test your application to make sure that it runs correctly.</span></span> <span data-ttu-id="483f9-122">È possibile testare la compatibilità come descritto nell'argomento relativo alla [compatibilità delle applicazioni .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="483f9-122">You can test compatibility as described in the [.NET Framework 4 Application Compatibility](/previous-versions/dd889541(v=msdn.10)) topic.</span></span>

<span data-ttu-id="483f9-123">Se l'applicazione o il componente non funziona dopo l'installazione di .NET Framework 4, inviare un bug tramite il sito Web [Microsoft Connect](https://connect.microsoft.com/visualstudio) .</span><span class="sxs-lookup"><span data-stu-id="483f9-123">If your application or component does not work after .NET Framework 4 is installed, submit a bug through the [Microsoft Connect](https://connect.microsoft.com/visualstudio) website.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="483f9-124">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="483f9-124">Links to Other Resources</span></span>

-   <span data-ttu-id="483f9-125">[**<supportedRuntime> elemento**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="483f9-125">[**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span></span>
-   <span data-ttu-id="483f9-126">[Guida di migrazione a .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="483f9-126">[Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span></span>
-   <span data-ttu-id="483f9-127">[Compatibilità tra le versioni in .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="483f9-127">[Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span></span>
-   <span data-ttu-id="483f9-128">**Procedura dettagliata per la compatibilità delle applicazioni .NET Framework 4 RTM:**<https://msdn.microsoft.com/library/dd889541.aspx></span><span class="sxs-lookup"><span data-stu-id="483f9-128">**.NET Framework 4 RTM Application Compatibility Walkthrough:**<https://msdn.microsoft.com/library/dd889541.aspx></span></span>
-   [<span data-ttu-id="483f9-129">Microsoft Connect</span><span class="sxs-lookup"><span data-stu-id="483f9-129">Microsoft Connect</span></span>](https://connect.microsoft.com/)

 

 
