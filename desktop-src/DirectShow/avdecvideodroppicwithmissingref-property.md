---
description: Specifica se il decodificatore elimina i fotogrammi intra con fotogrammi di riferimento mancanti.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Proprietà AVDecVideoDropPicWithMissingRef (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac5e8c02c63c977d8d5a8e47bb5d6f878c538364ac2fe5b65c1e691c84ca23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000321"
---
# <a name="avdecvideodroppicwithmissingref-property"></a>AVDecVideoDropPicWithMissingRef - proprietà

Specifica se il decodificatore elimina i fotogrammi intra con fotogrammi di riferimento mancanti.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecVideoDropPicWithMissingRef**

## <a name="remarks"></a>Commenti

Se il flusso di bit è danneggiato, un frame potrebbe avere frame di riferimento mancanti. Se il valore di questa proprietà è **VARIANT \_ TRUE,** il decodificatore elimina il frame. Se il valore è **VARIANT \_ FALSE,** il decodificatore tenta di decodificare il frame, usando uno o più fotogrammi vicini come frame di riferimento. Il frame decodificato risultante avrà elementi di blocco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop app \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 App desktop UWP per le app \[ desktop di 2000 \| Server\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




