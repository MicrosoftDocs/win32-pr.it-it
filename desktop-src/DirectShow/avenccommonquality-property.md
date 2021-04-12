---
description: Specifica il livello di qualità per la codifica.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Proprietà AVEncCommonQuality (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482509"
---
# <a name="avenccommonquality-property"></a>Proprietà AVEncCommonQuality

Specifica il livello di qualità per la codifica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonQuality**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà presenta l'intervallo seguente.



| Valore | Descrizione                           |
|-------|---------------------------------------|
| 0     | Qualità minima, dimensioni di output inferiori. |
| 100   | Qualità massima, dimensioni di output maggiori.  |



 

## <a name="remarks"></a>Commenti

Questa proprietà controlla il livello di qualità quando il codificatore non usa una velocità in bit vincolata. La proprietà [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) determina se la velocità in bit è vincolata.

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

 

 




