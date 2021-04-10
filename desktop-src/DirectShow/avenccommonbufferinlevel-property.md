---
description: Specifica il livello iniziale del buffer di codifica, in bit. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: Proprietà AVEncCommonBufferInLevel (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125253"
---
# <a name="avenccommonbufferinlevel-property"></a>Proprietà AVEncCommonBufferInLevel

Specifica il livello iniziale del buffer di codifica, in bit. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonBufferInLevel**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Commenti

Per il video MPEG questa proprietà definisce la completezza del verificatore video buffer iniziale (VBV). Supporta la concatenazione dei flussi durante la codifica.

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

 

 




