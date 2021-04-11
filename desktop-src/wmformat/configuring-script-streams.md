---
title: Configurazione di flussi di script
description: Configurazione di flussi di script
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- flussi, configurazione di flussi di script
- codec, configurazione di flussi di script
- flussi di script, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044587"
---
# <a name="configuring-script-streams"></a><span data-ttu-id="18ad3-106">Configurazione di flussi di script</span><span class="sxs-lookup"><span data-stu-id="18ad3-106">Configuring Script Streams</span></span>

<span data-ttu-id="18ad3-107">Come tutti i tipi di flusso arbitrari, i flussi di script devono avere una velocità in bit e una finestra del buffer definiti.</span><span class="sxs-lookup"><span data-stu-id="18ad3-107">Like all arbitrary stream types, script streams need to have a bit rate and buffer window defined for them.</span></span> <span data-ttu-id="18ad3-108">Il tipo di supporto principale nella struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) deve essere impostato su WMMEDIATYPE \_ script.</span><span class="sxs-lookup"><span data-stu-id="18ad3-108">The major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure must be set to WMMEDIATYPE\_Script.</span></span>

<span data-ttu-id="18ad3-109">Per i flussi di script è necessario che il membro **formatType** del **\_ \_ tipo di supporto WM** sia impostato su WMFORMAT \_ script, che indica che il membro **pbFormat** punta a una struttura [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .</span><span class="sxs-lookup"><span data-stu-id="18ad3-109">Script streams need to have the **formattype** member of **WM\_MEDIA\_TYPE** set to WMFORMAT\_Script, which indicates that the **pbFormat** member points to a [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) structure.</span></span>

<span data-ttu-id="18ad3-110">È disponibile un solo tipo di script supportato, WMSCRIPTTYPE \_ TwoStrings.</span><span class="sxs-lookup"><span data-stu-id="18ad3-110">There is only one supported script type, WMSCRIPTTYPE\_TwoStrings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18ad3-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18ad3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18ad3-112">**Configurazione comune a tutti i flussi**</span><span class="sxs-lookup"><span data-stu-id="18ad3-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="18ad3-113">**Configurazione di tipi di flusso arbitrari**</span><span class="sxs-lookup"><span data-stu-id="18ad3-113">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="18ad3-114">**Comandi script**</span><span class="sxs-lookup"><span data-stu-id="18ad3-114">**Script Commands**</span></span>](script-commands.md)
</dt> </dl>

 

 




