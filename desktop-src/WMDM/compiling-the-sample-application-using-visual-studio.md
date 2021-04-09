---
title: Compilazione dell'applicazione di esempio con Visual Studio
description: Compilazione dell'applicazione di esempio con Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Media Gestione dispositivi, esempio di applicazione desktop
- Esempio di Gestione dispositivi, applicazione desktop
- esempi, applicazioni desktop
- esempi, compilazione con Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044484"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a><span data-ttu-id="4bbf9-110">Compilazione dell'applicazione di esempio con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4bbf9-110">Compiling the Sample Application Using Visual Studio</span></span>

<span data-ttu-id="4bbf9-111">Windows Media Gestione dispositivi SDK include una soluzione di Visual Studio compatibile con Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="4bbf9-111">The Windows Media Device Manager SDK includes a Visual Studio solution that is compatible with Microsoft Visual Studio 2005.</span></span>

<span data-ttu-id="4bbf9-112">Prima di compilare l'applicazione di esempio, è necessario rinominare il file di intestazione shtypes. h per evitare conflitti con un file con lo stesso nome trovato in Microsoft Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="4bbf9-112">Before you compile the sample application, you must rename the header file shtypes.h to prevent conflicts with a file of the same name that is found in the Microsoft Platform SDK.</span></span> <span data-ttu-id="4bbf9-113">Ad esempio, è possibile rinominare il *percorso di installazione di <SDK* > \\ WMFSDK11 \\ includere \\ shtypes. h nel percorso di installazione di <*SDK* > \\ WMFSDK11 \\ includere \\ shtypes. h. backup.</span><span class="sxs-lookup"><span data-stu-id="4bbf9-113">For example, you could rename <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h to <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h.backup.</span></span>

<span data-ttu-id="4bbf9-114">Per compilare l'applicazione, avviare un'istanza di Visual Studio 2005, aprire il file di soluzione WMDMApp. sln, disponibile nella cartella <*percorso di installazione SDK* > \\ WMFSDK11 \\ Apps \\ WMDMApp e scegliere l'opzione **Compila/Compila soluzione** .</span><span class="sxs-lookup"><span data-stu-id="4bbf9-114">To build the application, start an instance of Visual Studio 2005, open the solution file, wmdmapp.sln, which is found in the folder <*SDK installation path*>\\WMFSDK11\\apps\\wmdmapp and choose the **Build/Build Solution** option.</span></span> <span data-ttu-id="4bbf9-115">In questo modo vengono creati due file di progetto: il progetto helper, proghelp. vcproj, e l'applicazione principale WMDMApp. vcproj.</span><span class="sxs-lookup"><span data-stu-id="4bbf9-115">This will create two project files: the helper project, proghelp.vcproj, as well as the main application wmdmapp.vcproj.</span></span> <span data-ttu-id="4bbf9-116">Inoltre, creerà la DLL dell'helper di avanzamento e l'applicazione principale (WMDMApp.exe).</span><span class="sxs-lookup"><span data-stu-id="4bbf9-116">In addition, it will create the progress helper DLL and the main application (WMDMApp.exe).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bbf9-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4bbf9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bbf9-118">**Applicazione desktop di esempio**</span><span class="sxs-lookup"><span data-stu-id="4bbf9-118">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




