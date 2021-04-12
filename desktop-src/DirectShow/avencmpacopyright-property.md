---
description: Specifica l'impostazione predefinita per il bit di copyright nel flusso audio MPEG-1. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Proprietà AVEncMPACopyright (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401278"
---
# <a name="avencmpacopyright-property"></a>Proprietà AVEncMPACopyright

Specifica l'impostazione predefinita per il bit di copyright nel flusso audio MPEG-1. Questa proprietà si applica ai codificatori audio MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncMPACopyright**

## <a name="property-value"></a>Valore proprietà

Questa proprietà può includere i valori seguenti.



| Valore          | Descrizione           |
|----------------|-----------------------|
| VARIANTE \_ false | Il copyright è disattivato. |
| VARIANT \_ true  | Il copyright è il bit on.  |



 

## <a name="remarks"></a>Commenti

Il codificatore potrebbe eseguire l'override di questa impostazione, in base al contenuto del flusso di input.

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

 

 




