---
title: Supporto di immagini personalizzate per i dispositivi
description: Supporto di immagini personalizzate per i dispositivi
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Windows Media Player, supporto immagini personalizzate per i dispositivi
- Windows Media Player, supporto immagini per i dispositivi
- supporto per immagini personalizzate del dispositivo
- supporto di immagini personalizzate per i dispositivi
- supporto delle immagini per i dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300064"
---
# <a name="custom-image-support-for-devices"></a><span data-ttu-id="6c79e-108">Supporto di immagini personalizzate per i dispositivi</span><span class="sxs-lookup"><span data-stu-id="6c79e-108">Custom Image Support for Devices</span></span>

> [!Note]  
> <span data-ttu-id="6c79e-109">In questa sezione viene documentata una funzionalità di Windows Media Player 10 disponibile quando si utilizza il sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6c79e-109">This section documents a feature of Windows Media Player 10 that is available when using the Windows XP operating system.</span></span> <span data-ttu-id="6c79e-110">Potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6c79e-110">It may be unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6c79e-111">I produttori di dispositivi possono fornire due file di immagine speciali per personalizzare la modalità di rappresentazione di un dispositivo nell'interfaccia utente di Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="6c79e-111">Device manufacturers can provide two special image files to customize the way a device is represented in the Windows Media Player 10 user interface.</span></span> <span data-ttu-id="6c79e-112">Questi due file sono:</span><span class="sxs-lookup"><span data-stu-id="6c79e-112">These two files are:</span></span>

-   <span data-ttu-id="6c79e-113">Devicon. fil.</span><span class="sxs-lookup"><span data-stu-id="6c79e-113">DevIcon.fil.</span></span> <span data-ttu-id="6c79e-114">Un file di formato dell'icona Windows che rappresenta l'hardware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c79e-114">A Windows icon format file that represents the device hardware.</span></span> <span data-ttu-id="6c79e-115">Questa immagine viene visualizzata in Windows Media Player 10 in qualsiasi punto in cui viene usata un'icona per rappresentare un dispositivo, ad esempio l'elenco dei dispositivi nella funzionalità di **sincronizzazione** .</span><span class="sxs-lookup"><span data-stu-id="6c79e-115">This image displays in Windows Media Player 10 anywhere an icon is used to represent a device, such as the device list in the **Sync** feature.</span></span>
-   <span data-ttu-id="6c79e-116">Devlogo. fil.</span><span class="sxs-lookup"><span data-stu-id="6c79e-116">DevLogo.fil.</span></span> <span data-ttu-id="6c79e-117">Un file di formato PNG che rappresenta il logo aziendale del produttore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c79e-117">A PNG format file that represents the corporate logo of the device manufacturer.</span></span> <span data-ttu-id="6c79e-118">Questa immagine viene visualizzata in Windows Media Player 10 ovunque viene utilizzata la personalizzazione aziendale, ad esempio la finestra di dialogo **Configurazione dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="6c79e-118">This image displays in Windows Media Player 10 anywhere corporate branding is used, such as the **Device Setup** dialog box.</span></span>

## <a name="general-guidelines-for-images"></a><span data-ttu-id="6c79e-119">Linee guida generali per le immagini</span><span class="sxs-lookup"><span data-stu-id="6c79e-119">General Guidelines for Images</span></span>

<span data-ttu-id="6c79e-120">Le linee guida seguenti si applicano al supporto di immagini personalizzate in generale:</span><span class="sxs-lookup"><span data-stu-id="6c79e-120">The following guidelines apply to custom image support in general:</span></span>

-   <span data-ttu-id="6c79e-121">Questa funzionalità è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="6c79e-121">This feature is optional.</span></span> <span data-ttu-id="6c79e-122">I dispositivi che non forniscono immagini verranno rappresentati da immagini predefinite.</span><span class="sxs-lookup"><span data-stu-id="6c79e-122">Devices that do not supply images will be represented by default images.</span></span>
-   <span data-ttu-id="6c79e-123">Questa funzionalità è supportata solo per i dispositivi abilitati per MTP.</span><span class="sxs-lookup"><span data-stu-id="6c79e-123">This feature is supported for MTP-enabled devices only.</span></span>
-   <span data-ttu-id="6c79e-124">Per evitare modifiche ai file, è consigliabile archiviare i file di immagine nel firmware o in un supporto di archiviazione protetto, non con i file creati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6c79e-124">To prevent changes to the files, it is recommended that the image files be stored in firmware or a protected storage medium, not with user-created files.</span></span>
-   <span data-ttu-id="6c79e-125">I file non devono essere restituiti a Windows Media Gestione dispositivi client che enumerano l'archiviazione radice del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c79e-125">The files should not be returned to Windows Media Device Manager clients that enumerate the root storage of the device.</span></span> <span data-ttu-id="6c79e-126">Inoltre, l'eliminazione, lo stato di trasferimento o la ridenominazione dei file dovrebbe avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6c79e-126">Also, deleting, moving, or renaming the files should fail.</span></span>
-   <span data-ttu-id="6c79e-127">Se il dispositivo fornisce più di un supporto di archiviazione, il dispositivo deve restituire i file di immagine in risposta alle richieste di apertura dei file da qualsiasi supporto.</span><span class="sxs-lookup"><span data-stu-id="6c79e-127">If the device provides more than one storage medium, the device should return the image files in response to file open requests from any medium.</span></span> <span data-ttu-id="6c79e-128">È possibile che vengano restituite icone del dispositivo diverse da ogni supporto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6c79e-128">Different device icons may be returned from each storage medium.</span></span>
-   <span data-ttu-id="6c79e-129">Per i client Windows Media Gestione dispositivi 1,2 abilitati, queste immagini avranno la precedenza sulle proprietà delle icone fornite dai meccanismi di installazione di Windows, ad esempio le proprietà dei nodi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c79e-129">For Windows Media Device Manager 1.2-enabled clients, these images will take precedence over icon properties supplied by Windows setup mechanisms, such as device node properties.</span></span>
-   <span data-ttu-id="6c79e-130">Le immagini non devono contenere informazioni che richiedono la localizzazione.</span><span class="sxs-lookup"><span data-stu-id="6c79e-130">The images must not contain any information that requires localization.</span></span>
-   <span data-ttu-id="6c79e-131">Per i dispositivi multifunzione, solo le funzionalità di riproduzione musica di Windows XP utilizzeranno tali immagini.</span><span class="sxs-lookup"><span data-stu-id="6c79e-131">For multi-function devices, only the music playback features of Windows XP will use these images.</span></span>

