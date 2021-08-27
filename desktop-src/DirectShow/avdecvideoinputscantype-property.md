---
description: Specifica la modalità di interlacciazione del flusso video decodificato.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Proprietà AVDecVideoInputScanType (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b86c9499019cdc07f095bf65be5817b828c78d277b02810bc1612cc0365edce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108701"
---
# <a name="avdecvideoinputscantype-property"></a>AVDecVideoInputScanType - proprietà

Specifica la modalità di interlacciazione del flusso video decodificato.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecVideoInputScanType**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro [**dell'enumerazione eAVDecVideoInputScanType.**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)

## <a name="remarks"></a>Commenti

I 16 bit superiori del valore contengono la larghezza e i 16 bit inferiori contengono l'altezza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server desktop apps UWP apps (App desktop UWP di Windows 2000 \[ \| Server)\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

