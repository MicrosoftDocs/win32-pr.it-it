---
description: 'Metodi virtuali puri CMSPAddress: questi metodi devono essere sottoposti a override dalle classi derivate.'
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Metodi virtuali puri CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d9b9494e4ee42972d97433927fd587034af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084209"
---
# <a name="cmspaddress-pure-virtual-methods"></a>Metodi virtuali puri CMSPAddress

Questi metodi devono essere sottoposti a override dalle classi derivate.



| Metodi virtuali puri CMSPAddress                           | Descrizione                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | Metodo AddRef privato per l'indirizzo.                                                                                                                                                 |
| [**MSPAddressRelease**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | Metodo Release privato per l'indirizzo.                                                                                                                                                |
| [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | Chiamato da TAPI per creare un oggetto chiamata. L'implementazione nella classe derivata deve semplicemente chiamare [**la funzione CreateMSPCallHelper.**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper)        |
| [**ShutdownMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | Chiamato da TAPI per arrestare un oggetto chiamata. L'implementazione nella classe derivata deve chiamare semplicemente la [**funzione ShutdownMSPCallHelper.**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) |
| [**GetCallMediaTypes**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | Ottiene i tipi di supporti supportati dal msp.                                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



