---
description: Imposta la tolleranza, in millisecondi, utilizzata quando l'origine multimediale ASF esegue la ricerca iterativa.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: Proprietà MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320667"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance \_ , \_ Proprietà in millisecondi

Imposta la tolleranza, in millisecondi, utilizzata quando l'origine multimediale ASF esegue la ricerca iterativa.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**ULONG**

\_UI4 VT

**ulVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare l'origine del supporto ASF. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Questa proprietà si applica solo quando è abilitata la ricerca iterativa. Per ulteriori informazioni, vedere [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

L'algoritmo di ricerca iterativo si interrompe se trova un pacchetto la cui distanza dal tempo di ricerca rientra nella tolleranza specificata. Il valore predefinito è 8000 millisecondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




