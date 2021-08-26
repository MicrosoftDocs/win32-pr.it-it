---
description: Abilita o disabilita l'equalizzazione della voce in un decodificatore audio o in un processore di segnale digitale (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Proprietà AVDSPLoudnessEqualization (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61696b51996d6fe57cf15372d511704e2dad482f0a5e99eb165795f56256656a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052831"
---
# <a name="avdsploudnessequalization-property"></a>AVDSPLoudnessEqualization - proprietà

Abilita o disabilita l'equalizzazione della voce in un decodificatore audio o in un processore di segnale digitale (DSP).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDSPLoudnessEqualization**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro [**dell'enumerazione eAVDSPLoudnessEqualization.**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)

## <a name="remarks"></a>Commenti

L'equalizzazione della voce è un processo DSP che mantiene un livello di volume coerente quando il flusso audio cambia.

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

 

 




