---
title: Proprietà defaultAudioLanguage di IWMPSettings2
description: La proprietà defaultAudioLanguage Ottiene l'identificatore delle impostazioni locali (LCID) della lingua audio predefinita specificata in Windows Media Player.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- Finestra delle proprietà di defaultAudioLanguage Media Player
- Proprietà di defaultAudioLanguage Media Player Windows, interfaccia IWMPSettings2
- Interfaccia IWMPSettings2 Windows Media Player, proprietà defaultAudioLanguage
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327478"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>IWMPSettings2::d proprietà efaultAudioLanguage

La proprietà **defaultAudioLanguage** Ottiene l'identificatore delle impostazioni locali (LCID) della lingua audio predefinita specificata in Windows Media Player.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta l'identificatore LCID.

## <a name="remarks"></a>Commenti

Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPControls3. currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings2 (VB e C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





