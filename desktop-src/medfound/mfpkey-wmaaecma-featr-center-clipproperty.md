---
description: Specifica se l'acquisizione vocale DSP esegue il ritaglio al centro.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: Proprietà MFPKEY_WMAAECMA_FEATR_CENTER_CLIP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226543"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a>\_Proprietà clip MFPKEY WMAAECMA \_ featr \_ Center \_

Specifica se l'acquisizione vocale DSP esegue il ritaglio al centro.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

VARIANT \_ true

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il ritaglio al centro è un processo che rimuove i residui di eco piccoli che rimangono dopo l'elaborazione AEC, in situazioni di sola conversazione (quando il discorso si verifica solo su un'estremità della riga).

Questa proprietà può includere i valori seguenti.



| Valore          | Descrizione              |
|----------------|--------------------------|
| VARIANTE \_ false | Disabilitare il ritaglio al centro. |
| VARIANT \_ true  | Abilita ritaglio al centro.  |



 

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

 

 
