---
title: Proprietà captioningId di IWMPClosedCaption
description: La proprietà IWMPClosedCaption Ottiene o imposta il nome dell'elemento HTML che visualizza la didascalia.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- Finestra delle proprietà di captioningId Media Player
- Proprietà di captioningId Media Player Windows, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player, proprietà captioningId
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329284"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a>Proprietà IWMPClosedCaption:: captioningId

La proprietà **IWMPClosedCaption** Ottiene o imposta il nome dell'elemento HTML che visualizza la didascalia.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che rappresenta l'ID dell'elemento HTML.

## <a name="remarks"></a>Commenti

Il nome dell'elemento specificato può essere qualsiasi elemento HTML nella pagina Web, purché supporti l'attributo **innerHTML** . Se la pagina Web contiene più frame, il nome dell'elemento può fare riferimento solo a un elemento nello stesso frame del controllo Media Player di Windows.

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

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





