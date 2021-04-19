---
description: Il terminale CAudioRenderTerminal è derivato da CSingleFilterTerminal e implementa un terminale di rendering audio statico per i dispositivi Wave usando il filtro di origine DirectShow. Per la maggior parte dei MSPs non è necessario eseguire l'override dell'implementazione di questo terminale.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314627"
---
# <a name="caudiorenderterminal"></a>CAudioRenderTerminal

Il terminale **CAudioRenderTerminal** è derivato da [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminale di rendering audio statico per i dispositivi Wave usando il filtro di origine DirectShow. Per la maggior parte dei MSPs non è necessario eseguire l'override dell'implementazione di questo terminale.

Definito in MSPtrmar. h.

## <a name="remarks"></a>Commenti

I metodi [**put \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) e [**get \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) di **CAudioRenderTerminal** non sono implementati e restituiscono e \_ NOTIMPL.

 

 



