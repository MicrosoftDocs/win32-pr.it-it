---
description: Questo attributo specifica una protezione aggiuntiva offerta da un'autorità di attendibilità dell'output video quando un connettore non offre protezione dell'output.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: MFPROTECTION_CONSTRICTVIDEO_NOOPM attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72d1d7cd858ec9cf254cca1dffc5fef4e24fbb5a3a288975a9f70c9ae118dde3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713741"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a>Attributo MFPROTECTION \_ CONSTRICTVIDEO \_ NOOPM

Questo attributo specifica una protezione aggiuntiva offerta da un'autorità di attendibilità dell'output video quando un connettore non offre protezione dell'output.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Si tratta di una protezione aggiuntiva offerta da un'autorità di attendibilità dell'output video quando un connettore non offre protezione dell'output (vedere [**IMFOutputTrustAuthority).**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority) In questo caso l'OTA può offrire questa protezione il cui effetto è lo stesso della protezione [MFPROTECTION \_ CONSTRICTVIDEO.](mfprotection-constrictvideo.md) Questo viene definito per evitare confusione con le chiamate precedenti alle interazioni [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) in cui è stata usata la protezione MFPROTECTION CONSTRICTVIDEO per identificare lo pseudocontenitore gestione finestre \_ desktop.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                       |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




