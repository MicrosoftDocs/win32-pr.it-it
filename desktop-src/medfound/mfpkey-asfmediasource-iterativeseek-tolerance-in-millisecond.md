---
description: Imposta la tolleranza, in millisecondi, usata quando l'origine del supporto ASF esegue la ricerca iterativa.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8cfc1ef656e1cff3da4bb33f19a3c2176729035f94a194a4ede21354f5dbc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874132"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance In \_ \_ MilliSecond - proprietà

Imposta la tolleranza, in millisecondi, usata quando l'origine del supporto ASF esegue la ricerca iterativa.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**Ulong**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare l'origine multimediale ASF. Per impostare la proprietà, passare un **puntatore IPropertyStore** al resolver di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale.](configuring-a-media-source.md)

Questa proprietà si applica solo quando è abilitata la ricerca iterativa. Per altre informazioni, vedere [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex.](mfpkey-asfmediasource-iterativeseekifnoindex.md)

L'algoritmo di ricerca iterativo si interrompe se trova un pacchetto la cui distanza dal tempo di ricerca rientra nella tolleranza specificata. Il valore predefinito è 8000 millisecondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




