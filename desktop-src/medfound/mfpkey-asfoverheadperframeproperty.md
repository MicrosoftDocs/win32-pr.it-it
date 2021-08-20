---
description: Specifica l'overhead, in byte per pacchetto, necessario per il contenitore usato per archiviare il contenuto compresso.
ms.assetid: 73ec52de-c74a-45b3-a453-7f32510b4484
title: MFPKEY_ASFOVERHEADPERFRAME proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c99c50a305219d0548007755d6b6ba27239e39bef5cb47d61ff3d665dfa47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874082"
---
# <a name="mfpkey_asfoverheadperframe-property"></a>Proprietà MFPKEY \_ ASFOVERHEADPERFRAME

Specifica l'overhead, in byte per pacchetto, necessario per il contenitore usato per archiviare il contenuto compresso.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVPacketOverhead

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

17

## <a name="remarks"></a>Commenti

Se si usa la struttura di file ASF (Advanced Systems Format), non modificare questo valore rispetto all'impostazione predefinita. Se i dati non vengono archiviati in un file ASF, è necessario impostare questo valore su 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




