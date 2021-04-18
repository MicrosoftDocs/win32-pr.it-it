---
title: Proprietà AxWindowsMediaPlayer. openState
description: La proprietà openState ottiene un valore di enumerazione che indica lo stato dell'origine del contenuto.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- Finestra delle proprietà di openState Media Player
- Proprietà openState Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà openState
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
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325867"
---
# <a name="axwindowsmediaplayeropenstate-property"></a>Proprietà AxWindowsMediaPlayer. openState

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

Valore di enumerazione WMPLib. WMPOpenState.

## <a name="remarks"></a>Commenti

Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare. Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi. Non è necessario scrivere codice che si basa sull'ordine di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer. OpenStateChange**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**WMPLib. WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





