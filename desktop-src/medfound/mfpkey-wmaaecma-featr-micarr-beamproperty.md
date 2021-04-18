---
description: Specifica il fascio utilizzato dal DSP di acquisizione vocale per l'elaborazione di matrici di microfoni.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: Proprietà MFPKEY_WMAAECMA_FEATR_MICARR_BEAM (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309131"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>MFPKEY \_ WMAAECMA \_ featr \_ MICARR \_ Beam proprietà

Specifica il fascio utilizzato dal DSP di acquisizione vocale per l'elaborazione di matrici di microfoni.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Impostare questa proprietà se il valore della proprietà [MFPKEY \_ WMAAECMA \_ featr \_ MICARR \_ mode](mfpkey-wmaaecma-featr-micarr-modeproperty.md) è MICARRAY \_ extern \_ Beam.

Se il valore di [**MFPKEY \_ WMAAECMA \_ featr \_ MICARR \_ mode**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) è MICARRAY \_ Single \_ Beam, è possibile leggere questa proprietà per eseguire una query su quale Beam è stato selezionato dal DSP.

Questa proprietà può includere i valori seguenti. I valori sono in gradi orizzontali.



| Valore | Descrizione              |
|-------|--------------------------|
| 0     | -50 gradi.             |
| 1     | -40 gradi.             |
| 2     | -30 gradi.             |
| 3     | -20 gradi.             |
| 4     | -10 gradi.             |
| 5     | 0 gradi (raggio centrale). |
| 6     | 10 gradi.              |
| 7     | 20 gradi.              |
| 8     | 30 gradi.              |
| 9     | 40 gradi.              |
| 10    | 50 gradi.              |



 

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

 

 
