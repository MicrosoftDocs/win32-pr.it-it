---
title: Proprietà IWMPClosedCaption2 SAMILangCount
description: La proprietà SAMILangCount ottiene il numero di lingue supportate dal file SAMI corrente.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Proprietà SAMILangCount Windows Media Player
- Proprietà SAMILangCount Windows Media Player, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player , proprietà SAMILangCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b85ce04bd672f0219b8dd96f91172241689a80042a37a7680e2f8e26b65c85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900001"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a>Proprietà IWMPClosedCaption2::SAMILangCount

La **proprietà SAMILangCount** ottiene il numero di lingue supportate dal file SAMI corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System.Int32** che rappresenta il numero di lingue supportate.

## <a name="remarks"></a>Commenti

Questa proprietà restituisce 0 a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer.openState è uguale a 13).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di sottotitoli codificati a supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.SAMILang (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2.getSAMILangName (VB e C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





