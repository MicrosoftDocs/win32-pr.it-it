---
description: Specifica se il provider di servizi di acquisizione vocale esegue il riempimento del disturbo.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: MFPKEY_WMAAECMA_FEATR_NOISE_FILL proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec3f2f6780157da97263bd6e68ac5f38c9448a5633fafe6481b082ed033331dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035119"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ FEATR \_ NOISE \_ FILL

Specifica se il provider di servizi di acquisizione vocale esegue il riempimento del disturbo.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="default-value"></a>Valore predefinito

VARIANT \_ TRUE

## <a name="applies-to"></a>Si applica a

-   [Provider di servizi di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il riempimento del rumore aggiunge una piccola quantità di disturbo alle parti del segnale in cui il ritaglio centrale ha rimosso gli echi residui. Ciò consente all'utente di ottenere un'esperienza migliore rispetto a lasciare lacune silenziose nel segnale.

Questa proprietà può avere i valori seguenti.



| Valore          | Descrizione            |
|----------------|------------------------|
| VARIANT \_ TRUE  | Abilitare il riempimento del disturbo.  |
| VARIANT \_ FALSE | Disabilitare il riempimento del disturbo. |



 

Il valore predefinito di questa proprietà è VARIANT \_ TRUE (abilitato). Prima di impostare questa proprietà, è necessario impostare la [proprietà MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) su VARIANT \_ TRUE.

DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Provider di servizi di acquisizione vocale](voicecapturedmo.md)
</dt> </dl>

 

 
