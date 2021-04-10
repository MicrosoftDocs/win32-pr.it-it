---
title: Esempio HTMLEditRibbon
description: Questo esempio di codice mostra il markup e il codice necessari per eseguire la migrazione di un'applicazione Microsoft Foundation Classes (MFC) esistente per usare la barra multifunzione di Windows.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f98d4d76508b812d86a4dab38f8dcec96dadc52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048077"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="7181f-103">Esempio HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="7181f-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="7181f-104">Questo esempio di codice mostra il markup e il codice necessari per eseguire la migrazione di un'applicazione Microsoft Foundation Classes (MFC) esistente per usare la barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="7181f-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="7181f-105">È stato creato prendendo l'applicazione di esempio MFC HTMLEdit esistente e modificando il codice e le risorse per usare la barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="7181f-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

-   [<span data-ttu-id="7181f-106">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="7181f-106">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="7181f-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="7181f-107">Usage</span></span>](#usage)
    -   [<span data-ttu-id="7181f-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="7181f-108">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="7181f-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="7181f-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="7181f-110">Supporto</span><span class="sxs-lookup"><span data-stu-id="7181f-110">Support</span></span>](#support)
-   [<span data-ttu-id="7181f-111">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="7181f-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="7181f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7181f-112">Remarks</span></span>

<span data-ttu-id="7181f-113">Per l'esempio MFC, vedere [esempio HTMLEdit: esegue il wrapping del controllo di modifica MSHTML di Internet Explorer](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="7181f-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="7181f-114">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="7181f-114">Usage</span></span>

<span data-ttu-id="7181f-115">L'esempio HTMLEditRibbon può essere scaricato come un progetto Microsoft Visual Studio autonomo dall' [area download Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) o installato come parte di [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7181f-115">The HTMLEditRibbon Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="7181f-116">Area download Microsoft: [esempi della barra multifunzione di Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="7181f-116">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="7181f-117">Windows Software Development Kit (SDK) (percorso di installazione standard):% ProgramFiles% \\ Microsoft \\ SDK \\ \[ numero di versione Windows \] \\ esempi \\ WinUI \\ WindowsRibbon \\ HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="7181f-117">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="7181f-118">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="7181f-118">Building the Sample</span></span>

<span data-ttu-id="7181f-119">Scaricare l'esempio nel disco rigido.</span><span class="sxs-lookup"><span data-stu-id="7181f-119">Download the sample to your hard disk.</span></span>

<span data-ttu-id="7181f-120">Installare la Windows SDK per Windows 7 e aprire la finestra di comando dell'ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="7181f-120">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="7181f-121">Fare clic sul menu Start, quindi scegliere Tutti i programmi, Microsoft Windows SDK, quindi fare clic su CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="7181f-121">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="7181f-122">Per compilare l'esempio dalla finestra di comando dell'ambiente di compilazione, passare alla directory di origine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="7181f-122">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="7181f-123">Al prompt dei comandi digitare MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="7181f-123">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="7181f-124">Per compilare l'esempio in Microsoft Visual Studio, caricare il file della soluzione o del progetto dell'esempio e premere CTRL+MAIUSC+B.</span><span class="sxs-lookup"><span data-stu-id="7181f-124">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="7181f-125">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="7181f-125">Running the Sample</span></span>

<span data-ttu-id="7181f-126">Per eseguire l'esempio dalla finestra di comando dell'ambiente di compilazione, eseguire i file con estensione exe nella \\ cartella bin debug o bin \\ Release contenuta nella cartella di origine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="7181f-126">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="7181f-127">Per eseguire l'esempio compilato con il debug in Visual Studio, premere F5.</span><span class="sxs-lookup"><span data-stu-id="7181f-127">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="7181f-128">Supporto</span><span class="sxs-lookup"><span data-stu-id="7181f-128">Support</span></span>

<span data-ttu-id="7181f-129">Il [Forum di sviluppo della barra multifunzione di Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) è disponibile per discutere argomenti e porre domande relative allo sviluppo di applicazioni della barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="7181f-129">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="7181f-130">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="7181f-130">Minimum Requirements</span></span>



| <span data-ttu-id="7181f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7181f-131">Requirement</span></span> | <span data-ttu-id="7181f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="7181f-132">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7181f-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7181f-133">Minimum supported client</span></span> | <span data-ttu-id="7181f-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7181f-134">Windows 7</span></span><br/> <span data-ttu-id="7181f-135">Windows Vista con Service Pack 2 (SP2) e [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="7181f-135">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="7181f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7181f-136">Minimum supported server</span></span> | <span data-ttu-id="7181f-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7181f-137">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="7181f-138">Windows Server 2008 con SP2 e [aggiornamento della piattaforma per Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="7181f-138">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="7181f-139">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7181f-139">Windows SDK</span></span>              | <span data-ttu-id="7181f-140">7.0</span><span class="sxs-lookup"><span data-stu-id="7181f-140">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="7181f-141">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7181f-141">Visual Studio</span></span>            | <span data-ttu-id="7181f-142">2008</span><span class="sxs-lookup"><span data-stu-id="7181f-142">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="7181f-143">File di intestazione e IDL</span><span class="sxs-lookup"><span data-stu-id="7181f-143">Header and IDL files</span></span>     | <span data-ttu-id="7181f-144">UIRibbon. h, UIRibbon. idl</span><span class="sxs-lookup"><span data-stu-id="7181f-144">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="7181f-145">L' [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l' [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di utilizzare applicazioni della barra multifunzione di Windows in Windows vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7181f-145">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="7181f-146">Gli aggiornamenti della piattaforma saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update.</span><span class="sxs-lookup"><span data-stu-id="7181f-146">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="7181f-147">Le applicazioni di terze parti che richiedono l' [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l' [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) possono avere Windows Update rilevare se l'aggiornamento richiesto è installato; in caso contrario, Windows Update lo scaricherà e installerà in background.</span><span class="sxs-lookup"><span data-stu-id="7181f-147">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





