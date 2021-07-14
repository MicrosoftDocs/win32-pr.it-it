---
title: Esempio di HTMLEditRibbon
description: Questo esempio di codice illustra il markup e il codice necessari per eseguire la migrazione di un'applicazione Microsoft Foundation Classes (MFC) esistente per usare la barra Windows multifunzione.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: cfe75d13a69e0122766e51a00bcb1b15d52eab4e
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691710"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="d53f3-103">Esempio di HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="d53f3-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="d53f3-104">Questo esempio di codice illustra il markup e il codice necessari per eseguire la migrazione di un'applicazione Microsoft Foundation Classes (MFC) esistente per usare la barra Windows multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d53f3-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="d53f3-105">È stato creato prendendo l'applicazione di esempio HTMLEdit MFC esistente e modificandone il codice e le risorse per usare la barra Windows multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d53f3-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

- [<span data-ttu-id="d53f3-106">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="d53f3-106">Remarks</span></span>](#remarks)
- [<span data-ttu-id="d53f3-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d53f3-107">Usage</span></span>](#usage)
  - [<span data-ttu-id="d53f3-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="d53f3-108">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="d53f3-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="d53f3-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="d53f3-110">Supporto</span><span class="sxs-lookup"><span data-stu-id="d53f3-110">Support</span></span>](#support)
- [<span data-ttu-id="d53f3-111">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="d53f3-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="d53f3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d53f3-112">Remarks</span></span>

<span data-ttu-id="d53f3-113">Per l'esempio MFC, vedere [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="d53f3-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="d53f3-114">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d53f3-114">Usage</span></span>

<span data-ttu-id="d53f3-115">Gli Windows di framework della barra multifunzione possono essere scaricati come progetti Microsoft Visual Studio autonomi dall'Area download [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o installati come parte di [Windows Software Development Kit (SDK).](https://developer.microsoft.com/windows/downloads/sdk-archive/)</span><span class="sxs-lookup"><span data-stu-id="d53f3-115">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="d53f3-116">Windows Software Development Kit (SDK) (percorso di installazione standard): %ProgramFiles% Microsoft SDK Windows numero di versione \\ \\ Esempi \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="d53f3-116">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="d53f3-117">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="d53f3-117">Building the Sample</span></span>

<span data-ttu-id="d53f3-118">Scaricare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="d53f3-118">Download the sample.</span></span>

<span data-ttu-id="d53f3-119">Installare l'SDK Windows per Windows 7 e aprire la finestra di comando dell'ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="d53f3-119">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="d53f3-120">Fare clic sul menu Start, quindi scegliere Tutti i programmi, Microsoft Windows SDK, quindi fare clic su CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="d53f3-120">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="d53f3-121">Per compilare l'esempio dalla finestra di comando dell'ambiente di compilazione, passare alla directory di origine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="d53f3-121">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="d53f3-122">Al prompt dei comandi digitare MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="d53f3-122">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="d53f3-123">Per compilare l'esempio in Microsoft Visual Studio, caricare il file della soluzione o del progetto dell'esempio e premere CTRL+MAIUSC+B.</span><span class="sxs-lookup"><span data-stu-id="d53f3-123">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="d53f3-124">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="d53f3-124">Running the Sample</span></span>

<span data-ttu-id="d53f3-125">Per eseguire l'esempio dalla finestra di comando dell'ambiente di compilazione, eseguire i file .exe nella cartella Bin Debug o Bin Release contenuta nella cartella \\ di origine \\ dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="d53f3-125">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="d53f3-126">Per eseguire l'esempio compilato con il debug in Visual Studio, premere F5.</span><span class="sxs-lookup"><span data-stu-id="d53f3-126">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="d53f3-127">Supporto</span><span class="sxs-lookup"><span data-stu-id="d53f3-127">Support</span></span>

<span data-ttu-id="d53f3-128">Il [Windows forum sullo sviluppo della](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) barra multifunzione è disponibile per discutere argomenti e porre domande relative allo sviluppo di applicazioni Windows ribbon.</span><span class="sxs-lookup"><span data-stu-id="d53f3-128">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="d53f3-129">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="d53f3-129">Minimum Requirements</span></span>



| <span data-ttu-id="d53f3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d53f3-130">Requirement</span></span> | <span data-ttu-id="d53f3-131">Valore</span><span class="sxs-lookup"><span data-stu-id="d53f3-131">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d53f3-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d53f3-132">Minimum supported client</span></span> | <span data-ttu-id="d53f3-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d53f3-133">Windows 7</span></span><br/> <span data-ttu-id="d53f3-134">Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="d53f3-134">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="d53f3-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d53f3-135">Minimum supported server</span></span> | <span data-ttu-id="d53f3-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d53f3-136">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="d53f3-137">Windows Server 2008 con SP2 e aggiornamento della piattaforma [per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="d53f3-137">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="d53f3-138">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d53f3-138">Windows SDK</span></span>              | <span data-ttu-id="d53f3-139">7.0</span><span class="sxs-lookup"><span data-stu-id="d53f3-139">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="d53f3-140">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d53f3-140">Visual Studio</span></span>            | <span data-ttu-id="d53f3-141">2008</span><span class="sxs-lookup"><span data-stu-id="d53f3-141">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="d53f3-142">File di intestazione e IDL</span><span class="sxs-lookup"><span data-stu-id="d53f3-142">Header and IDL files</span></span>     | <span data-ttu-id="d53f3-143">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="d53f3-143">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="d53f3-144">L'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di scegliere come destinazione le applicazioni della barra multifunzione Windows Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d53f3-144">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="d53f3-145">Gli aggiornamenti della piattaforma saranno disponibili per tutti i Windows Vista e Windows Server 2008 tramite Windows Update.</span><span class="sxs-lookup"><span data-stu-id="d53f3-145">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="d53f3-146">Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) possono fare in modo che Windows Update rilevi se l'aggiornamento richiesto è installato; In caso contrario, l Windows Update lo scariderà e lo installerà in background.</span><span class="sxs-lookup"><span data-stu-id="d53f3-146">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





