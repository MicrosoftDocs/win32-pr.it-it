---
description: Specifica se il DSP di acquisizione vocale usa la modalità di origine o filtro.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: Proprietà MFPKEY_WMAAECMA_DMO_SOURCE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226544"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a>\_ \_ \_ Proprietà modalità origine MFPKEY WMAAECMA DMO \_

Specifica se il DSP di acquisizione vocale usa la modalità di origine o filtro.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

VARIANT \_ true

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

In modalità origine, l'applicazione non deve inviare dati di input al DSP, perché il DSP estrae automaticamente i dati dai dispositivi audio. In modalità filtro, l'applicazione deve inviare i dati di input al DSP.

Questa proprietà può includere i valori seguenti.



| Valore          | Descrizione  |
|----------------|--------------|
| VARIANTE \_ false | Modalità filtro. |
| VARIANT \_ true  | Modalità di origine. |



 

> [!Note]  
> Quando DMO è in modalità origine, è necessario chiamare [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) per impostare il formato del flusso di output e non chiamare [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) per impostare i formati del flusso di input. In caso contrario, l'inizializzazione DMO non riuscirà.

 

Se il valore di questa proprietà è VARIANT \_ true, il DSP ha zero input. Se il valore è VARIANT \_ false, il DSP dispone di uno o due input, a seconda del valore della proprietà [MFPKEY \_ WMAAECMA \_ System \_ mode](mfpkey-wmaaecma-system-modeproperty.md) , come illustrato nella tabella seguente.



| Valore                     | Numero di input |
|---------------------------|------------------|
| OPTIBEAM \_ array \_ e \_ AEC | 2                |
| \_solo matrice \_ OPTIBEAM     | 1                |
| \_AEC canale \_ singolo      | 2                |
| \_NSAGC a canale singolo \_    | 1                |



 

> [!Note]  
> Solo le modalità con un singolo input funzioneranno con il filtro del wrapper DMO dall'API DirectShow 9,0.

 

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

 

 
