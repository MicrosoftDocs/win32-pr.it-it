---
description: Specifica se l'applicazione richiede prestazioni di codifica in tempo reale.
ms.assetid: 7e98a9f4-113b-45d0-ae55-7dc3f2af099e
title: Proprietà AVEncCommonRealTime (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a03e51da1a088603273da3d083573e5921edf7a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304239"
---
# <a name="avenccommonrealtime-property"></a>Proprietà AVEncCommonRealTime

Specifica se l'applicazione richiede prestazioni di codifica in tempo reale.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonRealTime**

## <a name="remarks"></a>Commenti

Per specificare che la codifica deve essere eseguita in tempo reale, impostare questa proprietà su **Variant \_ true**. I codec possono inoltre restituire questa proprietà come funzionalità.

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

 

 




