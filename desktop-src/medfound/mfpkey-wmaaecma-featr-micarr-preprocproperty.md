---
description: Specifica se il DSP di acquisizione vocale esegue la pre-elaborazione dell'array di microfoni.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbba5faeb1a1e70feb1ef6182d3ac2a397a52c4a56f27e767be93f4a3fff773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873015"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a>Proprietà PREPROC MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_

Specifica se il DSP di acquisizione vocale esegue la pre-elaborazione dell'array di microfoni.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="default-value"></a>Valore predefinito

VARIANT \_ TRUE

## <a name="applies-to"></a>Si applica a

-   [Voice Capture DSP](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

La pre-elaborazione può rimuovere toni stazionari che interferiscono con l'elaborazione, ad esempio un tono con un passo fisso.

Questa proprietà può avere i valori seguenti.



| Valore          | Descrizione            |
|----------------|------------------------|
| VARIANT \_ FALSE | Disabilitare la pre-elaborazione. |
| VARIANT \_ TRUE  | Abilitare la pre-elaborazione.  |



 

Il valore predefinito di questa proprietà è VARIANT \_ TRUE (abilitato). Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) su VARIANT \_ TRUE.

Il provider di servizi di configurazione usa questa proprietà solo quando è abilitata l'elaborazione della matrice del microfono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Voice Capture DSP](voicecapturedmo.md)
</dt> </dl>

 

 
