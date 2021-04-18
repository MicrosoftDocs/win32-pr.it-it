---
description: Imposta il numero massimo di iterazioni di ricerca che l'origine multimediale ASF utilizzerà quando esegue la ricerca iterativa.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: Proprietà MFPKEY_ASFMediaSource_IterativeSeek_Max_Count (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320740"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a>\_Proprietà MFPKEY ASFMediaSource \_ IterativeSeek \_ Max \_ Count

Imposta il numero massimo di iterazioni di ricerca che l'origine multimediale ASF utilizzerà quando esegue la ricerca iterativa.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**ULONG**

\_UI4 VT

**ulVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare l'origine del supporto ASF. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Questa proprietà si applica solo quando è abilitata la ricerca iterativa. Per ulteriori informazioni, vedere [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

L'intervallo valido di questa proprietà è \[ 1-10 \] , inclusivo. Con un numero più elevato, la ricerca iterativa tende a essere più precisa, ma richiede più tempo.

Il valore predefinito è 5.

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

 

 




