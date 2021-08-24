---
description: Specifica il numero di campi da ignorare durante la codifica.
ms.assetid: 82f2a2c1-52ff-410d-b5da-b2419c0adfe3
title: Proprietà AVEncVideoNoOfFieldsToSkip (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 908a169b6f8ea868f7959afbd8fc90afa0b7a129b90674791990a156e67af948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342131"
---
# <a name="avencvideonooffieldstoskip-property"></a>AVEncVideoNoOfFieldsToSkip - proprietà

Specifica il numero di campi da ignorare durante la codifica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoNoOfFieldsToSkip**

## <a name="remarks"></a>Commenti

Per il video progressivo, impostare questa proprietà su due volte il numero di fotogrammi da ignorare.

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

 

 




