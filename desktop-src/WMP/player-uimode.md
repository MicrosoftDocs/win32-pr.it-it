---
title: Player.uiMode
description: La proprietà uiMode specifica o recupera un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Player.uiMode Windows Media Player
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
ms.openlocfilehash: f082da34ffc3b77869e84ceb576b4e6273ccaff15a5f95e66d98cae93697c251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835338"
---
# <a name="playeruimode"></a>Player.uiMode

La **proprietà uiMode** specifica o recupera un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.

## <a name="syntax"></a>Sintassi

*lettore* . **uiMode**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di **lettura/scrittura.**



| Valore     | Descrizione                                                                                                                                                                                                           | Esempio di audio                                          | Esempio di video                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| invisibile | Windows Media Player è incorporato senza alcuna interfaccia utente visibile (controlli, video o finestra di visualizzazione).                                                                                                        | Non viene visualizzato nulla.                                | Non viene visualizzato nulla.                                |
| Nessuno      | Windows Media Player è incorporato senza controlli e con solo la finestra video o di visualizzazione visualizzata.                                                                                                         | !["none" con audio](images/uimode-none-audio-v11.png) | !["none" con il video](images/uimode-none-video-v11.png) |
| Mini      | Windows Media Player è incorporato con la finestra di stato, la riproduzione/sospensione, l'arresto, l'disattivazione dell'audio e i controlli volume visualizzati oltre alla finestra video o di visualizzazione.                                                          | !["mini" con audio](images/uimode-mini-audio-v11.png) | !["mini" con video](images/uimode-mini-video-v11.png) |
| completi      | Valore predefinito. Windows Media Player è incorporato con la finestra di stato, la barra di ricerca, la riproduzione/sospensione, l'arresto, l'disattivazione dell'audio, il successivo, il precedente, l'avanzamento rapido, l'inversione rapida e i controlli del volume oltre alla finestra video o di visualizzazione. | !["full" con audio](images/uimode-full-audio-v11.png) | !["full" con video](images/uimode-full-video-v11.png) |
| custom    | Windows Media Player è incorporato con un'interfaccia utente personalizzata. Può essere usato solo nei programmi C++.                                                                                                                      | Viene visualizzata l'interfaccia utente personalizzata.                  | Viene visualizzata l'interfaccia utente personalizzata.                  |



 

## <a name="remarks"></a>Commenti

Questa proprietà specifica l'aspetto del Windows Media Player. Quando **uiMode** è impostato su "none", "mini" o "full", è presente una finestra per la visualizzazione di clip video e visualizzazioni audio. Questa finestra può essere nascosta in modalità mini o completa impostando l'attributo **height** del tag **OBJECT** su 40, misurato dal basso, e lasciando visibile la parte dei controlli dell'interfaccia utente. Se non si desidera alcuna interfaccia incorporata, impostare entrambi gli attributi **width** **e height** su zero.

Se **uiMode è** impostato su "invisible", non viene visualizzata alcuna interfaccia utente, ma lo spazio è ancora riservato nella pagina come specificato da **width** e **height.** Ciò è utile per mantenere il layout di pagina quando **uiMode** può cambiare. Inoltre, lo spazio riservato è trasparente, quindi tutti gli elementi a livelli dietro il controllo saranno visibili.

Se **uiMode è** impostato su "full" o "mini", Windows Media Player i controlli di trasporto in modalità schermo intero. Se **uiMode** è impostato su "none", non vengono visualizzati controlli in modalità schermo intero.

Se la finestra è visibile e viene riprodotto il contenuto audio, la visualizzazione visualizzata sarà quella usata più di recente in Windows Media Player.

Se **uiMode** è impostato su "custom" in un programma C++ che implementa **IWMPRemoteMediaServices,** viene visualizzato il file di interfaccia indicato da **IWMPRemoteMediaServices::GetCustomUIMode.**

Durante la riproduzione a schermo intero, Windows Media Player il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a "none".

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento HTML SELECT che consente all'utente di modificare l'interfaccia utente per un oggetto **Player** incorporato. **L'oggetto** Player è stato creato con ID = "Player".


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



Windows Media Player 10 Mobile: questa proprietà accetta o restituisce solo valori "none" o "full". Nei dispositivi Smartphone vengono visualizzati solo lo stato di riproduzione e un contatore quando *uiMode* è impostato su "full".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva. Windows Media Player serie 9 o successive per "invisibili" o "personalizzate".<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPRemoteMediaServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[**IWMPRemoteMediaServices::GetCustomUIMode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





