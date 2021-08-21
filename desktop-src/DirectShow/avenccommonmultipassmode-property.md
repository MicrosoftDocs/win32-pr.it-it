---
description: Specifica il numero di passaggi di codifica supportati dal codificatore.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Proprietà AVEncCommonMultipassMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6fb909e58dbdfd5d1431d0101365db78efa83fd68e9299b8578f19770787fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159809"
---
# <a name="avenccommonmultipassmode-property"></a>AVEncCommonMultipassMode - proprietà

Specifica il numero di passaggi di codifica supportati dal codificatore.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonMultipassMode**

## <a name="property-value"></a>Valore proprietà

Questa proprietà viene restituita come intervallo di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Commenti

La latenza di decodifica è definita come la quantità di dati che il decodificatore deve buffer. Ad esempio, l'impostazione di questa proprietà su **VARIANT \_ TRUE** in un codificatore video MPEG limita i tipi di strutture GOP che il codificatore può usare.

Per impostare il passaggio di codifica corrente, impostare la [**proprietà AVEncCommonPassStart.**](avenccommonpassstart-property.md)

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

 

 




