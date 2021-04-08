---
description: Specifica il numero di passaggi di codifica supportati dal codificatore.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Proprietà AVEncCommonMultipassMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876897"
---
# <a name="avenccommonmultipassmode-property"></a>Proprietà AVEncCommonMultipassMode

Specifica il numero di passaggi di codifica supportati dal codificatore.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonMultipassMode**

## <a name="property-value"></a>Valore proprietà

Questa proprietà viene restituita come un intervallo di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Commenti

La latenza di decodifica viene definita come la quantità di dati che il decodificatore deve memorizzare nel buffer. Se ad esempio si imposta questa proprietà su **Variant \_ true** in un codificatore video MPEG, vengono limitati i tipi di strutture GOP che il codificatore può utilizzare.

Per impostare il passaggio di codifica corrente, impostare la proprietà [**AVEncCommonPassStart**](avenccommonpassstart-property.md) .

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

 

 




