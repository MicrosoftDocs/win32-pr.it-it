---
description: Specifica la velocità in bit media del flusso audio codificato, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica CBR (Constant Bit Rate) e VBR (Variable Bit Rate).
ms.assetid: 9513ad64-2de9-497d-86ce-46cfdf87e0f8
title: Proprietà AVEncAudioMeanBitRate (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7b0d1ad6cfde3aee4ec9c747feb8d692c3917332808e40e3d5f76e3d01ce21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079471"
---
# <a name="avencaudiomeanbitrate-property"></a>AVEncAudioMeanBitRate - proprietà

Specifica la velocità in bit media del flusso audio codificato, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica CBR (Constant Bit Rate) e VBR (Variable Bit Rate).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonMeanBitRate**

## <a name="property-value"></a>Valore proprietà

I codificatori possono implementare questa proprietà come set enumerato o come intervallo lineare.

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

 

 




