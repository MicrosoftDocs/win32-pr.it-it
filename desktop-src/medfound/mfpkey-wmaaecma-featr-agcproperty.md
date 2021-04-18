---
description: Specifica se il DSP di acquisizione vocale esegue il controllo di guadagno automatico.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: Proprietà MFPKEY_WMAAECMA_FEATR_AGC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309135"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>\_Proprietà MFPKEY WMAAECMA \_ featr \_ AGC

Specifica se il DSP di acquisizione vocale esegue il controllo di guadagno automatico.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

VARIANTE \_ false

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il controllo del guadagno automatico è un componente DSP (Digital Signal Processing) che regola il guadagno in modo che il livello di output del segnale rimanga entro lo stesso intervallo approssimativo.

Questa proprietà può includere i valori seguenti.



| Valore          | Descrizione                     |
|----------------|---------------------------------|
| VARIANTE \_ false | Disabilitare il controllo di guadagno automatico. |
| VARIANT \_ true  | Abilitare il controllo di guadagno automatico.  |



 

Il valore predefinito di questa proprietà è VARIANT \_ false (disabilitato). Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.

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

 

 
