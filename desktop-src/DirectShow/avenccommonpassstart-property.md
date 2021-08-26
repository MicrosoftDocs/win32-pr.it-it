---
description: Avvia il primo passaggio di codifica.
ms.assetid: a062be3f-7806-4f1c-b98e-2c9ed31f010c
title: Proprietà AVEncCommonPassStart (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7830537e6345d43927c7009e0e3ec9148505217818e981d7354a100a4ff2d68e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000141"
---
# <a name="avenccommonpassstart-property"></a>AVEncCommonPassStart - proprietà

Avvia il primo passaggio di codifica.

Questa proprietà è di sola scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonPassStart**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è il passaggio di codifica da avviare. Per ottenere l'intervallo di valori supportati, eseguire una query sulla [**proprietà AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md) del codificatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | app \[ desktop UWP di Windows 2000 Server \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




