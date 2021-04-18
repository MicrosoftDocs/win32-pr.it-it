---
title: Proprietà Balance IWMPSettings
description: La proprietà Balance Ottiene o imposta il saldo stereo corrente.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- Proprietà bilancia Media Player di Windows
- Proprietà Balance Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Media Player Windows, Balance (proprietà)
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
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330447"
---
# <a name="iwmpsettingsbalance-property"></a>Proprietà IWMPSettings:: Balance

La proprietà **Balance** Ottiene o imposta il saldo stereo corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il valore di bilanciamento. Questo valore può essere compreso tra 100 e 100. Il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Il valore zero indica che l'audio viene riprodotto in un volume uguale sui canali sinistro e destro. Il valore 100 indica che l'audio viene riprodotto solo sul canale sinistro. Il valore 100 indica che l'audio viene riprodotto solo sul canale destro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva.<br/>                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





