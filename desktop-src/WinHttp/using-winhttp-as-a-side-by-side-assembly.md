---
description: In Windows Server 2003, WinHTTP viene implementato come assembly affiancato e deve essere collegato a tale scopo. Si noti che questa operazione non si applica a Windows Vista e versioni successive.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Uso di WinHTTP come assembly affiancato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751511"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a><span data-ttu-id="35c23-104">Uso di WinHTTP come assembly affiancato</span><span class="sxs-lookup"><span data-stu-id="35c23-104">Using WinHTTP as a Side-by-side Assembly</span></span>

<span data-ttu-id="35c23-105">In Windows Server 2003, WinHTTP viene implementato come assembly affiancato e deve essere collegato a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="35c23-105">On Windows Server 2003, WinHTTP is implemented as a side-by-side assembly, and must be linked to as such.</span></span> <span data-ttu-id="35c23-106">Si noti che questa operazione non si applica a Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="35c23-106">Note that this does not apply to Windows Vista and later.</span></span>

## <a name="side-by-side-assemblies"></a><span data-ttu-id="35c23-107">Assembly affiancati</span><span class="sxs-lookup"><span data-stu-id="35c23-107">Side-by-side Assemblies</span></span>

<span data-ttu-id="35c23-108">A partire da Microsoft Windows XP, è stato fornito un meccanismo di assembly affiancati per controllare il collegamento della fase di esecuzione per evitare conflitti di controllo delle versioni delle librerie a collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="35c23-108">Starting with Microsoft Windows XP, a side-by-side assemblies mechanism was provided to control run-time linking to avoid dynamic-link-library (DLL) versioning conflicts.</span></span> <span data-ttu-id="35c23-109">Per informazioni sugli assembly affiancati, vedere [informazioni sulle applicazioni isolate e gli assembly affiancati](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span><span class="sxs-lookup"><span data-stu-id="35c23-109">For information about side-by-side assemblies, see [About Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span></span>

<span data-ttu-id="35c23-110">Per usare questo meccanismo per il collegamento a WinHTTP versione 5,1 in Windows Server 2003, un'applicazione deve incorporare un manifesto che specifichi WinHTTP come assembly dipendente.</span><span class="sxs-lookup"><span data-stu-id="35c23-110">To use this mechanism to link to WinHTTP version 5.1 on Windows Server 2003, an application must incorporate a manifest that specifies WinHTTP as a dependent assembly.</span></span> <span data-ttu-id="35c23-111">Per ulteriori informazioni su come eseguire questa operazione, vedere [utilizzo degli assembly affiancati](/windows/desktop/SbsCs/using-side-by-side-assemblies) .</span><span class="sxs-lookup"><span data-stu-id="35c23-111">See [Using Side-by-side Assemblies](/windows/desktop/SbsCs/using-side-by-side-assemblies) for more information about how to do this.</span></span>

## <a name="a-sample-winhttp-application-manifest"></a><span data-ttu-id="35c23-112">Manifesto dell'applicazione WinHTTP di esempio</span><span class="sxs-lookup"><span data-stu-id="35c23-112">A Sample WinHTTP Application Manifest</span></span>

<span data-ttu-id="35c23-113">Il manifesto di esempio seguente illustra un manifesto dell'applicazione che può essere usato per il collegamento a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="35c23-113">The sample manifest below illustrates an application manifest that can be used for linking to WinHTTP.</span></span>

<span data-ttu-id="35c23-114">Tutti gli attributi tranne "Type" di " <assembly> <assemblyIdentity> " devono essere modificati in modo appropriato per l'applicazione specifica.</span><span class="sxs-lookup"><span data-stu-id="35c23-114">All attributes except "type" of the "<assembly><assemblyIdentity>" must be modified as appropriate for your particular application.</span></span> <span data-ttu-id="35c23-115">Lo stesso vale per il contenuto dell'elemento " &lt; Description &gt; ".</span><span class="sxs-lookup"><span data-stu-id="35c23-115">The same goes for the contents of the "&lt;description&gt;" element.</span></span>

<span data-ttu-id="35c23-116">Assicurarsi inoltre che l'attributo "processorArchitecture" di " <dependentAssembly> <assemblyIdentity> " corrisponda all'attributo "ProcessorArchitecture" di " <assembly> <assemblyIdentity> ".</span><span class="sxs-lookup"><span data-stu-id="35c23-116">In addition, make sure that the "processorArchitecture" attribute of the "<dependentAssembly><assemblyIdentity>" matches the "processorArchitecture" attribute of the "<assembly><assemblyIdentity>".</span></span> <span data-ttu-id="35c23-117">Di seguito, ad esempio, entrambi sono impostati su "x86".</span><span class="sxs-lookup"><span data-stu-id="35c23-117">Below, for example, both are set to "x86".</span></span>

<span data-ttu-id="35c23-118">Tutti i valori non specifici dell'applicazione dovrebbero avere i moduli mostrati di seguito.</span><span class="sxs-lookup"><span data-stu-id="35c23-118">All values not specific to your application should take the forms shown below.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
