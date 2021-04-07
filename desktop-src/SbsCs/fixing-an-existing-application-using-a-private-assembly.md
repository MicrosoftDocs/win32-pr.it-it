---
description: A partire da Windows XP, è possibile creare un assembly privato e renderlo disponibile per un'applicazione specifica.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Correggere un'applicazione esistente utilizzando un assembly privato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049428"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a><span data-ttu-id="10dc9-103">Correzione di un'applicazione esistente mediante un assembly privato</span><span class="sxs-lookup"><span data-stu-id="10dc9-103">Fixing an Existing Application Using a Private Assembly</span></span>

<span data-ttu-id="10dc9-104">A partire da Windows XP, è possibile creare un assembly privato e renderlo disponibile per un'applicazione specifica.</span><span class="sxs-lookup"><span data-stu-id="10dc9-104">Beginning with Windows XP, you can create a private assembly and make it available to a specific application.</span></span> <span data-ttu-id="10dc9-105">Questa funzionalità può essere usata per correggere un'applicazione che diventa incompatibile con un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="10dc9-105">This capability can be used to fix an application that becomes incompatible with an update.</span></span> <span data-ttu-id="10dc9-106">Un esempio è un'applicazione che diventa incompatibile con la versione più recente di MSVCRT.DLL dopo l'aggiornamento del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="10dc9-106">An example would be an application that becomes incompatible with the latest version of MSVCRT.DLL after upgrading the operating system.</span></span> <span data-ttu-id="10dc9-107">In questo caso, non è possibile sostituire la versione del sistema perché MSVCRT.DLL è un file protetto da Windows.</span><span class="sxs-lookup"><span data-stu-id="10dc9-107">In this case, you do not have the option of replacing the system version because MSVCRT.DLL is a Windows Protected File.</span></span> <span data-ttu-id="10dc9-108">Anziché dover riscrivere l'applicazione in modo che funzioni con la nuova versione di MSVCRT, è possibile creare un assembly privato per MSVCRT e installarlo nella cartella dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="10dc9-108">Rather than having to rewrite the application to work with the new version of MSVCRT, you can create a private assembly for MSVCRT and install this in your application folder.</span></span> <span data-ttu-id="10dc9-109">Si noti che non tutti i componenti condivisi sono un candidato adatto per un assembly side-by-side privato e che alcuni componenti presentano restrizioni di licenza sulla posizione in cui possono essere installati i componenti.</span><span class="sxs-lookup"><span data-stu-id="10dc9-109">Note that not every shared component is a suitable candidate for a private side-by-side assembly, and some components have licensing restrictions about where their components can be installed.</span></span> <span data-ttu-id="10dc9-110">Il componente deve soddisfare i criteri per un componente affiancato.</span><span class="sxs-lookup"><span data-stu-id="10dc9-110">The component needs to meet the criteria for a side-by-side component.</span></span> <span data-ttu-id="10dc9-111">Richiedere all'autore del componente se è possibile fornire un assembly adatto.</span><span class="sxs-lookup"><span data-stu-id="10dc9-111">Ask the publisher of the component if they can provide a suitable assembly.</span></span>

<span data-ttu-id="10dc9-112">Il manifesto dell'assembly privato e il manifesto dell'applicazione devono essere installati nella stessa cartella del file eseguibile dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="10dc9-112">The private assembly's manifest and the application's manifest should both be installed in the same folder as the application's executable.</span></span> <span data-ttu-id="10dc9-113">Quando l'applicazione viene eseguita, viene consultato il manifesto dell'applicazione e viene caricata la versione di MSVCRT privata per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="10dc9-113">When the application runs, it consults the application manifest and load the version of MSVCRT that is private to the application.</span></span>

<span data-ttu-id="10dc9-114">Per questo esempio, l'assembly privato include sia MSVCRT.DLL che MSVCIRT.DLL come nel seguente manifesto dell'assembly:</span><span class="sxs-lookup"><span data-stu-id="10dc9-114">For this example, the private assembly would include both MSVCRT.DLL and MSVCIRT.DLL as in the following assembly manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

<span data-ttu-id="10dc9-115">Di seguito è riportato un esempio di un possibile manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="10dc9-115">The following is an example of a possible application manifest.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



