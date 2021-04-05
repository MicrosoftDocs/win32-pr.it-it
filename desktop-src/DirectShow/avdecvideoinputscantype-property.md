---
description: Specifica il modo in cui il flusso video decodificato è interlacciato.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Proprietà AVDecVideoInputScanType (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 560db1cd1cf0238fc9e50257f2f24559e9a94c8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876778"
---
# <a name="avdecvideoinputscantype-property"></a>Proprietà AVDecVideoInputScanType

Specifica il modo in cui il flusso video decodificato è interlacciato.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecVideoInputScanType**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro dell'enumerazione [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) .

## <a name="remarks"></a>Commenti

I 16 bit superiori del valore contengono la larghezza e i 16 bit inferiori contengono l'altezza.

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

 

