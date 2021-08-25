---
description: Contrassegna il frame corrente come fotogramma LTR.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: CODECAPI_AVEncVideoMarkLTRFrame proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a62f7bed0fd913dd17e06055ad259f4c8ed7037d90df2ecc53100e14ec4e505a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606431"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>CODECAPI \_ AVEncVideoMarkLTRFrame - proprietà

Contrassegna il frame corrente come fotogramma LTR.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoMarkLTRFrame**

## <a name="remarks"></a>Commenti

**Codificatori H.264/AVC:**

Il valore di questo controllo è il valore della sintassi H.264 *LongTermFramIdx* associato al frame corrente. Se il frame corrente non si trova nel livello di base, ad esempio *\_ l'ID* temporale dell'elemento della sintassi non è uguale a 0, questa proprietà si applica al frame del livello di base successivo in ordine di codifica.

Questa proprietà non deve essere chiamata se è stata emessa una chiamata in sospeso per contrassegnare un fotogramma LTR usando la proprietà CODECAPI AVEncVideoMarkLTRFrame e il codificatore non ha ancora contrassegnato un frame come \_ LTR. In altre parole, il codificatore non deve accodare le richieste CODECAPI \_ AVEncVideoMarkLTRFrame. Se viene inviata una richiesta \_ CODECAPI AVEncVideoMarkLTRFrame mentre un'altra richiesta CODECAPI AVEncVideoMarkLTRFrame è ancora in sospeso, la richiesta precedente deve essere \_ eliminata.

La proprietà CODECAPI \_ AVEncVideoMarkLTRFrame è dinamica e può essere impostata durante la sessione di codifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                   |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




