---
title: Controls. pause (metodo)
description: Il metodo pause sospende la riproduzione dell'elemento multimediale. | Controls. pause (metodo)
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- sospendere il metodo Windows Media Player
- Metodo pause Media Player Windows, classe Controls
- Classe Controls Media Player Windows, metodo pause
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331244"
---
# <a name="controlspause-method"></a>Controls. pause (metodo)

Il metodo **pause** sospende la riproduzione dell'elemento multimediale.

## <a name="syntax"></a>Sintassi


```JScript
Controls.pause()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando un file viene sospeso, Windows Media Player non cede alcuna risorsa di sistema, ad esempio il dispositivo audio.

Alcuni tipi di supporto non possono essere sospesi, ad esempio i flussi live. Per determinare se un tipo di supporto specifico può essere sospeso, utilizzare i *controlli*. non **disponibile (' pause ')**.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che utilizza **pause** per sospendere la riproduzione. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
">
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Controls. disavailable**](controls-isavailable.md)
</dt> </dl>

 

 





