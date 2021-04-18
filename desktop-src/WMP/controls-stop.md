---
title: Metodo Controls. Stop
description: Il metodo Stop interrompe la riproduzione dell'elemento multimediale. | Metodo Controls. Stop
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- arresta il metodo Windows Media Player
- Metodo Stop Media Player Windows, classe Controls
- Classe Controls Media Player Windows, metodo Stop
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327388"
---
# <a name="controlsstop-method"></a>Metodo Controls. Stop

Il metodo **Stop** interrompe la riproduzione dell'elemento multimediale.

## <a name="syntax"></a>Sintassi


```JScript
Controls.stop()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo fa in modo che Windows Media Player rilasciare tutte le risorse di sistema utilizzate, ad esempio il dispositivo audio. L'elemento multimediale corrente, tuttavia, non viene rilasciato.

Quando il lettore viene arrestato, la traccia viene ricaricata fino all'inizio. La chiamata di **Play** inizierà la riproduzione della clip dall'inizio. Per arrestare un'operazione di riproduzione senza modificare la posizione corrente, usare il metodo **pause** .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che utilizza **Stop** per arrestare la riproduzione. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
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

[**Controlli. Next**](controls-next.md)
</dt> <dt>

[**Controls. pause**](controls-pause.md)
</dt> <dt>

[**Controlli. Previous**](controls-previous.md)
</dt> </dl>

 

 





