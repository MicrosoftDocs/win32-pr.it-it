---
title: Esempio di DropDownColorPicker
description: Questo esempio di codice illustra il markup e il codice necessari per usare Windows controllo DropDownColorPicker della barra multifunzione.
ms.assetid: cc8e18a6-9ed5-47ca-a807-f50838821f14
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 0bb4cb91fdcd5450bd9be5ee70a8ca6c0fe253f6
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691690"
---
# <a name="dropdowncolorpicker-sample"></a><span data-ttu-id="c1904-103">Esempio di DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="c1904-103">DropDownColorPicker Sample</span></span>

<span data-ttu-id="c1904-104">Questo esempio di codice illustra il markup e il codice necessari per usare Windows controllo DropDownColorPicker della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c1904-104">This code sample demonstrates the markup and code required to use a Windows Ribbon DropDownColorPicker control.</span></span>

- [<span data-ttu-id="c1904-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="c1904-105">Usage</span></span>](#usage)
  - [<span data-ttu-id="c1904-106">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c1904-106">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="c1904-107">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c1904-107">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="c1904-108">Supporto</span><span class="sxs-lookup"><span data-stu-id="c1904-108">Support</span></span>](#support)
- [<span data-ttu-id="c1904-109">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="c1904-109">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="c1904-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1904-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="c1904-111">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="c1904-111">Usage</span></span>

<span data-ttu-id="c1904-112">Gli Windows di framework della barra multifunzione possono essere scaricati come progetti Microsoft Visual Studio autonomi dall'Area download [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o installati come parte di [Windows Software Development Kit (SDK).](https://developer.microsoft.com/windows/downloads/sdk-archive/)</span><span class="sxs-lookup"><span data-stu-id="c1904-112">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="c1904-113">Windows Software Development Kit (SDK) (percorso di installazione standard): %ProgramFiles% Microsoft SDK Windows numero di versione \\ \\ Esempi \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="c1904-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\DropDownColorPicker</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="c1904-114">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c1904-114">Building the Sample</span></span>

<span data-ttu-id="c1904-115">Scaricare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="c1904-115">Download the sample.</span></span>

<span data-ttu-id="c1904-116">Installare l'SDK Windows per Windows 7 e aprire la finestra di comando dell'ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="c1904-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="c1904-117">Fare clic sul menu Start, quindi scegliere Tutti i programmi, Microsoft Windows SDK, quindi fare clic su CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="c1904-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="c1904-118">Per compilare l'esempio dalla finestra di comando dell'ambiente di compilazione, passare alla directory di origine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="c1904-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="c1904-119">Al prompt dei comandi digitare MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="c1904-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="c1904-120">Per compilare l'esempio in Microsoft Visual Studio, caricare il file della soluzione o del progetto dell'esempio e premere CTRL+MAIUSC+B.</span><span class="sxs-lookup"><span data-stu-id="c1904-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="c1904-121">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c1904-121">Running the Sample</span></span>

<span data-ttu-id="c1904-122">Per eseguire l'esempio dalla finestra di comando dell'ambiente di compilazione, eseguire i file .exe nella cartella Bin Debug o Bin Release contenuta nella cartella \\ di origine \\ dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="c1904-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="c1904-123">Per eseguire l'esempio compilato con il debug in Visual Studio, premere F5.</span><span class="sxs-lookup"><span data-stu-id="c1904-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="c1904-124">Supporto</span><span class="sxs-lookup"><span data-stu-id="c1904-124">Support</span></span>

<span data-ttu-id="c1904-125">Il [Windows forum sullo sviluppo della](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) barra multifunzione è disponibile per discutere argomenti e porre domande relative allo sviluppo di applicazioni Windows ribbon.</span><span class="sxs-lookup"><span data-stu-id="c1904-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="c1904-126">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="c1904-126">Minimum Requirements</span></span>



| <span data-ttu-id="c1904-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1904-127">Requirement</span></span> | <span data-ttu-id="c1904-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c1904-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1904-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1904-129">Minimum supported client</span></span> | <span data-ttu-id="c1904-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1904-130">Windows 7</span></span><br/> <span data-ttu-id="c1904-131">Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1904-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="c1904-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1904-132">Minimum supported server</span></span> | <span data-ttu-id="c1904-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1904-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="c1904-134">Windows Server 2008 con SP2 e aggiornamento della piattaforma [per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1904-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="c1904-135">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c1904-135">Windows SDK</span></span>              | <span data-ttu-id="c1904-136">7.0</span><span class="sxs-lookup"><span data-stu-id="c1904-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="c1904-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c1904-137">Visual Studio</span></span>            | <span data-ttu-id="c1904-138">2008</span><span class="sxs-lookup"><span data-stu-id="c1904-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="c1904-139">File di intestazione e IDL</span><span class="sxs-lookup"><span data-stu-id="c1904-139">Header and IDL files</span></span>     | <span data-ttu-id="c1904-140">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="c1904-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="c1904-141">L'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di scegliere come destinazione le applicazioni della barra multifunzione Windows Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c1904-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="c1904-142">Gli aggiornamenti della piattaforma saranno disponibili per tutti i Windows Vista e Windows Server 2008 tramite Windows Update.</span><span class="sxs-lookup"><span data-stu-id="c1904-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="c1904-143">Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) possono fare in modo che Windows Update rilevi se l'aggiornamento richiesto è installato; In caso contrario, l Windows Update lo scariderà e lo installerà in background.</span><span class="sxs-lookup"><span data-stu-id="c1904-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c1904-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1904-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1904-145">Elenco a discesa Selezione colori</span><span class="sxs-lookup"><span data-stu-id="c1904-145">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="c1904-146">Selezione colori proprietà</span><span class="sxs-lookup"><span data-stu-id="c1904-146">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 





