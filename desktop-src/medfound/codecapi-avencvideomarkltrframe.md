---
description: Contrassegna il frame corrente come frame LTR.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: Proprietà CODECAPI_AVEncVideoMarkLTRFrame (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524626"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>Proprietà AVEncVideoMarkLTRFrame di codecapi \_

Contrassegna il frame corrente come frame LTR.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoMarkLTRFrame**

## <a name="remarks"></a>Commenti

**Codificatori H. 264/AVC:**

Il valore di questo controllo corrisponde al valore della sintassi H. 264 *LongTermFramIdx* associato al frame corrente. Se il frame corrente non è nel livello di base, ad esempio l' *\_ ID temporale* dell'elemento della sintassi non è uguale a 0, questa proprietà si applica al frame del livello di base successivo nell'ordine di codifica.

Questa proprietà non deve essere chiamata se è stata eseguita una chiamata in sospeso per contrassegnare un frame LTR usando la proprietà codecapis \_ AVEncVideoMarkLTRFrame e il codificatore non ha ancora contrassegnato un frame come LTR. In altre parole, il codificatore non deve accodare le richieste AVEncVideoMarkLTRFrame di codecapis \_ . Se viene inviata una richiesta AVEncVideoMarkLTRFrame di codecapite \_ mentre un'altra \_ richiesta AVEncVideoMarkLTRFrame di codecapites è ancora in sospeso, la richiesta precedente deve essere eliminata.

La proprietà codecapis \_ AVEncVideoMarkLTRFrame è dinamica e può essere impostata durante la sessione di codifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                   |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




