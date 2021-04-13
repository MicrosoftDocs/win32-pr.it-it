---
title: Accesso e controllo dei dati del frame DWM
description: In questo argomento vengono illustrate le API di Gestione finestre desktop (DWM) utilizzate per la pianificazione e la presentazione multimediale.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- API di presentazione Gestione finestre desktop (DWM), pianificazione e supporti
- DWM (Gestione finestre desktop), pianificazione e API presentazione di supporti
- API per la pianificazione e la presentazione multimediale
- Gestione finestre desktop (DWM), accesso ai dati del frame
- DWM (Gestione finestre desktop), accesso ai dati del frame
- accesso ai dati del frame
- Gestione finestre desktop (DWM), controllo dei dati del frame
- DWM (Gestione finestre desktop), controllo dei dati del frame
- controllo dei dati del frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330279"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a><span data-ttu-id="9c680-112">Accesso e controllo dei dati del frame DWM</span><span class="sxs-lookup"><span data-stu-id="9c680-112">Accessing and Controlling DWM Frame Data</span></span>

<span data-ttu-id="9c680-113">In questo argomento vengono illustrate le API di Gestione finestre desktop (DWM) utilizzate per la pianificazione e la presentazione multimediale.</span><span class="sxs-lookup"><span data-stu-id="9c680-113">This topic discusses the Desktop Window Manager (DWM) APIs that are used for scheduling and media presentation.</span></span>

## <a name="dwm-frame-timing-api"></a><span data-ttu-id="9c680-114">API intervallo frame DWM</span><span class="sxs-lookup"><span data-stu-id="9c680-114">DWM Frame Timing API</span></span>

<span data-ttu-id="9c680-115">Le API per la pianificazione e la presentazione multimediale consentono un controllo più dettagliato del momento in cui l'immagine desktop viene composita e presentata.</span><span class="sxs-lookup"><span data-stu-id="9c680-115">The scheduling and media presentation APIs enable more detailed control of when the desktop image is composited and presented.</span></span> <span data-ttu-id="9c680-116">Questa operazione è in genere necessaria per le applicazioni per la riproduzione di file multimediali e video per le quali DWM viene eseguito in modo asincrono con la propria pianificazione di presentazione, che può generare artefatti di campionamento, se non strettamente controllati.</span><span class="sxs-lookup"><span data-stu-id="9c680-116">This is typically needed by media and video playback applications for whom the DWM is running asynchronously with their own presentation schedule, which can lead to sampling artifacts if not tightly controlled.</span></span>

<span data-ttu-id="9c680-117">Le funzioni di pianificazione e presentazione multimediale includono quanto segue.</span><span class="sxs-lookup"><span data-stu-id="9c680-117">The scheduling and media presentation functions include the following.</span></span> <span data-ttu-id="9c680-118">I dettagli relativi all'utilizzo sono disponibili in tali pagine.</span><span class="sxs-lookup"><span data-stu-id="9c680-118">Details of their use are found on those pages.</span></span>

-   <span data-ttu-id="9c680-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span><span class="sxs-lookup"><span data-stu-id="9c680-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span></span> <span data-ttu-id="9c680-120">Notifica a DWM di abilitare la pianificazione MMCSS (Multimedia Class Schedule Service) mentre il processo chiamante è attivo.</span><span class="sxs-lookup"><span data-stu-id="9c680-120">Notifies the DWM to enable Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span>
-   <span data-ttu-id="9c680-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span><span class="sxs-lookup"><span data-stu-id="9c680-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span></span> <span data-ttu-id="9c680-122">Recupera le informazioni sulla tempistica di composizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9c680-122">Retrieves the current composition timing information.</span></span>
-   <span data-ttu-id="9c680-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="9c680-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span></span> <span data-ttu-id="9c680-124">Modifica il numero di aggiornamenti durante i quali verrà visualizzato il frame precedente.</span><span class="sxs-lookup"><span data-stu-id="9c680-124">Changes the number of refreshes during which the previous frame will be displayed.</span></span>
-   <span data-ttu-id="9c680-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="9c680-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span></span> <span data-ttu-id="9c680-126">Imposta il numero di aggiornamenti in cui visualizzare il frame presentato.</span><span class="sxs-lookup"><span data-stu-id="9c680-126">Sets the number of refreshes in which to display the presented frame.</span></span>
-   <span data-ttu-id="9c680-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span><span class="sxs-lookup"><span data-stu-id="9c680-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span></span> <span data-ttu-id="9c680-128">Imposta i parametri presenti per la composizione del frame.</span><span class="sxs-lookup"><span data-stu-id="9c680-128">Sets the present parameters for frame composition.</span></span>

 

 




