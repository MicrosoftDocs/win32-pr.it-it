---
description: Specifica il numero di volte in cui il DSP di acquisizione vocale esegue l'eliminazione dell'eco acustico (AES) sul segnale residuo.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: Proprietà MFPKEY_WMAAECMA_FEATR_AES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5da7505a259a51ca8456f3caffa153790649320
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309136"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a>\_ \_ Proprietà AES MFPKEY WMAAECMA featr \_

Specifica il numero di volte in cui il DSP di acquisizione vocale esegue l'eliminazione dell'eco acustico (AES) sul segnale residuo.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il DSP di acquisizione vocale può eseguire AES sul segnale residuo dopo l'annullamento di Echo. Il valore di questa proprietà può essere 0, 1 o 2. Il valore predefinito è 0. Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.

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

 

 
