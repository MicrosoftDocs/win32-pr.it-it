---
description: Questi metodi devono essere sottoposti a override dalle classi derivate.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Metodi virtuali puri CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312728"
---
# <a name="cmspaddress-pure-virtual-methods"></a>Metodi virtuali puri CMSPAddress

Questi metodi devono essere sottoposti a override dalle classi derivate.



| Metodi virtuali puri CMSPAddress                           | Descrizione                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | Metodo AddRef privato per l'indirizzo.                                                                                                                                                 |
| [**MSPAddressRelease**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | Metodo di rilascio privato per l'indirizzo.                                                                                                                                                |
| [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | Chiamato da TAPI per creare un oggetto chiamata. L'implementazione nella classe derivata deve semplicemente chiamare la funzione [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) .        |
| [**ShutdownMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | Chiamato da TAPI per arrestare un oggetto chiamata. L'implementazione nella classe derivata deve semplicemente chiamare la funzione [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) . |
| [**GetCallMediaTypes**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | Ottiene i tipi di supporto supportati dall'MSP.                                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



