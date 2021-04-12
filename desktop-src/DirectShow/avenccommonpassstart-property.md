---
description: Avvia il primo passaggio di codifica.
ms.assetid: a062be3f-7806-4f1c-b98e-2c9ed31f010c
title: Proprietà AVEncCommonPassStart (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d5be37fc4866aea6f442d4d8a2c0f74c6609cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401299"
---
# <a name="avenccommonpassstart-property"></a>Proprietà AVEncCommonPassStart

Avvia il primo passaggio di codifica.

Questa proprietà è di sola scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonPassStart**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è il passaggio di codifica da avviare. Per ottenere l'intervallo di valori supportati, eseguire una query sulla proprietà [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md) del codificatore.

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

 

 




