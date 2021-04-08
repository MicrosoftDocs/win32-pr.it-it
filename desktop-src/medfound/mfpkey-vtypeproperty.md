---
description: Specifica la logica che il codec userà per rilevare il video di origine interlacciato.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: Proprietà MFPKEY_VTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880085"
---
# <a name="mfpkey_vtype-property"></a>\_Proprietà VTYPE di MFPKEY

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
| 0     | Il codec userà la logica di rilevamento dei tipi di frame standard.                                                                                 |
| 1     | Il codec considererà tutti i fotogrammi video di origine come frame interlacciati.                                                                          |
| 2     | Il codec considererà tutti i frame video di origine come campi di video interlacciato.                                                                 |
| 3     | Il codec determina automaticamente se i fotogrammi video di input sono frame o campi interlacciati di video interlacciato.                      |
| 4     | Il codec determina automaticamente se i fotogrammi video di input sono frame progressivi, frame interlacciati o campi di video interlacciato. |



 

Questa proprietà determina il metodo di codifica immagine usato per la codifica video progressiva o interlacciata.

Se non viene specificato alcun tipo di video, il codec userà la codifica del frame progressiva per le sessioni di codifica progressiva e la codifica interlacciata del campo per le sessioni di codifica interlacciate. Il tipo di sessione di codifica video (progressivo o interlacciato) viene impostato tramite la proprietà [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) .

> [!Note]  
> La [proprietà \_ INTERLACEDCODINGENABLED di MFPKEY](mfpkey-interlacedcodingenabledproperty.md) deve essere impostata su Variant \_ true per produrre output interlacciato. in caso contrario, l'impostazione della proprietà VTYPE di MPFKEY non avrà \_ alcun effetto.

 

Quando si codifica il video interlacciato, è possibile specificare diversi metodi di codifica dell'immagine. In genere, il modo più efficiente per codificare video interlacciato consiste nell'usare il metodo interlacciato del campo (2). Se il video di origine contiene un movimento molto ridotto, il metodo interlacciato del frame (1) o il metodo di frame/campo automatico (2) potrebbe essere più appropriato.

Quando si codificano contenuti misti (contenenti frame progressivi e interlacciati), è preferibile usare il valore auto frame/Field/progressive Method (4).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




