---
description: Questi metodi devono essere sottoposti a override dalle classi derivate.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Metodi virtuali puri CMSPCallBase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d8dea4c1a240e362a4dc3a19b3c09a37a318947
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882022"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>Metodi virtuali puri CMSPCallBase

Questi metodi devono essere sottoposti a override dalle classi derivate.



| Metodi virtuali puri CMSPCallBase                                 | Descrizione                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPCallAddRef**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Metodo AddRef privato per l'oggetto call.                                                                                              |
| [**MSPCallRelease**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | Metodo di rilascio privato per l'oggetto call.                                                                                             |
| [**Init**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | Chiamato dall'oggetto dell'indirizzo MSP (nel metodo [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) per inizializzare l'oggetto chiamata msp. |
| [**Arresto**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | Chiamato dall'oggetto dell'indirizzo MSP per arrestare la chiamata.                                                                                |
| [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | Chiamato da [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) per creare un oggetto flusso.                                               |
| [**CreateStreamObject**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | Chiamato da [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) per creare un oggetto flusso.                                  |
| [**RemoveStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | Chiamato dall'applicazione per rimuovere un flusso dalla chiamata                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
