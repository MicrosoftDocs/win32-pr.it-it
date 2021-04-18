---
title: Metodo Controls. Play
description: Il metodo Play causa l'avvio della riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- Metodo di riproduzione Media Player Windows
- Metodo Play Media Player Windows, classe Controls
- Classe Controls Media Player Windows, metodo Play
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331242"
---
# <a name="controlsplay-method"></a>Metodo Controls. Play

Il metodo **Play** causa l'avvio della riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.

## <a name="syntax"></a>Sintassi


```JScript
Controls.play()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se questo metodo viene chiamato durante l'avanzamento rapido o il riavvolgimento, il valore delle *Impostazioni*. **rate** è impostato su 1,0.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che utilizza **Play** per riprodurre l'elemento multimediale corrente. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
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
</dt> </dl>

 

 





