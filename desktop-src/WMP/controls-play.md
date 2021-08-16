---
title: Metodo Controls.play
description: Il metodo play fa sì che l'elemento multimediale corrente inizi la riproduzione o riprendi la riproduzione di un elemento sospeso.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- Metodo play Windows Media Player
- Metodo play Windows Media Player , classe Controls
- Classe Controls Windows Media Player, metodo play
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
ms.openlocfilehash: 86ce3c1572515b320a62b1b3c76aac72e44101e21f3b0f89d7c3356046ea95f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997451"
---
# <a name="controlsplay-method"></a>Metodo Controls.play

Il **metodo play** fa sì che l'elemento multimediale corrente inizi la riproduzione o riprendi la riproduzione di un elemento sospeso.

## <a name="syntax"></a>Sintassi


```JScript
Controls.play()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se questo metodo viene chiamato durante l'inoltro rapido o il riavvolgimento rapido, il valore *di* Impostazioni . **rate** è impostato su 1.0.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che usa **play** per riprodurre l'elemento multimediale corrente. **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> </dl>

 

 





