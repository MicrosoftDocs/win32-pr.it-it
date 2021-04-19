---
title: Proprietà SAMILangCount di IWMPClosedCaption2
description: La proprietà SAMILangCount ottiene il numero di lingue supportate dal file SAMI corrente.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Finestra delle proprietà di SAMILangCount Media Player
- Proprietà di SAMILangCount Media Player Windows, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player, proprietà SAMILangCount
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
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332493"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a>Proprietà IWMPClosedCaption2:: SAMILangCount

La proprietà **SAMILangCount** ottiene il numero di lingue supportate dal file Sami corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il numero di lingue supportate.

## <a name="remarks"></a>Commenti

Questa proprietà restituisce 0, a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer. openState è uguale a 13).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. SAMILang (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2. getSAMILangName (VB e C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





