---
description: Il terminale CAudioCaptureTerminal è derivato da CSingleFilterTerminal e implementa un terminale di acquisizione audio statico per i dispositivi Wave usando il filtro di DirectShow WaveIn. Per la maggior parte dei MSPs non è necessario eseguire l'override dell'implementazione di questo terminale.
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: CAudioCaptureTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314628"
---
# <a name="caudiocaptureterminal"></a><span data-ttu-id="fac67-104">CAudioCaptureTerminal</span><span class="sxs-lookup"><span data-stu-id="fac67-104">CAudioCaptureTerminal</span></span>

<span data-ttu-id="fac67-105">Il terminale **CAudioCaptureTerminal** è derivato da [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminale di acquisizione audio statico per i dispositivi Wave usando il filtro di DirectShow WaveIn.</span><span class="sxs-lookup"><span data-stu-id="fac67-105">The **CAudioCaptureTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio capture terminal for wave devices using the DirectShow wavein filter.</span></span> <span data-ttu-id="fac67-106">Per la maggior parte dei MSPs non è necessario eseguire l'override dell'implementazione di questo terminale.</span><span class="sxs-lookup"><span data-stu-id="fac67-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="fac67-107">Definito in MSPtmac. h.</span><span class="sxs-lookup"><span data-stu-id="fac67-107">Defined in MSPtmac.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac67-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="fac67-108">Remarks</span></span>

<span data-ttu-id="fac67-109">I metodi [**put \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) e [**get \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) di **CAudioCaptureTerminal** non sono implementati e restituiscono e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="fac67-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioCaptureTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



