---
title: Ridimensionamento della finestra di dialogo acquisizione licenza
description: Ridimensionamento della finestra di dialogo acquisizione licenza
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Finestra di dialogo Media Player di Windows, ridimensionamento dell'acquisizione delle licenze
- Windows Media Player, finestra di dialogo acquisizione licenza
- Media Player di Windows, attributo DRM_LicenseAcqURL
- finestra di dialogo di ridimensionamento dell'acquisizione delle licenze
- Finestra di dialogo acquisizione licenza
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396383"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a><span data-ttu-id="f2ec6-109">Ridimensionamento della finestra di dialogo acquisizione licenza</span><span class="sxs-lookup"><span data-stu-id="f2ec6-109">Resizing the License Acquisition Dialog Box</span></span>

<span data-ttu-id="f2ec6-110">È possibile aggiungere i parametri della stringa di query all'URL specificato per l'attributo **\_ LicenseAcqURL di DRM** per specificare una dimensione per la finestra di dialogo di acquisizione della licenza di Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-110">You can append query string parameters to the URL you provide for the **DRM\_LicenseAcqURL** attribute to specify a size for the Windows Media Player 10 or later license acquisition dialog box.</span></span> <span data-ttu-id="f2ec6-111">Nella tabella seguente sono elencati i parametri.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-111">The following table lists the parameters.</span></span>



| <span data-ttu-id="f2ec6-112">Parametro</span><span class="sxs-lookup"><span data-stu-id="f2ec6-112">Parameter</span></span> | <span data-ttu-id="f2ec6-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2ec6-113">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="f2ec6-114">*DlgX*</span><span class="sxs-lookup"><span data-stu-id="f2ec6-114">*DlgX*</span></span>    | <span data-ttu-id="f2ec6-115">Specifica la larghezza, in pixel, della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-115">Specifies the width of the dialog box, in pixels.</span></span>  |
| <span data-ttu-id="f2ec6-116">*DlgY*</span><span class="sxs-lookup"><span data-stu-id="f2ec6-116">*DlgY*</span></span>    | <span data-ttu-id="f2ec6-117">Specifica l'altezza, in pixel, della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-117">Specifies the height of the dialog box, in pixels.</span></span> |



 

<span data-ttu-id="f2ec6-118">Ad esempio, l'URL di acquisizione della licenza seguente determina l'apertura della finestra di dialogo acquisizione licenza con una dimensione di 800 per 600 pixel:</span><span class="sxs-lookup"><span data-stu-id="f2ec6-118">For example, the following license acquisition URL would cause the license acquisition dialog box to open with a size of 800 by 600 pixels:</span></span>


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



<span data-ttu-id="f2ec6-119">Le dimensioni massime per la finestra di dialogo non supereranno mai le dimensioni correnti dello schermo meno 20 pixel.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-119">The maximum size for the dialog box will never exceed the current screen dimensions minus 20 pixels.</span></span> <span data-ttu-id="f2ec6-120">La dimensione minima è 333 x 210 pixel (dimensione predefinita).</span><span class="sxs-lookup"><span data-stu-id="f2ec6-120">The minimum size is 333 x 210 pixels (the default size).</span></span>

<span data-ttu-id="f2ec6-121">Questa funzionalità richiede Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-121">This feature requires Windows Media Player 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2ec6-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2ec6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2ec6-123">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="f2ec6-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




