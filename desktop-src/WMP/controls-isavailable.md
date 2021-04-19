---
title: Controls. disavailable
description: La proprietà disavailable indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. | Controls. disavailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Media Player di Windows Controls. available
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
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330006"
---
# <a name="controlsisavailable"></a>Controls. disavailable

La proprietà **disavailable** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.

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
| currentItem     | Determina se l'utente può impostare la proprietà **CurrentItem** .                                                                                                 |
| currentMarker   | Determina se l'utente può cercare un marcatore specifico.                                                                                                        |
| currentPosition | Determina se l'utente può eseguire la ricerca in una posizione specifica nel file. Alcuni file non supportano la ricerca.                                                       |
| fastForward     | Determina se il file supporta l'avanzamento rapido e se tale funzionalità può essere richiamata. Molti tipi di file (o flussi live) non supportano fastForward. |
| fastReverse     | Determina se il file supporta fastReverse e se tale funzionalità può essere richiamata. Molti tipi di file (o flussi live) non supportano fastReverse.     |
| Avanti            | Determina se l'utente può cercare la voce successiva in una playlist.                                                                                             |
| Sospendi           | Determina se il metodo **pause** è disponibile.                                                                                                             |
| Play            | Determina se il metodo **Play** è disponibile.                                                                                                              |
| previous        | Determina se l'utente può cercare la voce precedente in una playlist.                                                                                         |
| step            | Determina se il metodo **Step** è disponibile durante la riproduzione.                                                                                              |
| stop            | Determina se il metodo **Stop** è disponibile.                                                                                                              |



 

## <a name="return-values"></a>Valori restituiti

Questo metodo restituisce un valore **booleano** .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che cerca la posizione iniziale dell'elemento multimediale corrente. Il codice **JScript utilizza l'** oggetto per verificare che il file supporti l'operazione Seek. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> </dl>

 

 





