---
description: Specifica il numero massimo di QP supportato dal codificatore.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: Proprietà CODECAPI_AVEncVideoMaxQP (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305488"
---
# <a name="codecapi_avencvideomaxqp-property"></a>Proprietà AVEncVideoMaxQP di codecapi \_

Specifica il numero massimo di QP supportato dal codificatore.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoMaxQP**

## <a name="remarks"></a>Commenti

**Codificatori H. 264/AVC:**

Il codificatore deve supportare [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Si tratta di una proprietà statica che significa che può essere impostata solo prima dell'avvio della sessione di codifica.

Il valore predefinito deve essere il numero massimo di QP consentito dallo standard di codifica corrispondente. Ad esempio, i codificatori H. 264 avranno un valore predefinito di 51.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                   |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Codecapis \_ AVEncVideoMinQP](codecapi-avencvideominqp.md)
</dt> </dl>

 

