---
description: Specifica la logica che il codec userà per rilevare il video di origine interlacciato.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: MFPKEY_VTYPE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f406f0bc91e3431672c2b7f92cc544273e2a64403017a22eb4567054cef0155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973340"
---
# <a name="mfpkey_vtype-property"></a>Proprietà VTYPE MFPKEY \_

Specifica la logica che il codec userà per rilevare il video di origine interlacciato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCVType

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata su uno dei valori seguenti.



| Valore | Descrizione                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Il codec userà la logica di rilevamento del tipo di frame standard.                                                                                 |
| 1     | Il codec considera tutti i fotogrammi video di origine come fotogrammi interlacciati.                                                                          |
| 2     | Il codec considera tutti i fotogrammi video di origine come campi del video interlacciato.                                                                 |
| 3     | Il codec determinerà automaticamente se i fotogrammi video di input sono fotogrammi interlacciati o campi di video interlacciati.                      |
| 4     | Il codec determinerà automaticamente se i fotogrammi video di input sono fotogrammi progressivi, fotogrammi interlacciati o campi di video interlacciati. |



 

Questa proprietà determina il metodo di codifica delle immagini usato per la codifica video progressiva o interlacciata.

Se non viene specificato alcun tipo di video, il codec userà la codifica dei fotogrammi progressivi per le sessioni di codifica progressiva e la codifica interlacciata di campo per le sessioni di codifica interlacciata. Il tipo di sessione di codifica video (progressiva o interlacciata) viene impostato usando la proprietà [MFPKEY \_ INTERLACEDCODINGENABLED.](mfpkey-interlacedcodingenabledproperty.md)

> [!Note]  
> La [proprietà MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) deve essere impostata su VARIANT TRUE per produrre output interlacciato. In caso contrario, l'impostazione della proprietà VTYPE MPFKEY non avrà \_ \_ alcun effetto.

 

Quando il video interlacciato viene codificato, è possibile specificare diversi metodi di codifica delle immagini. In genere il modo più efficiente per codificare video interlacciato è usare il metodo interlacciato di campo (2). Se il video di origine contiene pochissimo movimento, il metodo interlacciato dei fotogrammi (1) o il metodo frame/campo automatico (2) potrebbe essere più adatto.

Quando si codifica contenuto misto (che contiene fotogrammi sia progressivi che interlacciati), è meglio usare il metodo frame/campo/progressivo automatico (4).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




