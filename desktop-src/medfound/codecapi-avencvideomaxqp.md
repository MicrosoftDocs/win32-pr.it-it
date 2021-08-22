---
description: Specifica il valore QP massimo supportato dal codificatore.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: CODECAPI_AVEncVideoMaxQP proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d95f605dbb647ed96ec40e89870c761400a6d414cd354cb0197bb316bd3cf27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606321"
---
# <a name="codecapi_avencvideomaxqp-property"></a>CODECAPI \_ AVEncVideoMaxQP - proprietà

Specifica il valore QP massimo supportato dal codificatore.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoMaxQP**

## <a name="remarks"></a>Commenti

**Codificatori H.264/AVC:**

Il codificatore deve [**supportare GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Si tratta di una proprietà statica che indica che può essere impostata solo prima dell'avvio della sessione di codifica.

Il valore predefinito deve essere il valore QP massimo consentito dallo standard di codifica corrispondente. Ad esempio, i codificatori H.264 devono avere un valore predefinito di 51.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                   |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md)
</dt> </dl>

 

