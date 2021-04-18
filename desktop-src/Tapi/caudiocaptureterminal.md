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
# <a name="caudiocaptureterminal"></a>CAudioCaptureTerminal

Il terminale **CAudioCaptureTerminal** è derivato da [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminale di acquisizione audio statico per i dispositivi Wave usando il filtro di DirectShow WaveIn. Per la maggior parte dei MSPs non è necessario eseguire l'override dell'implementazione di questo terminale.

Definito in MSPtmac. h.

## <a name="remarks"></a>Commenti

I metodi [**put \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) e [**get \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) di **CAudioCaptureTerminal** non sono implementati e restituiscono e \_ NOTIMPL.

 

 



