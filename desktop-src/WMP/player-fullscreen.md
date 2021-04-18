---
title: Player. fullScreen
description: La proprietà fullScreen Specifica o recupera un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player. fullScreen Windows Media Player
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
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324982"
---
# <a name="playerfullscreen"></a>Player. fullScreen

La proprietà **FullScreen** specifica o recupera un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.

## <a name="syntax"></a>Sintassi

*Player* . a **schermo intero**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                                    |
|-------|----------------------------------------------------------------|
| true  | Il contenuto video viene riprodotto in modalità schermo intero.              |
| false | Valore predefinito. Il contenuto video non viene riprodotto in modalità schermo intero. |



 

## <a name="remarks"></a>Commenti

Per il corretto funzionamento della modalità a schermo intero quando si incorpora il controllo Media Player di Windows, l'area di visualizzazione del video deve avere un'altezza e una larghezza pari ad almeno un pixel. Se **uiMode** è impostato su "mini" o "full", l'altezza del controllo deve essere 65 o superiore per ospitare l'area di visualizzazione video oltre all'interfaccia utente.

Se **uiMode** è impostato su "invisibile", l'impostazione di questa proprietà su true genera un errore e non influisce sul comportamento del controllo.

Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a "None".

Se **uiMode** è impostato su "full" o "mini", Windows Media Player Visualizza i controlli di trasporto in modalità schermo intero quando il cursore del mouse si sposta. Dopo un breve intervallo di assenza del movimento del mouse, i controlli di trasporto sono nascosti. Se **uiMode** è impostato su "None", non viene visualizzato alcun controllo in modalità schermo intero.

**Nota**

Per visualizzare i controlli di trasporto in modalità schermo intero, è necessario il sistema operativo Windows XP.

Se i controlli di trasporto non vengono visualizzati in modalità schermo intero, Windows Media Player esce automaticamente dalla modalità schermo intero quando la riproduzione viene arrestata.

**Nota**

Assicurarsi sempre di informare l'utente come tornare dalla modalità a schermo intero.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un pulsante di input HTML che utilizza *Player*. **FullScreen** per passare un oggetto Player incorporato alla modalità schermo intero. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





