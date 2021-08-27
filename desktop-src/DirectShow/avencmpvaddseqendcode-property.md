---
description: Specifica se il codificatore aggiunge un codice finale della sequenza alla fine del flusso. Questa proprietà si applica ai codificatori video MPEG.
ms.assetid: ef606207-2ee3-420b-afae-67c764e05e54
title: Proprietà AVEncMPVAddSeqEndCode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba3d757bd3023ca9539172c96f6f276bc1833eb7c4e24c8b2bb3adc6038d77c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087591"
---
# <a name="avencmpvaddseqendcode-property"></a>AVEncMPVAddSeqEndCode - proprietà

Specifica se il codificatore aggiunge un codice finale della sequenza alla fine del flusso. Questa proprietà si applica ai codificatori video MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncMPVAddSeqEndCode**

## <a name="remarks"></a>Commenti

Se il valore è **VARIANT \_ TRUE,** il codificatore aggiunge un codice finale della sequenza alla fine del flusso.

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

 

 




