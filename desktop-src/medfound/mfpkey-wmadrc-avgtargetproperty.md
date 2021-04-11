---
description: Specifica il livello di volume medio desiderato per il contenuto audio di output.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: Proprietà MFPKEY_WMADRC_AVGTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226916"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a>MFPKEY \_ WMADRC- \_ Proprietà AVGTARGET

Specifica il livello di volume medio desiderato per il contenuto audio di output.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMADRCAverageTarget

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

È possibile impostare questo valore nel decodificatore allo scopo di un controllo intervallo dinamico, ma avrà effetto solo se viene impostata la proprietà [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .

> [!Note]  
> Non è consigliabile impostare il valore di destinazione medio. La regolazione del valore medio non influisce sulla differenza tra sonorità e suoni morbidi. Viene invece tagliato o incrementato il volume medio complessivo che può causare una distorsione indesiderata durante la riproduzione.

 

Se si richiede il controllo dinamico degli intervalli dal decodificatore quando questa proprietà non è impostata, il codec calcolerà un valore predefinito.

Usare le proprietà [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) per calcolare i valori appropriati per questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




