---
title: Proprietà volume IWMPSettings
description: La proprietà volume Ottiene o imposta il volume di riproduzione corrente.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Proprietà volume Media Player Windows
- Proprietà volume Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà volume
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
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325962"
---
# <a name="iwmpsettingsvolume-property"></a>Proprietà IWMPSettings:: volume

La proprietà **volume** Ottiene o imposta il volume di riproduzione corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il livello del volume, compreso tra 0 e 100.

## <a name="remarks"></a>Commenti

Un valore pari a zero non specifica alcun volume (disattivato). Il valore 100 specifica il volume completo. Se per questa proprietà non viene specificato alcun valore, per impostazione predefinita viene impostata l'ultima impostazione del volume stabilita per Windows Media Player.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





