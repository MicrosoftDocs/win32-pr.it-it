---
title: Proprietà del volume IWMPSettings
description: La proprietà volume ottiene o imposta il volume di riproduzione corrente.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Proprietà volume Windows Media Player
- Proprietà del volume Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player , proprietà del volume
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2077547dd00b5c75b6ca77a966190db2bb3bb1bcde61d1f5c5b84c794af84e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568398"
---
# <a name="iwmpsettingsvolume-property"></a>Proprietà IWMPSettings::volume

La **proprietà volume** ottiene o imposta il volume di riproduzione corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System.Int32** che rappresenta il livello del volume, compreso tra 0 e 100.

## <a name="remarks"></a>Commenti

Il valore zero specifica che non è presente alcun volume (disattivato). Il valore 100 specifica il volume completo. Se non viene specificato alcun valore per questa proprietà, per impostazione predefinita viene impostata l'ultima impostazione del volume stabilita per Windows Media Player.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





