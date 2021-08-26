---
description: Specifica se il provider di servizi di acquisizione vocale applica il limite di guadagno del microfono.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d00e906ec953e2fd00d9c288336c322c2d0dc07ea1c2d74a014ab78ae21acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113151"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ MIC \_ GAIN \_ BOUNDER

Specifica se il provider di servizi di acquisizione vocale applica il limite di guadagno del microfono.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="default-value"></a>Valore predefinito

VARIANT \_ TRUE

## <a name="applies-to"></a>Si applica a

-   [Provider di servizi di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il limite di guadagno del microfono garantisce che il microfono abbia il livello di guadagno corretto. Se il guadagno è troppo alto, il segnale acquisito potrebbe essere saturo e verrà ritagliato. Il ritaglio è un effetto non lineare, che causerà l'esito negativo dell'algoritmo di annullamento dell'eco acustica (AEC). Se il guadagno è troppo basso, il rapporto segnale-rumore è basso, il che può anche causare un errore dell'algoritmo AEC o di prestazioni non riuscite.

Questa proprietà può avere i valori seguenti.



| Valore          | Descrizione                       |
|----------------|-----------------------------------|
| VARIANT \_ TRUE  | Abilitare il delimitazione del guadagno del microfono.  |
| VARIANT \_ FALSE | Disabilitare il delimitazione del guadagno del microfono. |



 

Il valore predefinito di questa proprietà è VARIANT \_ TRUE (abilitato).

Il delimitazione del guadagno del microfono si applica solo quando il DSP opera in modalità di origine. In modalità filtro, l'applicazione deve assicurarsi che il microfono abbia il livello di guadagno corretto.

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

 

 
