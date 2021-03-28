---
description: Questa sezione descrive le funzioni di gestione della tavolozza dei colori della shell di Windows. Gli elementi di programmazione descritti in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi. h e Shlwapi. lib.
title: Funzioni di gestione della tavolozza dei colori della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 93848cb3-60c6-4b2f-82d9-abfee97e372a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba92dcf280b8d54b8778e276bb603d888f5991c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231920"
---
# <a name="shell-color-palette-handling-functions"></a><span data-ttu-id="dfbee-104">Funzioni di gestione della tavolozza dei colori della shell</span><span class="sxs-lookup"><span data-stu-id="dfbee-104">Shell Color Palette Handling Functions</span></span>

<span data-ttu-id="dfbee-105">Questa sezione descrive le funzioni di gestione della tavolozza dei colori della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="dfbee-105">This section describes the Windows Shell color palette handling functions.</span></span> <span data-ttu-id="dfbee-106">Gli elementi di programmazione descritti in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi. h e Shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="dfbee-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dfbee-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="dfbee-107">In this section</span></span>



| <span data-ttu-id="dfbee-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="dfbee-108">Topic</span></span>                                                           | <span data-ttu-id="dfbee-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfbee-109">Description</span></span>                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfbee-110">**ColorAdjustLuma**</span><span class="sxs-lookup"><span data-stu-id="dfbee-110">**ColorAdjustLuma**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-coloradjustluma)<br/>           | <span data-ttu-id="dfbee-111">Modifica la luminosità di un valore RGB.</span><span class="sxs-lookup"><span data-stu-id="dfbee-111">Changes the luminance of a RGB value.</span></span> <span data-ttu-id="dfbee-112">Hue e Saturation non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="dfbee-112">Hue and saturation are not affected.</span></span><br/> |
| [<span data-ttu-id="dfbee-113">**ColorHLSToRGB**</span><span class="sxs-lookup"><span data-stu-id="dfbee-113">**ColorHLSToRGB**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorhlstorgb)<br/>               | <span data-ttu-id="dfbee-114">Converte i colori da Hue-Luminance-Saturation (HLS) a formato RGB.</span><span class="sxs-lookup"><span data-stu-id="dfbee-114">Converts colors from hue-luminance-saturation (HLS) to RGB format.</span></span><br/>         |
| [<span data-ttu-id="dfbee-115">**ColorRGBToHLS**</span><span class="sxs-lookup"><span data-stu-id="dfbee-115">**ColorRGBToHLS**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorrgbtohls)<br/>               | <span data-ttu-id="dfbee-116">Converte i colori dal formato RGB a Hue-Luminance (HLS).</span><span class="sxs-lookup"><span data-stu-id="dfbee-116">Converts colors from RGB to hue-luminance-saturation (HLS) format.</span></span><br/>         |
| [<span data-ttu-id="dfbee-117">**SHCreateShellPalette**</span><span class="sxs-lookup"><span data-stu-id="dfbee-117">**SHCreateShellPalette**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreateshellpalette)<br/> | <span data-ttu-id="dfbee-118">Crea una tavolozza di mezzitoni per il contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="dfbee-118">Creates a halftone palette for the specified device context.</span></span><br/>               |



 

 

 




