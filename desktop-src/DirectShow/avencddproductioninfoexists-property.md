---
description: Specifica il flag di informazioni di produzione audio in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Proprietà AVEncDDProductionInfoExists (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d0341cf97b4641dc2ece7e93408e527458235620b32b7e25abe583a67c2ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103471"
---
# <a name="avencddproductioninfoexists-property"></a>AVEncDDProductionInfoExists - proprietà

Specifica il flag di informazioni di produzione audio in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncDDProductionInfoExists**

## <a name="remarks"></a>Commenti

Se il valore è **VARIANT \_ TRUE,** le impostazioni del livello di combinazione e del tipo di stanza sono valide. Specificare queste impostazioni con le [**proprietà AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) e [**AVEncDDProductionMixLevel.**](avencddproductionmixlevel-property.md)

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

 

 




