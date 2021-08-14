---
title: Player.playState
description: La proprietà playState recupera un valore che indica lo stato dell'Windows Media Player operazione.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Player.playState Windows Media Player
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0241f8ab538e985a64835065e1eb6bca0a831164cd66fbb7d9166724a72680e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835120"
---
# <a name="playerplaystate"></a>Player.playState

La **proprietà playState** recupera un valore che indica lo stato dell'Windows Media Player operazione.

## <a name="syntax"></a>Sintassi

*lettore* . **playState**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**). La costante di enumerazione di tipo C può essere derivata antefiando il valore di stato con "wmpps". Ad esempio, la costante per lo stato Playing è **wmppsPlaying**.



| Valore | State         | Descrizione                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| 0     | Non definito     | Windows Media Player è in uno stato non definito.                                                                              |
| 1     | Arrestato       | La riproduzione dell'elemento multimediale corrente viene arrestata.                                                                              |
| 2     | Paused        | La riproduzione dell'elemento multimediale corrente è sospesa. Quando un elemento multimediale viene sospeso, la ripresa della riproduzione inizia dalla stessa posizione. |
| 3     | Playing       | L'elemento multimediale corrente è in riproduzione.                                                                                          |
| 4     | ScanForward   | L'elemento multimediale corrente viene inoltrato rapidamente.                                                                                  |
| 5     | ScanReverse   | L'elemento multimediale corrente è in rapida riavvolgimento.                                                                                   |
| 6     | responseBuffering     | L'elemento multimediale corrente sta ottenendo dati aggiuntivi dal server.                                                          |
| 7     | Attesa       | La connessione viene stabilita, ma il server non invia dati. In attesa dell'avvio della sessione.                                |
| 8     | MediaEnded    | La riproduzione dell'elemento multimediale è stata completata.                                                                                          |
| 9     | Transizione | Preparazione del nuovo elemento multimediale.                                                                                                   |
| 10    | Ready         | Pronto per iniziare a riprodurre.                                                                                                     |
| 11    | Ricollegare  | Riconnessione al flusso.                                                                                                     |



 

## <a name="remarks"></a>Commenti

Windows Media Player non è garantito che si verifichino in un ordine specifico. Inoltre, non tutti gli stati si verificano necessariamente durante una sequenza di eventi. Non è consigliabile scrivere codice che si basa sull'ordine di stato.

## <a name="examples"></a>Esempio

Il codice JScript seguente illustra l'uso del *lettore*. **proprietà playState.** Un elemento di testo HTML, denominato "myText", visualizza lo stato corrente. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Evento Player.PlayStateChange**](player-player-playstatechange.md)
</dt> </dl>

 

 





