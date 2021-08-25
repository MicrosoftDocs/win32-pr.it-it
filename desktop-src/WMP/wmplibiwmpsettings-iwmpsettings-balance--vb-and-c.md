---
title: Proprietà di bilanciamento IWMPSettings
description: La proprietà balance ottiene o imposta il bilanciamento stereo corrente.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- proprietà balance Windows Media Player
- proprietà balance Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player proprietà , balance
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d519d656be6b4974e2b4dd2707aafb2bb153f6b26bafe75de948d5e50c67b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861084"
---
# <a name="iwmpsettingsbalance-property"></a>Proprietà IWMPSettings::balance

La **proprietà balance** ottiene o imposta il bilanciamento stereo corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.Int32** che rappresenta il valore di saldo. Questo valore può essere compreso tra 100 e 100. Il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Il valore zero indica che l'audio viene riprodotto con un volume uguale su entrambi i canali sinistro e destro. Il valore 100 indica che l'audio viene riprodotto solo sul canale sinistro. Il valore 100 indica che l'audio viene riprodotto solo sul canale destro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive.<br/>                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





