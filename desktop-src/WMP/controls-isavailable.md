---
title: Controls.isAvailable
description: La proprietà isAvailable indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. | Controls.isAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Controlli.isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502343b7654241a00e9efb33acc6f5de842c6fb6bad650f24839a5fe7febf9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135744"
---
# <a name="controlsisavailable"></a>Controls.isAvailable

La **proprietà isAvailable** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parametri

*nome*

**Stringa** contenente uno dei valori seguenti.



| string          | Descrizione                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Currentitem     | Determina se l'utente può impostare la **proprietà currentItem.**                                                                                                 |
| currentMarker   | Determina se l'utente può cercare un marcatore specifico.                                                                                                        |
| currentPosition | Determina se l'utente può cercare una posizione specifica nel file. Alcuni file non supportano la ricerca.                                                       |
| Fastforward     | Determina se il file supporta l'inoltro rapido e se tale funzionalità può essere richiamata. Molti tipi di file (o flussi live) non supportano fastForward. |
| fastReverse     | Determina se il file supporta fastReverse e se tale funzionalità può essere richiamata. Molti tipi di file (o flussi live) non supportano fastReverse.     |
| Avanti            | Determina se l'utente può cercare la voce successiva in una playlist.                                                                                             |
| Sospendi           | Determina se il **metodo pause** è disponibile.                                                                                                             |
| Giocare            | Determina se il **metodo di** riproduzione è disponibile.                                                                                                              |
| previous        | Determina se l'utente può cercare la voce precedente in una playlist.                                                                                         |
| step            | Determina se il metodo **step** è disponibile durante la riproduzione.                                                                                              |
| stop            | Determina se il **metodo stop** è disponibile.                                                                                                              |



 

## <a name="return-values"></a>Valori restituiti

Questo metodo restituisce un **valore booleano.**

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che cerca la posizione iniziale dell'elemento multimediale corrente. Il JScript usa **isAvailable** per verificare che il file supporti l'operazione di ricerca. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> </dl>

 

 





