---
description: Specifica se il decodificatore rilascia i frame intra con frame di riferimento mancanti.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Proprietà AVDecVideoDropPicWithMissingRef (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225378"
---
# <a name="avdecvideodroppicwithmissingref-property"></a>Proprietà AVDecVideoDropPicWithMissingRef

Specifica se il decodificatore rilascia i frame intra con frame di riferimento mancanti.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecVideoDropPicWithMissingRef**

## <a name="remarks"></a>Commenti

Se il Bitstream è danneggiato, un frame potrebbe contenere frame di riferimento mancanti. Se il valore di questa proprietà è **Variant \_ true**, il decodificatore rilascia il frame. Se il valore è **Variant \_ false**, il decodificatore tenta di decodificare il frame, utilizzando uno o più frame adiacenti come frame di riferimento. Il frame decodificato risultante avrà elementi di blocco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




