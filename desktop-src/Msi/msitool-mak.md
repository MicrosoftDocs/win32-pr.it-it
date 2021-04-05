---
description: MSITool. MAK è un makefile che è possibile usare per compilare strumenti e azioni personalizzate.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: MSITool. MAK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131307"
---
# <a name="msitoolmak"></a><span data-ttu-id="02487-103">MSITool. MAK</span><span class="sxs-lookup"><span data-stu-id="02487-103">Msitool.mak</span></span>

<span data-ttu-id="02487-104">MSITool. MAK è un makefile che è possibile usare per compilare strumenti e azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="02487-104">Msitool.mak is a makefile that you can use to build tools and custom actions.</span></span> <span data-ttu-id="02487-105">Può essere usato con Visual C++ versione 4,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="02487-105">It may be used with Visual C++ version 4.0 or later.</span></span> <span data-ttu-id="02487-106">Per ulteriori informazioni, vedere il file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="02487-106">For more information, see the header file.</span></span> <span data-ttu-id="02487-107">È necessario definire un set di valori prima di includere questo file.</span><span class="sxs-lookup"><span data-stu-id="02487-107">It requires a set of values to be defined before including this file.</span></span> <span data-ttu-id="02487-108">In genere, gli sviluppatori li inseriscono all'inizio di. cpp, ifdef deve essere ignorato dal compilatore C.</span><span class="sxs-lookup"><span data-stu-id="02487-108">Typically developers put those at the start of the .cpp, ifdef'd to be skipped by the C compiler.</span></span> <span data-ttu-id="02487-109">Allo stesso modo, le risorse vengono aggiunte alla fine del file con estensione cpp.</span><span class="sxs-lookup"><span data-stu-id="02487-109">Likewise resources are added to the end of the .cpp file.</span></span> <span data-ttu-id="02487-110">Per informazioni dettagliate, vedere esempi.</span><span class="sxs-lookup"><span data-stu-id="02487-110">See samples for details.</span></span>

<span data-ttu-id="02487-111">VCBIN può essere definito nella directory in cui vengono trovati gli strumenti di Visual C++ o il makefile USA MSVCDIR e MSDEVDIR.</span><span class="sxs-lookup"><span data-stu-id="02487-111">VCBIN can be defined to the directory where the Visual C++ tools are found or the makefile uses MSVCDIR and MSDEVDIR.</span></span> <span data-ttu-id="02487-112">Se non sono definiti, non specifica un percorso, supponendo che gli strumenti si trovino nel percorso.</span><span class="sxs-lookup"><span data-stu-id="02487-112">If those are not defined, it does not specify a location, assuming the tools to be on the PATH.</span></span> <span data-ttu-id="02487-113">Un problema con le variabili di ambiente in Visual C++ versione 5,0 è che se non sono presenti entrambi i percorsi, il linker non è in grado di trovare Msdis100.dll.</span><span class="sxs-lookup"><span data-stu-id="02487-113">An issue with the environment variables in Visual C++ version 5.0 is that if both are not on you path, the linker cannot find Msdis100.dll.</span></span> <span data-ttu-id="02487-114">Se lo si copia da MSDEVDIR a MSVCDIR, funziona.</span><span class="sxs-lookup"><span data-stu-id="02487-114">If you copy that from MSDEVDIR to MSVCDIR, it works.</span></span> <span data-ttu-id="02487-115">L'altra opzione consiste nel copiare Msdis100.dll e Rc.exe e Rcdll.dll in MSVCDIR e impostare VCBIN su tale.</span><span class="sxs-lookup"><span data-stu-id="02487-115">The other option is to copy Msdis100.dll and Rc.exe and Rcdll.dll to MSVCDIR, and set VCBIN to that.</span></span>

<span data-ttu-id="02487-116">Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="02487-116">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02487-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02487-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02487-118">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="02487-118">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="02487-119">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="02487-119">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



