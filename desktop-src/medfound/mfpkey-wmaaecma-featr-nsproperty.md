---
description: Specifica se il DSP di acquisizione vocale esegue l'eliminazione del rumore.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: Proprietà MFPKEY_WMAAECMA_FEATR_NS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309121"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a>\_ \_ Proprietà NS MFPKEY WMAAECMA featr \_

Specifica se il DSP di acquisizione vocale esegue l'eliminazione del rumore.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

1

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

L'eliminazione del rumore è un componente DSP (Digital Signal Processing) che elimina o riduce i rumori di fondo fissi nel segnale audio. L'eliminazione del rumore viene applicata dopo l'elaborazione di annullamenti acustici (AEC) e della matrice microfonica.

Questa proprietà può includere i valori seguenti.



| Valore | Descrizione                |
|-------|----------------------------|
| 0     | Disabilitare l'eliminazione del rumore. |
| 1     | Abilitare l'eliminazione del rumore.  |



 

Il valore predefinito di questa proprietà è 1 (abilitato). Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.

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

 

 
