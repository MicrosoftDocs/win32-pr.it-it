---
title: Player.fullScreen
description: La proprietà fullScreen specifica o recupera un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player.fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f380dcbcaeedddd23c5e6ff42f9750ea8bcd2f552942e19ba7b847e725edc3b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054379"
---
# <a name="playerfullscreen"></a>Player.fullScreen

La **proprietà fullScreen** specifica o recupera un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.

## <a name="syntax"></a>Sintassi

*lettore* . **fullScreen**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                                                    |
|-------|----------------------------------------------------------------|
| true  | Il contenuto video viene riprodotto in modalità schermo intero.              |
| false | Valore predefinito. Il contenuto video non viene riprodotto in modalità schermo intero. |



 

## <a name="remarks"></a>Commenti

Per il corretto funzionamento della modalità schermo intero durante l'incorporamento del controllo Windows Media Player, l'area di visualizzazione video deve avere un'altezza e una larghezza di almeno un pixel. Se **uiMode è** impostato su "mini" o "full", l'altezza del controllo stesso deve essere 65 o superiore per contenere l'area di visualizzazione video oltre all'interfaccia utente.

Se **uiMode** è impostato su "invisible", l'impostazione di questa proprietà su true genera un errore e non influisce sul comportamento del controllo.

Durante la riproduzione a schermo intero, Windows Media Player il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a "none".

Se **uiMode è** impostato su "full" o "mini", Windows Media Player visualizza i controlli di trasporto in modalità schermo intero quando il cursore del mouse viene spostato. Dopo un breve intervallo di assenza di spostamento del mouse, i controlli di trasporto vengono nascosti. Se **uiMode** è impostato su "none", non viene visualizzato alcun controllo in modalità schermo intero.

**Nota**

La visualizzazione dei controlli di trasporto in modalità schermo intero richiede Windows sistema operativo XP.

Se i controlli di trasporto non vengono visualizzati in modalità schermo intero, Windows Media Player automaticamente la modalità schermo intero all'arresto della riproduzione.

**Nota**

Assicurarsi sempre di informare l'utente come tornare dalla modalità schermo intero.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un pulsante di input HTML che usa *Player.* **fullScreen per** attivare la modalità schermo intero per un oggetto lettore incorporato. **L'oggetto Player** è stato creato con ID = "Player".


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