## <a name="creating-the-device-icon-image"></a><span data-ttu-id="6c79e-132">Creazione dell'immagine dell'icona del dispositivo</span><span class="sxs-lookup"><span data-stu-id="6c79e-132">Creating the Device Icon Image</span></span>

<span data-ttu-id="6c79e-133">Il file di immagine dell'icona del dispositivo, devicon. fil, deve contenere un file nel formato dell'icona di Windows.</span><span class="sxs-lookup"><span data-stu-id="6c79e-133">The device icon image file, DevIcon.fil, must contain a file in Windows icon format.</span></span> <span data-ttu-id="6c79e-134">[Nelle icone degli articoli di MSDN in Win32](/previous-versions/ms997538(v=msdn.10)) viene descritto come creare un file di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="6c79e-134">The MSDN article [Icons in Win32](/previous-versions/ms997538(v=msdn.10)) describes how to create such a file.</span></span> <span data-ttu-id="6c79e-135">L'articolo di MSDN [creazione di icone di Windows XP](/previous-versions/ms997636(v=msdn.10)) offre linee guida di stile per le icone di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6c79e-135">The MSDN article [Creating Windows XP Icons](/previous-versions/ms997636(v=msdn.10)) provides style guidelines for Windows XP icons.</span></span> <span data-ttu-id="6c79e-136">Il file di immagine dell'icona del dispositivo incorpora dodici immagini in un singolo file, fornendo quattro dimensioni diverse con tre diverse profondità di colore.</span><span class="sxs-lookup"><span data-stu-id="6c79e-136">The device icon image file incorporates twelve images in a single file by providing four different sizes with three different color depths each.</span></span>

<span data-ttu-id="6c79e-137">Accertarsi di prestare particolare attenzione alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c79e-137">Be certain to pay particular attention to the following guidelines:</span></span>

-   <span data-ttu-id="6c79e-138">Le dimensioni consigliate (in pixel) sono 16x16, 32x32, 48x48 e 256x256.</span><span class="sxs-lookup"><span data-stu-id="6c79e-138">Recommended sizes (in pixels) are 16x16, 32x32, 48x48, and 256x256.</span></span>
-   <span data-ttu-id="6c79e-139">Le profondità di colore consigliate sono a 24 bit con canale alfa a 8 bit, a 8 bit con trasparenza a 1 bit e a 4 bit con trasparenza a 1 bit.</span><span class="sxs-lookup"><span data-stu-id="6c79e-139">Recommended color depths are 24-bit with 8-bit alpha channel, 8-bit with 1-bit transparency, and 4-bit with 1-bit transparency.</span></span>
-   <span data-ttu-id="6c79e-140">Usare l'angolo prospettico e i consigli per l'ombreggiatura descritti negli articoli di MSDN menzionati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="6c79e-140">Use the perspective angle and drop shadow recommendations described in the MSDN articles mentioned previously.</span></span>

<span data-ttu-id="6c79e-141">Una volta creato il file icona, è sufficiente rinominarlo devicon. fil.</span><span class="sxs-lookup"><span data-stu-id="6c79e-141">Once you have created the icon file, simply rename it DevIcon.fil.</span></span>

## <a name="creating-the-corporate-logo-image"></a><span data-ttu-id="6c79e-142">Creazione dell'immagine del logo aziendale</span><span class="sxs-lookup"><span data-stu-id="6c79e-142">Creating the Corporate Logo Image</span></span>

<span data-ttu-id="6c79e-143">Il file di immagine del logo aziendale, devlogo. fil, deve contenere un file in formato PNG.</span><span class="sxs-lookup"><span data-stu-id="6c79e-143">The corporate logo image file, DevLogo.fil, must contain a file in PNG format.</span></span> <span data-ttu-id="6c79e-144">Quando si crea l'immagine, attenersi alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c79e-144">Use the following guidelines when creating the image:</span></span>

-   <span data-ttu-id="6c79e-145">Le dimensioni massime per l'immagine sono 150x32 pixel.</span><span class="sxs-lookup"><span data-stu-id="6c79e-145">The maximum dimensions for the image are 150x32 pixels.</span></span>
-   <span data-ttu-id="6c79e-146">L'immagine deve supportare la fusione alfa per consentire una transizione uniforme tra l'interfaccia utente di Windows Media Player 10 e il logo.</span><span class="sxs-lookup"><span data-stu-id="6c79e-146">The image should support alpha blending to enable a smooth transition between the Windows Media Player 10 user interface and the logo.</span></span>

<span data-ttu-id="6c79e-147">Una volta creato il file del logo aziendale, è sufficiente rinominarlo devlogo. fil.</span><span class="sxs-lookup"><span data-stu-id="6c79e-147">Once you have created the corporate logo file, simply rename it DevLogo.fil.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c79e-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c79e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c79e-149">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="6c79e-149">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 