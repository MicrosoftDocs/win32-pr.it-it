---
description: Specifica se il DSP di acquisizione vocale esegue la pre-elaborazione della matrice di microfoni.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: Proprietà MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309126"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a>\_ \_ \_ Proprietà Preproc di MFPKEY WMAAECMA featr MICARR \_

Specifica se il DSP di acquisizione vocale esegue la pre-elaborazione della matrice di microfoni.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

VARIANT \_ true

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

La pre-elaborazione può rimuovere i toni stazionari che interferiscono con l'elaborazione, ad esempio un tono con un passo fisso.

Questa proprietà può includere i valori seguenti.



| Valore          | Descrizione            |
|----------------|------------------------|
| VARIANTE \_ false | Disabilitare la pre-elaborazione. |
| VARIANT \_ true  | Abilitare la pre-elaborazione.  |



 

Il valore predefinito di questa proprietà è VARIANT \_ true (Enabled). Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.

Il DSP usa questa proprietà solo quando è abilitata l'elaborazione della matrice microfonica.

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

 

 
