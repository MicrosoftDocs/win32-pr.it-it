---
title: Player. uiMode
description: La proprietà uiMode specifica o recupera un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Player. uiMode Windows Media Player
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327063"
---
# <a name="playeruimode"></a>Player. uiMode

La proprietà **uiMode** specifica o recupera un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.

## <a name="syntax"></a>Sintassi

*Player* . **uiMode**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di lettura/scrittura.



| Valore     | Descrizione                                                                                                                                                                                                           | Esempio di audio                                          | Esempio video                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| invisibile | Windows Media Player è incorporato senza alcuna interfaccia utente visibile (controlli, video o finestra di visualizzazione).                                                                                                        | Non viene visualizzato alcun elemento.                                | Non viene visualizzato alcun elemento.                                |
| Nessuno      | Windows Media Player viene incorporato senza controlli e con solo la finestra video o visualizzazione visualizzata.                                                                                                         | !["None" con audio](images/uimode-none-audio-v11.png) | !["None" con video](images/uimode-none-video-v11.png) |
| minima      | Windows Media Player è incorporato con la finestra di stato, i controlli di riproduzione, sospensione, arresto, silenziamento e volume visualizzati oltre alla finestra video o visualizzazione.                                                          | !["mini" con audio](images/uimode-mini-audio-v11.png) | !["mini" con video](images/uimode-mini-video-v11.png) |
| completi      | Valore predefinito. Windows Media Player viene incorporato con la finestra di stato, la barra di ricerca, i controlli di riproduzione, pausa, arresto, silenziamento, avanti, precedente, avanzamento rapido, Reverse veloce e volume, oltre alla finestra visualizzazione o video. | !["completo" con audio](images/uimode-full-audio-v11.png) | !["completo" con video](images/uimode-full-video-v11.png) |
| custom    | Windows Media Player è incorporato con un'interfaccia utente personalizzata. Può essere usato solo nei programmi C++.                                                                                                                      | Viene visualizzata l'interfaccia utente personalizzata.                  | Viene visualizzata l'interfaccia utente personalizzata.                  |



 

## <a name="remarks"></a>Commenti

Questa proprietà specifica l'aspetto della Media Player Windows incorporata. Quando **uiMode** è impostato su "None", "mini" o "full", per la visualizzazione di clip video e visualizzazioni audio è presente una finestra. Questa finestra può essere nascosta in modalità mini o full impostando l'attributo **Height** del tag **Object** su 40, che viene misurato dalla parte inferiore e lascia visibile la parte Controls dell'interfaccia utente. Se non si desidera alcuna interfaccia incorporata, impostare gli attributi **Width** e **Height** su zero.

Se **uiMode** è impostato su "invisibile", non viene visualizzata alcuna interfaccia utente, ma lo spazio è ancora riservato nella pagina come specificato in **larghezza** e **altezza**. Questa operazione è utile per mantenere il layout di pagina quando è possibile modificare **uiMode** . Inoltre, lo spazio riservato è trasparente, quindi tutti gli elementi a livelli dietro il controllo saranno visibili.

Se **uiMode** è impostato su "full" o "mini", Windows Media Player Visualizza i controlli di trasporto in modalità schermo intero. Se **uiMode** è impostato su "None", non viene visualizzato alcun controllo in modalità schermo intero.

Se la finestra è visibile e il contenuto audio viene riprodotto, la visualizzazione visualizzata sarà quella usata più di recente in Windows Media Player.

Se **uiMode** è impostato su "Custom" in un programma C++ che implementa **IWMPRemoteMediaServices**, viene visualizzato il file dell'interfaccia indicato da **IWMPRemoteMediaServices:: GetCustomUIMode** .

Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a "None".

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento HTML SELECT che consente all'utente di modificare l'interfaccia utente per un oggetto **Player** incorporato. L'oggetto **Player** è stato creato con ID = "Player".


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



Windows Media Player 10 Mobile: questa proprietà accetta o restituisce solo i valori "None" o "full". Nei dispositivi smartphone vengono visualizzati solo lo stato della riproduzione e un contatore quando *uiMode* è impostato su "full".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva. Windows Media Player 9 Series o versione successiva per "invisibile" o "personalizzato".<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPRemoteMediaServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[**IWMPRemoteMediaServices::GetCustomUIMode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





