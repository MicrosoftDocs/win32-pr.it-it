---
description: Specifica l'impostazione predefinita per il bit di copyright nel flusso audio MPEG-1. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Proprietà AVEncMPACopyright (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd747de4f4351e5d540fcf8235194308457e0dcc985500f2743209061cedbdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824271"
---
# <a name="avencmpacopyright-property"></a>AVEncMPACopyright - proprietà

Specifica l'impostazione predefinita per il bit di copyright nel flusso audio MPEG-1. Questa proprietà si applica ai codificatori audio MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncMPACopyright**

## <a name="property-value"></a>Valore proprietà

Questa proprietà può avere i valori seguenti.



| Valore          | Descrizione           |
|----------------|-----------------------|
| VARIANT \_ FALSE | Il bit di copyright è disattivato. |
| VARIANT \_ TRUE  | Il bit di copyright è on.  |



 

## <a name="remarks"></a>Commenti

Il codificatore potrebbe eseguire l'override di questa impostazione, in base al contenuto del flusso di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| app UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 App desktop UWP per le app \[ desktop di 2000 \| Server\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




