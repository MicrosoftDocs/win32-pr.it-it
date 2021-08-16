---
title: AxWindowsMediaPlayer.openState - proprietà
description: La proprietà openState ottiene un valore di enumerazione che indica lo stato dell'origine del contenuto.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- Proprietà openState Windows Media Player
- Proprietà openState Windows Media Player , classe AxWindowsMediaPlayer
- La classe AxWindowsMediaPlayer Windows Media Player , proprietà openState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fa09451bf323a9f30afeddf7b2d003183a1eba7b0999a79fb42c70e1417013
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573571"
---
# <a name="axwindowsmediaplayeropenstate-property"></a>AxWindowsMediaPlayer.openState - proprietà

La proprietà openState ottiene un valore di enumerazione che indica lo stato dell'origine del contenuto.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a>Valore proprietà

Valore di enumerazione WMPLib.WMPOpenState.

## <a name="remarks"></a>Commenti

Windows Media Player non è garantito che gli stati si verifichino in un ordine particolare. Inoltre, non tutti gli stati si verificano necessariamente durante una sequenza di eventi. È consigliabile non scrivere codice che si basa sull'ordine di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer.OpenStateChange**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**WMPLib.WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





