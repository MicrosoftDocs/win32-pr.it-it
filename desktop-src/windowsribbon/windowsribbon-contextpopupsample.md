---
title: Esempio ContextPopup
description: Questo esempio di codice illustra il markup e il codice necessari per implementare un'applicazione della barra multifunzione di Windows con ContextPopups.
ms.assetid: f334dbfc-710a-4652-b914-a668ae36aecd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ff2f66b27c3fb244181a779718079b3f992b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301713"
---
# <a name="contextpopup-sample"></a><span data-ttu-id="31d92-103">Esempio ContextPopup</span><span class="sxs-lookup"><span data-stu-id="31d92-103">ContextPopup Sample</span></span>

<span data-ttu-id="31d92-104">Questo esempio di codice illustra il markup e il codice necessari per implementare un'applicazione della barra multifunzione di Windows con ContextPopups.</span><span class="sxs-lookup"><span data-stu-id="31d92-104">This code sample demonstrates the markup and code required to implement a Windows Ribbon application with ContextPopups.</span></span>

-   [<span data-ttu-id="31d92-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="31d92-105">Usage</span></span>](#usage)
    -   [<span data-ttu-id="31d92-106">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="31d92-106">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="31d92-107">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="31d92-107">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="31d92-108">Supporto</span><span class="sxs-lookup"><span data-stu-id="31d92-108">Support</span></span>](#support)
-   [<span data-ttu-id="31d92-109">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="31d92-109">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="31d92-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31d92-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="31d92-111">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="31d92-111">Usage</span></span>

<span data-ttu-id="31d92-112">L'esempio ContextPopup può essere scaricato come un progetto Microsoft Visual Studio autonomo dall' [area download Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) o installato come parte di [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="31d92-112">The ContextPopup Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="31d92-113">Area download Microsoft: [esempi della barra multifunzione di Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="31d92-113">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="31d92-114">Windows Software Development Kit (SDK) (percorso di installazione standard):% ProgramFiles% \\ Microsoft \\ SDK \\ \[ numero di versione Windows \] \\ esempi \\ WinUI \\ WindowsRibbon \\ ContextPopup</span><span class="sxs-lookup"><span data-stu-id="31d92-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\ContextPopup</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="31d92-115">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="31d92-115">Building the Sample</span></span>

<span data-ttu-id="31d92-116">Scaricare l'esempio nel disco rigido.</span><span class="sxs-lookup"><span data-stu-id="31d92-116">Download the sample to your hard disk.</span></span>

<span data-ttu-id="31d92-117">Installare la Windows SDK per Windows 7 e aprire la finestra di comando dell'ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="31d92-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="31d92-118">Fare clic sul menu Start, quindi scegliere Tutti i programmi, Microsoft Windows SDK, quindi fare clic su CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="31d92-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="31d92-119">Per compilare l'esempio dalla finestra di comando dell'ambiente di compilazione, passare alla directory di origine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="31d92-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="31d92-120">Al prompt dei comandi digitare MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="31d92-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="31d92-121">Per compilare l'esempio in Microsoft Visual Studio, caricare il file della soluzione o del progetto dell'esempio e premere CTRL+MAIUSC+B.</span><span class="sxs-lookup"><span data-stu-id="31d92-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="31d92-122">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="31d92-122">Running the Sample</span></span>

<span data-ttu-id="31d92-123">Per eseguire l'esempio dalla finestra di comando dell'ambiente di compilazione, eseguire i file con estensione exe nella \\ cartella bin debug o bin \\ Release contenuta nella cartella di origine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="31d92-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="31d92-124">Per eseguire l'esempio compilato con il debug in Visual Studio, premere F5.</span><span class="sxs-lookup"><span data-stu-id="31d92-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="31d92-125">Supporto</span><span class="sxs-lookup"><span data-stu-id="31d92-125">Support</span></span>

<span data-ttu-id="31d92-126">Il [Forum di sviluppo della barra multifunzione di Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) è disponibile per discutere argomenti e porre domande relative allo sviluppo di applicazioni della barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="31d92-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="31d92-127">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="31d92-127">Minimum Requirements</span></span>



| <span data-ttu-id="31d92-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="31d92-128">Requirement</span></span> | <span data-ttu-id="31d92-129">Valore</span><span class="sxs-lookup"><span data-stu-id="31d92-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31d92-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31d92-130">Minimum supported client</span></span> | <span data-ttu-id="31d92-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31d92-131">Windows 7</span></span><br/> <span data-ttu-id="31d92-132">Windows Vista con Service Pack 2 (SP2) e [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="31d92-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="31d92-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31d92-133">Minimum supported server</span></span> | <span data-ttu-id="31d92-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31d92-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="31d92-135">Windows Server 2008 con SP2 e [aggiornamento della piattaforma per Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="31d92-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="31d92-136">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="31d92-136">Windows SDK</span></span>              | <span data-ttu-id="31d92-137">7.0</span><span class="sxs-lookup"><span data-stu-id="31d92-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="31d92-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="31d92-138">Visual Studio</span></span>            | <span data-ttu-id="31d92-139">2008</span><span class="sxs-lookup"><span data-stu-id="31d92-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="31d92-140">File di intestazione e IDL</span><span class="sxs-lookup"><span data-stu-id="31d92-140">Header and IDL files</span></span>     | <span data-ttu-id="31d92-141">UIRibbon. h, UIRibbon. idl</span><span class="sxs-lookup"><span data-stu-id="31d92-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="31d92-142">L' [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l' [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di utilizzare applicazioni della barra multifunzione di Windows in Windows vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="31d92-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="31d92-143">Gli aggiornamenti della piattaforma saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update.</span><span class="sxs-lookup"><span data-stu-id="31d92-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="31d92-144">Le applicazioni di terze parti che richiedono l' [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l' [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) possono avere Windows Update rilevare se l'aggiornamento richiesto è installato; in caso contrario, Windows Update lo scaricherà e installerà in background.</span><span class="sxs-lookup"><span data-stu-id="31d92-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="31d92-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31d92-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31d92-146">Popup contesto</span><span class="sxs-lookup"><span data-stu-id="31d92-146">Context Popup</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





