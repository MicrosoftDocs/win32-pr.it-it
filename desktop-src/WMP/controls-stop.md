---
title: Metodo Controls.stop
description: Il metodo stop arresta la riproduzione dell'elemento multimediale. | Metodo Controls.stop
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- Metodo stop Windows Media Player
- Metodo stop Windows Media Player , classe Controls
- Classe Controls Windows Media Player, metodo stop
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
ms.openlocfilehash: b882f462903c2c5f75a3655cd26b927e7439043828dad41fcce7d0e64e4ce812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580160"
---
# <a name="controlsstop-method"></a>Metodo Controls.stop

Il **metodo stop** arresta la riproduzione dell'elemento multimediale.

## <a name="syntax"></a>Sintassi


```JScript
Controls.stop()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo Windows Media Player rilasciare tutte le risorse di sistema in uso, ad esempio il dispositivo audio. L'elemento multimediale corrente, tuttavia, non viene rilasciato.

Quando il giocatore viene arrestato, la traccia si riavvolge all'inizio. La **chiamata di** play inizierà quindi la riproduzione del clip dall'inizio. Per arrestare un'operazione di riproduzione senza modificare la posizione corrente, usare il **metodo pause.**

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che usa **stop per** arrestare la riproduzione. **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Controls.next**](controls-next.md)
</dt> <dt>

[**Controls.pause**](controls-pause.md)
</dt> <dt>

[**Controls.previous**](controls-previous.md)
</dt> </dl>

 

 





