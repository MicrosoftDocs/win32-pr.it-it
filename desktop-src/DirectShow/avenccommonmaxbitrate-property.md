---
description: Specifica la velocità in bit massima, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).
ms.assetid: 053fdad0-dc5f-4af1-84a6-bb7c0dac7e79
title: Proprietà AVEncCommonMaxBitRate (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03844935e909591b2fe3c7244db79e77e7936f1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876898"
---
# <a name="avenccommonmaxbitrate-property"></a>Proprietà AVEncCommonMaxBitRate

Specifica la velocità in bit massima, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonMaxBitRate**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

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

 

 




