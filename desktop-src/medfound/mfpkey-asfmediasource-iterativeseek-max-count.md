---
description: Imposta il numero massimo di iterazioni di ricerca che l'origine multimediale ASF userà quando esegue la ricerca iterativa.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: MFPKEY_ASFMediaSource_IterativeSeek_Max_Count proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183ed13143260f9d6d5de67ba38fcff27ebfd5a6afb01c75a07e92497d571cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874254"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a>Proprietà MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count

Imposta il numero massimo di iterazioni di ricerca che l'origine multimediale ASF userà quando esegue la ricerca iterativa.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**Ulong**

Interfaccia utente \_ VT4

**ulVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare l'origine multimediale ASF. Per impostare la proprietà, passare un **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

Questa proprietà si applica solo quando è abilitata la ricerca iterativa. Per altre informazioni, vedere [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

L'intervallo valido di questa proprietà è \[ compreso tra 1 e 10, \] inclusi. Con un numero più elevato, la ricerca iterativa tende a essere più accurata, ma richiede più tempo.

Il valore predefinito è 5.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




