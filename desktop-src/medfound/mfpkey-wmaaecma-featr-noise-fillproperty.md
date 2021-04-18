---
description: Specifica se l'acquisizione vocale DSP esegue il riempimento del rumore.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: Proprietà MFPKEY_WMAAECMA_FEATR_NOISE_FILL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309122"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a>\_ \_ \_ Proprietà riempimento rumore MFPKEY WMAAECMA featr \_

Specifica se l'acquisizione vocale DSP esegue il riempimento del rumore.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

VARIANT \_ true

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il riempimento del rumore aggiunge una piccola quantità di rumore alle parti del segnale in cui il ritaglio al centro ha rimosso gli echi residui. In questo modo si ottiene un'esperienza migliore per l'utente rispetto alla mancata presenza di gap nel segnale.

Questa proprietà può includere i valori seguenti.



| Valore          | Descrizione            |
|----------------|------------------------|
| VARIANT \_ true  | Abilita riempimento rumore.  |
| VARIANTE \_ false | Disabilitare il riempimento del rumore. |



 

Il valore predefinito di questa proprietà è VARIANT \_ true (Enabled). Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.

Il DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP di acquisizione vocale](voicecapturedmo.md)
</dt> </dl>

 

 
