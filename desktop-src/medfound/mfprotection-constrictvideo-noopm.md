---
description: Questo attributo specifica una protezione aggiuntiva offerta da un'autorità di attendibilità video output quando un connettore non offre la protezione dell'output.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: Attributo MFPROTECTION_CONSTRICTVIDEO_NOOPM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966993"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a>MFPROTECTION \_ CONSTRICTVIDEO- \_ attributo NOOPM

Questo attributo specifica una protezione aggiuntiva offerta da un'autorità di attendibilità video output quando un connettore non offre la protezione dell'output.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Si tratta di una protezione aggiuntiva offerta da un servizio OTA (video output Trust Authority) quando un connettore non offre la protezione dell'output (vedere [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)). In questo caso, l'OTA può offrire questa protezione il cui effetto è identico a quello di [MFPROTECTION \_ CONSTRICTVIDEO](mfprotection-constrictvideo.md) Protection. Questa operazione viene definita per evitare confusione con le chiamate precedenti a [**IMFOutputPolicy:: GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interazioni in cui \_ è stata usata la protezione MFPROTECTION CONSTRICTVIDEO per identificare lo pseudo-connettore Desktop Window Manager.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                       |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




