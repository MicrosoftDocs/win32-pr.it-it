---
description: Specifica il livello di volume massimo desiderato del contenuto audio di output.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: MFPKEY_WMADRC_PEAKTARGET proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79f54d15978bb3f6a34c015886d2aeb2a8ec48a0069669e81ea40bbd79353902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973230"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a>Proprietà MFPKEY \_ WMADRC \_ PEAKTARGET

Specifica il livello di volume massimo desiderato del contenuto audio di output.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMADRCPeakTarget

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

È possibile impostare questo valore nel decodificatore ai fini del controllo a intervalli dinamici, ma avrà effetto solo se è impostata la proprietà [MFPKEY \_ WMADEC \_ DRCMODE.](mfpkey-wmadec-drcmodeproperty.md)

Se si richiede il controllo dell'intervallo dinamico dal decodificatore quando questa proprietà non è impostata, il codec calcola un valore predefinito.

Usare le [proprietà MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) per calcolare i valori appropriati per questa proprietà.

Per altre informazioni sul controllo dinamico degli intervalli, vedere l'articolo Web [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
