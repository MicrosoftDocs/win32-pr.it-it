---
title: Proprietà SAMIStyleCount di IWMPClosedCaption2
description: La proprietà SAMIStyleCount ottiene il numero di stili supportati dal file SAMI corrente.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Finestra delle proprietà di SAMIStyleCount Media Player
- Proprietà di SAMIStyleCount Media Player Windows, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player, proprietà SAMIStyleCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332491"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a>Proprietà IWMPClosedCaption2:: SAMIStyleCount

La proprietà **SAMIStyleCount** ottiene il numero di stili supportati dal file Sami corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il numero di stili.

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

[**IWMPClosedCaption. SAMIStyle (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2. getSAMIStyleName (VB e C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





