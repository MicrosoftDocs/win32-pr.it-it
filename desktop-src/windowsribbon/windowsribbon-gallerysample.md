---
title: Esempio di raccolta
description: Questo esempio di codice illustra il markup e il codice necessari per usare i diversi tipi di controlli Raccolta inclusi nel framework Windows ribbon.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: ef776a8a1a8eadf9ee41cf9964066cc612a9f9a1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691750"
---
# <a name="gallery-sample"></a><span data-ttu-id="ca08a-103">Esempio di raccolta</span><span class="sxs-lookup"><span data-stu-id="ca08a-103">Gallery Sample</span></span>

<span data-ttu-id="ca08a-104">Questo esempio di codice illustra il markup e il codice necessari per usare i diversi tipi di controlli Raccolta inclusi nel framework Windows ribbon.</span><span class="sxs-lookup"><span data-stu-id="ca08a-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="ca08a-105">L'esempio include codice che può essere usato per popolare dinamicamente gli elementi nelle raccolte e gestire eventi speciali di anteprima della Raccolta che supportano l'interfaccia utente orientata ai risultati.</span><span class="sxs-lookup"><span data-stu-id="ca08a-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

- [<span data-ttu-id="ca08a-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ca08a-106">Usage</span></span>](#usage)
  - [<span data-ttu-id="ca08a-107">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca08a-107">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="ca08a-108">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca08a-108">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="ca08a-109">Supporto</span><span class="sxs-lookup"><span data-stu-id="ca08a-109">Support</span></span>](#support)
- [<span data-ttu-id="ca08a-110">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="ca08a-110">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="ca08a-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca08a-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="ca08a-112">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ca08a-112">Usage</span></span>

<span data-ttu-id="ca08a-113">Gli Windows di framework della barra multifunzione possono essere scaricati come progetti Microsoft Visual Studio autonomi dall'Area download [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o installati come parte di [Windows Software Development Kit (SDK).](https://developer.microsoft.com/windows/downloads/sdk-archive/)</span><span class="sxs-lookup"><span data-stu-id="ca08a-113">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="ca08a-114">Windows Software Development Kit (SDK) (percorso di installazione standard): %ProgramFiles% Microsoft SDK Windows numero di versione \\ \\ Esempi \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="ca08a-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="ca08a-115">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca08a-115">Building the Sample</span></span>

<span data-ttu-id="ca08a-116">Scaricare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="ca08a-116">Download the sample.</span></span>

<span data-ttu-id="ca08a-117">Installare l'SDK Windows per Windows 7 e aprire la finestra di comando dell'ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="ca08a-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="ca08a-118">Fare clic sul menu Start, quindi scegliere Tutti i programmi, Microsoft Windows SDK, quindi fare clic su CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="ca08a-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="ca08a-119">Per compilare l'esempio dalla finestra di comando dell'ambiente di compilazione, passare alla directory di origine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="ca08a-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="ca08a-120">Al prompt dei comandi digitare MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="ca08a-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="ca08a-121">Per compilare l'esempio in Microsoft Visual Studio, caricare il file della soluzione o del progetto dell'esempio e premere CTRL+MAIUSC+B.</span><span class="sxs-lookup"><span data-stu-id="ca08a-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="ca08a-122">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca08a-122">Running the Sample</span></span>

<span data-ttu-id="ca08a-123">Per eseguire l'esempio dalla finestra di comando dell'ambiente di compilazione, eseguire i file .exe nella cartella Bin Debug o Bin Release contenuta nella cartella \\ di origine \\ dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="ca08a-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="ca08a-124">Per eseguire l'esempio compilato con il debug in Visual Studio, premere F5.</span><span class="sxs-lookup"><span data-stu-id="ca08a-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="ca08a-125">Supporto</span><span class="sxs-lookup"><span data-stu-id="ca08a-125">Support</span></span>

<span data-ttu-id="ca08a-126">Il [Windows forum sullo sviluppo della](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) barra multifunzione è disponibile per discutere argomenti e porre domande relative allo sviluppo di applicazioni Windows ribbon.</span><span class="sxs-lookup"><span data-stu-id="ca08a-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="ca08a-127">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="ca08a-127">Minimum Requirements</span></span>



| <span data-ttu-id="ca08a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca08a-128">Requirement</span></span> | <span data-ttu-id="ca08a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ca08a-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca08a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca08a-130">Minimum supported client</span></span> | <span data-ttu-id="ca08a-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca08a-131">Windows 7</span></span><br/> <span data-ttu-id="ca08a-132">Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca08a-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="ca08a-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca08a-133">Minimum supported server</span></span> | <span data-ttu-id="ca08a-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca08a-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="ca08a-135">Windows Server 2008 con SP2 e aggiornamento della piattaforma [per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca08a-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="ca08a-136">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="ca08a-136">Windows SDK</span></span>              | <span data-ttu-id="ca08a-137">7.0</span><span class="sxs-lookup"><span data-stu-id="ca08a-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="ca08a-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ca08a-138">Visual Studio</span></span>            | <span data-ttu-id="ca08a-139">2008</span><span class="sxs-lookup"><span data-stu-id="ca08a-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="ca08a-140">File di intestazione e IDL</span><span class="sxs-lookup"><span data-stu-id="ca08a-140">Header and IDL files</span></span>     | <span data-ttu-id="ca08a-141">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="ca08a-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="ca08a-142">L'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di scegliere come destinazione le applicazioni della barra multifunzione Windows Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ca08a-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="ca08a-143">Gli aggiornamenti della piattaforma saranno disponibili per tutti i Windows Vista e Windows Server 2008 tramite Windows Update.</span><span class="sxs-lookup"><span data-stu-id="ca08a-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="ca08a-144">Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) possono fare in modo che Windows Update rilevi se l'aggiornamento richiesto è installato; In caso contrario, l Windows Update lo scariderà e lo installerà in background.</span><span class="sxs-lookup"><span data-stu-id="ca08a-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ca08a-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca08a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca08a-146">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="ca08a-146">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="ca08a-147">ComboBox</span><span class="sxs-lookup"><span data-stu-id="ca08a-147">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="ca08a-148">Raccolta a discesa</span><span class="sxs-lookup"><span data-stu-id="ca08a-148">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="ca08a-149">Raccolta nella barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="ca08a-149">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="ca08a-150">Raccolta pulsanti di divisione</span><span class="sxs-lookup"><span data-stu-id="ca08a-150">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="ca08a-151">Proprietà raccolta</span><span class="sxs-lookup"><span data-stu-id="ca08a-151">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





