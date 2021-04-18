---
description: VSDiagview e VSSAgent sono strumenti che è possibile usare per risolvere i problemi relativi alle applicazioni VSS. Si noti che questi strumenti sono inclusi in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Uso della diagnostica VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307180"
---
# <a name="using-vss-diagnostics"></a><span data-ttu-id="02044-103">Uso della diagnostica VSS</span><span class="sxs-lookup"><span data-stu-id="02044-103">Using VSS Diagnostics</span></span>

<span data-ttu-id="02044-104">VSDiagview e VSSAgent sono strumenti che è possibile usare per risolvere i problemi relativi alle applicazioni VSS.</span><span class="sxs-lookup"><span data-stu-id="02044-104">Vsdiagview and Vssagent are tools that you can use to troubleshoot VSS applications.</span></span>

> [!Note]  
> <span data-ttu-id="02044-105">Questi strumenti sono inclusi in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="02044-105">These tools are included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="02044-106">È possibile scaricare il Windows SDK da [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="02044-106">You can download the Windows SDK from [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx).</span></span>

 

<span data-ttu-id="02044-107">Nell'installazione di Windows SDK, questi strumenti sono disponibili in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (per Windows a 64 bit) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (per windows a 32 bit).</span><span class="sxs-lookup"><span data-stu-id="02044-107">In the Windows SDK installation, these tools can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="gathering-data"></a><span data-ttu-id="02044-108">Raccolta dati</span><span class="sxs-lookup"><span data-stu-id="02044-108">Gathering Data</span></span>

<span data-ttu-id="02044-109">È possibile raccogliere dati tramite il comando VSSAgent.</span><span class="sxs-lookup"><span data-stu-id="02044-109">You can gather data by using the Vssagent command.</span></span>

<span data-ttu-id="02044-110">**Per raccogliere dati mediante VSSAgent**</span><span class="sxs-lookup"><span data-stu-id="02044-110">**To gather data using Vssagent**</span></span>

1.  <span data-ttu-id="02044-111">Per raccogliere dati dalla riga di comando, usare il comando VSSAgent come segue:</span><span class="sxs-lookup"><span data-stu-id="02044-111">To gather data from the command line, use the Vssagent command as follows:</span></span>

    <span data-ttu-id="02044-112">**VSSAgent-raccoglie** *xmlFileName \* \* *. XML**</span><span class="sxs-lookup"><span data-stu-id="02044-112">**vssagent -gather** *XmlFileName\*\*\*.xml*\*</span></span>

2.  <span data-ttu-id="02044-113">Per visualizzare il file di output, vedere la sezione seguente relativa alla visualizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="02044-113">To view the output file, see the following Viewing Data section.</span></span>

## <a name="viewing-data"></a><span data-ttu-id="02044-114">Visualizzazione dei dati</span><span class="sxs-lookup"><span data-stu-id="02044-114">Viewing Data</span></span>

<span data-ttu-id="02044-115">L'applicazione VSDiagview può essere usata per visualizzare i dati raccolti tramite il comando VSSAgent.</span><span class="sxs-lookup"><span data-stu-id="02044-115">The Vsdiagview application can be used to view data that was gathered by using the Vssagent command.</span></span> <span data-ttu-id="02044-116">VSDiagview Visualizza le informazioni seguenti sul computer:</span><span class="sxs-lookup"><span data-stu-id="02044-116">Vsdiagview displays the following information about the computer:</span></span>

-   <span data-ttu-id="02044-117">Informazioni sul computer, ad esempio la versione del sistema operativo, la memoria totale disponibile e la velocità della CPU</span><span class="sxs-lookup"><span data-stu-id="02044-117">Information about the computer, such as the operating system version, total available memory, and CPU speed</span></span>
-   <span data-ttu-id="02044-118">I nomi e i numeri di versione dei file binari VSS</span><span class="sxs-lookup"><span data-stu-id="02044-118">The names and version numbers of the VSS binaries</span></span>
-   <span data-ttu-id="02044-119">I nomi e le proprietà dei dispositivi disco e volume</span><span class="sxs-lookup"><span data-stu-id="02044-119">The names and properties of the disk and volume devices</span></span>
-   <span data-ttu-id="02044-120">I nomi e le proprietà di qualsiasi applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="02044-120">The names and properties of any COM+ applications</span></span>
-   <span data-ttu-id="02044-121">Nomi dei registri eventi che possono essere utilizzati per la diagnosi dei problemi del servizio Copia Shadow del volume</span><span class="sxs-lookup"><span data-stu-id="02044-121">The names of event logs that can be used for diagnosing VSS problems</span></span>
-   <span data-ttu-id="02044-122">I nomi dei writer VSS e degli eventi gestiti</span><span class="sxs-lookup"><span data-stu-id="02044-122">The names of any VSS writers and the events that they handle</span></span>
-   <span data-ttu-id="02044-123">Informazioni su altri file del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="02044-123">Information about other operating system files</span></span>

<span data-ttu-id="02044-124">**Per visualizzare i dati tramite VSDiagview**</span><span class="sxs-lookup"><span data-stu-id="02044-124">**To view data using Vsdiagview**</span></span>

1.  <span data-ttu-id="02044-125">Scegliere **Apri** dal menu file per cercare un file.</span><span class="sxs-lookup"><span data-stu-id="02044-125">In the File menu, choose **Open** to browse for a file.</span></span> <span data-ttu-id="02044-126">(Il percorso predefinito è C: \\ vssdiag).</span><span class="sxs-lookup"><span data-stu-id="02044-126">(The default location is C:\\vssdiag.)</span></span>
2.  <span data-ttu-id="02044-127">Fare clic su **Apri** per visualizzare i dati.</span><span class="sxs-lookup"><span data-stu-id="02044-127">Click **Open** to view the data.</span></span>

 

 



