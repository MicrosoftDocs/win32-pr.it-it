---
description: Specifica se l'applicazione richiede prestazioni di codifica in tempo reale.
ms.assetid: 7e98a9f4-113b-45d0-ae55-7dc3f2af099e
title: Proprietà AVEncCommonRealTime (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b718f4f58d230448689700fc2e681c109e645d48cb33eb1788e45ac607350951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403891"
---
# <a name="avenccommonrealtime-property"></a>AVEncCommonRealTime - proprietà

Specifica se l'applicazione richiede prestazioni di codifica in tempo reale.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonRealTime**

## <a name="remarks"></a>Commenti

Per specificare che la codifica deve essere eseguita in tempo reale, impostare questa proprietà su **VARIANT \_ TRUE.** I codec possono anche restituire questa proprietà come funzionalità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows app desktop di Windows 2000 Server \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




