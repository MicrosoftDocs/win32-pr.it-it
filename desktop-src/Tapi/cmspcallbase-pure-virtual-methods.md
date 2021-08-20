---
description: 'Metodi virtuali puri CMSPCallBase: questi metodi devono essere sottoposti a override dalle classi derivate.'
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Metodi virtuali puri CMSPCallBase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9fdd6fb66c0dd7dabfcf2b78866b49ff617cfca22a53495ad23b35680d7b47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117947170"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>Metodi virtuali puri CMSPCallBase

Questi metodi devono essere sottoposti a override dalle classi derivate.



| Metodi virtuali puri CMSPCallBase                                 | Descrizione                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPCallAddRef**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Metodo AddRef privato per l'oggetto di chiamata.                                                                                              |
| [**MSPCallRelease**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | Metodo Release privato per l'oggetto di chiamata.                                                                                             |
| [**Init**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | Chiamato dall'oggetto indirizzo MSP (nel metodo [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) per inizializzare l'oggetto chiamata MSP. |
| [**Arresto**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | Chiamato dall'oggetto indirizzo MSP per arrestare la chiamata.                                                                                |
| [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | Chiamato da [**CreateStream per**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) creare un oggetto flusso.                                               |
| [**CreateStreamObject**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | Chiamato da [**InternalCreateStream per**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) creare un oggetto flusso.                                  |
| [**RemoveStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | Chiamato dall'applicazione per rimuovere un flusso dalla chiamata                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
