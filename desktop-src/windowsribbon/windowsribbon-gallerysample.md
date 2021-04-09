---
title: Esempio di raccolta
description: Questo esempio di codice illustra il markup e il codice necessari per usare i diversi tipi di controlli della raccolta inclusi nel framework della barra multifunzione di Windows.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aacc52081fbcd2b6b58fd4c2439894705880d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119247"
---
# <a name="gallery-sample"></a><span data-ttu-id="a7d0f-103">Esempio di raccolta</span><span class="sxs-lookup"><span data-stu-id="a7d0f-103">Gallery Sample</span></span>

<span data-ttu-id="a7d0f-104">Questo esempio di codice illustra il markup e il codice necessari per usare i diversi tipi di controlli della raccolta inclusi nel framework della barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="a7d0f-105">Nell'esempio è incluso il codice che può essere usato per popolare dinamicamente gli elementi nelle raccolte e per gestire eventi di anteprima della raccolta speciali che supportano l'interfaccia utente orientata ai risultati.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

-   [<span data-ttu-id="a7d0f-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a7d0f-106">Usage</span></span>](#usage)
    -   [<span data-ttu-id="a7d0f-107">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a7d0f-107">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="a7d0f-108">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a7d0f-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="a7d0f-109">Supporto</span><span class="sxs-lookup"><span data-stu-id="a7d0f-109">Support</span></span>](#support)
-   [<span data-ttu-id="a7d0f-110">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="a7d0f-110">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="a7d0f-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7d0f-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="a7d0f-112">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a7d0f-112">Usage</span></span>

<span data-ttu-id="a7d0f-113">L'esempio di raccolta può essere scaricato come un progetto di Microsoft Visual Studio autonomo dall' [area download Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) o installato come parte di [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7d0f-113">The Gallery Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="a7d0f-114">Area download Microsoft: [esempi della barra multifunzione di Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="a7d0f-114">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="a7d0f-115">Windows Software Development Kit (SDK) (percorso di installazione standard):% ProgramFiles% \\ Microsoft \\ SDK \\ \[ numero di versione Windows \] \\ esempi \\ WinUI \\ \\ raccolta WindowsRibbon</span><span class="sxs-lookup"><span data-stu-id="a7d0f-115">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="a7d0f-116">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a7d0f-116">Building the Sample</span></span>

<span data-ttu-id="a7d0f-117">Scaricare l'esempio nel disco rigido.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-117">Download the sample to your hard disk.</span></span>

<span data-ttu-id="a7d0f-118">Installare la Windows SDK per Windows 7 e aprire la finestra di comando dell'ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-118">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="a7d0f-119">Fare clic sul menu Start, quindi scegliere Tutti i programmi, Microsoft Windows SDK, quindi fare clic su CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-119">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="a7d0f-120">Per compilare l'esempio dalla finestra di comando dell'ambiente di compilazione, passare alla directory di origine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-120">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="a7d0f-121">Al prompt dei comandi digitare MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-121">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="a7d0f-122">Per compilare l'esempio in Microsoft Visual Studio, caricare il file della soluzione o del progetto dell'esempio e premere CTRL+MAIUSC+B.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-122">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="a7d0f-123">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a7d0f-123">Running the Sample</span></span>

<span data-ttu-id="a7d0f-124">Per eseguire l'esempio dalla finestra di comando dell'ambiente di compilazione, eseguire i file con estensione exe nella \\ cartella bin debug o bin \\ Release contenuta nella cartella di origine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-124">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="a7d0f-125">Per eseguire l'esempio compilato con il debug in Visual Studio, premere F5.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-125">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="a7d0f-126">Supporto</span><span class="sxs-lookup"><span data-stu-id="a7d0f-126">Support</span></span>

<span data-ttu-id="a7d0f-127">Il [Forum di sviluppo della barra multifunzione di Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) è disponibile per discutere argomenti e porre domande relative allo sviluppo di applicazioni della barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-127">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="a7d0f-128">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="a7d0f-128">Minimum Requirements</span></span>



| <span data-ttu-id="a7d0f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7d0f-129">Requirement</span></span> | <span data-ttu-id="a7d0f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="a7d0f-130">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d0f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7d0f-131">Minimum supported client</span></span> | <span data-ttu-id="a7d0f-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a7d0f-132">Windows 7</span></span><br/> <span data-ttu-id="a7d0f-133">Windows Vista con Service Pack 2 (SP2) e [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7d0f-133">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="a7d0f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7d0f-134">Minimum supported server</span></span> | <span data-ttu-id="a7d0f-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7d0f-135">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="a7d0f-136">Windows Server 2008 con SP2 e [aggiornamento della piattaforma per Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7d0f-136">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="a7d0f-137">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a7d0f-137">Windows SDK</span></span>              | <span data-ttu-id="a7d0f-138">7.0</span><span class="sxs-lookup"><span data-stu-id="a7d0f-138">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="a7d0f-139">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a7d0f-139">Visual Studio</span></span>            | <span data-ttu-id="a7d0f-140">2008</span><span class="sxs-lookup"><span data-stu-id="a7d0f-140">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="a7d0f-141">File di intestazione e IDL</span><span class="sxs-lookup"><span data-stu-id="a7d0f-141">Header and IDL files</span></span>     | <span data-ttu-id="a7d0f-142">UIRibbon. h, UIRibbon. idl</span><span class="sxs-lookup"><span data-stu-id="a7d0f-142">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="a7d0f-143">L' [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l' [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di utilizzare applicazioni della barra multifunzione di Windows in Windows vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-143">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a7d0f-144">Gli aggiornamenti della piattaforma saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-144">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="a7d0f-145">Le applicazioni di terze parti che richiedono l' [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l' [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) possono avere Windows Update rilevare se l'aggiornamento richiesto è installato; in caso contrario, Windows Update lo scaricherà e installerà in background.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-145">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a7d0f-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7d0f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7d0f-147">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="a7d0f-147">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="a7d0f-148">ComboBox</span><span class="sxs-lookup"><span data-stu-id="a7d0f-148">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="a7d0f-149">Raccolta a discesa</span><span class="sxs-lookup"><span data-stu-id="a7d0f-149">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="a7d0f-150">Raccolta della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="a7d0f-150">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="a7d0f-151">Raccolta di pulsanti di suddivisione</span><span class="sxs-lookup"><span data-stu-id="a7d0f-151">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="a7d0f-152">Proprietà della raccolta</span><span class="sxs-lookup"><span data-stu-id="a7d0f-152">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





