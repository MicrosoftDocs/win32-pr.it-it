---
title: Proprietà defaultAudioLanguage IWMPSettings2
description: La proprietà defaultAudioLanguage ottiene l'identificatore delle impostazioni locali (LCID) della lingua audio predefinita specificata in Windows Media Player.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- Proprietà defaultAudioLanguage Windows Media Player
- Proprietà defaultAudioLanguage Windows Media Player, interfaccia IWMPSettings2
- Interfaccia IWMPSettings2 Windows Media Player , proprietà defaultAudioLanguage
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
ms.openlocfilehash: 4f09df11cc53e9b813de2e40e40eca1e31a88afeff0c16ce1f9c0c5ba4745277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331101"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>Proprietà IWMPSettings2::d efaultAudioLanguage

La **proprietà defaultAudioLanguage** ottiene l'identificatore delle impostazioni locali (LCID) della lingua audio predefinita specificata in Windows Media Player.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System.Int32** che rappresenta l'identificatore LCID.

## <a name="remarks"></a>Commenti

Un LCID identifica in modo univoco un particolare dialetto di lingua, denominato impostazioni locali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPControls3.currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings2 (VB e C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





