---
description: Specifica se il provider di servizi di acquisizione vocale usa la modalità di origine o di filtro.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: MFPKEY_WMAAECMA_DMO_SOURCE_MODE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec9dd01be5a020047410362b2fdfc27fd8d703a393e3ae2f557b1dd3a42bf80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555301"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ DMO \_ SOURCE \_ MODE

Specifica se il provider di servizi di acquisizione vocale usa la modalità di origine o di filtro.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="default-value"></a>Valore predefinito

VARIANT \_ TRUE

## <a name="applies-to"></a>Si applica a

-   [Provider di servizi di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

In modalità di origine, non è necessario che l'applicazione invii dati di input al provider di servizi di distribuzione, perché esegue automaticamente il pull dei dati dai dispositivi audio. In modalità filtro, l'applicazione deve inviare i dati di input al provider di servizi di distribuzione.

Questa proprietà può avere i valori seguenti.



| Valore          | Descrizione  |
|----------------|--------------|
| VARIANT \_ FALSE | Modalità filtro. |
| VARIANT \_ TRUE  | Modalità di origine. |



 

> [!Note]  
> Quando il DMO è in modalità di origine, è necessario chiamare [**solo IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) per impostare il formato del flusso di output e non [**chiamare IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) per impostare i formati del flusso di input. In caso DMO'inizializzazione avrà esito negativo.

 

Se il valore di questa proprietà è VARIANT \_ TRUE, DSP ha zero input. Se il valore è VARIANT FALSE, il provider di servizi di configurazione dispone di uno o due input, a seconda del valore della proprietà \_ [MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE,](mfpkey-wmaaecma-system-modeproperty.md) come illustrato nella tabella seguente.



| Valore                     | Numero di input |
|---------------------------|------------------|
| MATRICE OPTIBEAM \_ \_ E \_ AEC | 2                |
| SOLO MATRICE \_ \_ OPTIBEAM     | 1                |
| \_ \_ AEC AEC a CANALE SINGOLO      | 2                |
| \_ \_ NSAGC A CANALE SINGOLO    | 1                |



 

> [!Note]  
> Solo le modalità con un singolo input funzioneranno con il filtro wrapper DMO dall'API DirectShow 9.0.

 

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

 

 
