---
description: Specifica il livello medio di volume desiderato del contenuto audio di output.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: MFPKEY_WMADRC_AVGTARGET proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1cdd3143d7ca91be3856c9eaf3b7daecbfd80bff53fbd36c20c830dcb64e1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887611"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a>Proprietà AVGTARGET MFPKEY \_ WMADRC \_

Specifica il livello medio di volume desiderato del contenuto audio di output.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMADRCAverageTarget

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

È possibile impostare questo valore nel decodificatore ai fini del controllo a intervalli dinamici, ma avrà effetto solo se è impostata la proprietà [MFPKEY \_ WMADEC \_ DRCMODE.](mfpkey-wmadec-drcmodeproperty.md)

> [!Note]  
> L'impostazione del valore medio di destinazione non è consigliata. La regolazione del valore medio non influisce sulla differenza tra suoni forti e soffi. Riduce o aumenta invece il volume medio complessivo che può causare distorsioni indesiderate durante la riproduzione.

 

Se si richiede il controllo dell'intervallo dinamico dal decodificatore quando questa proprietà non è impostata, il codec calcola un valore predefinito.

Usare le [proprietà MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) per calcolare i valori appropriati per questa proprietà.

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

 

 




