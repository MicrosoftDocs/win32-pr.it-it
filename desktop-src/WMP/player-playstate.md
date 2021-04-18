---
title: Player. riproduzione
description: La proprietà riproduzione recupera un valore che indica lo stato dell'operazione Windows Media Player.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Player. riproduzione Windows Media Player
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
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327704"
---
# <a name="playerplaystate"></a>Player. riproduzione

La proprietà **riproduzione** recupera un valore che indica lo stato dell'operazione Windows Media Player.

## <a name="syntax"></a>Sintassi

*Player* . **riproduzione**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**). La costante di enumerazione di tipo C può essere derivata anteponendo il valore di stato con "wmpps". La costante per lo stato di riproduzione, ad esempio, è **wmppsPlaying**.



| Valore | State         | Descrizione                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| 0     | Non definito     | Windows Media Player è in uno stato non definito.                                                                              |
| 1     | Arrestato       | La riproduzione dell'elemento multimediale corrente è stata arrestata.                                                                              |
| 2     | Paused        | La riproduzione dell'elemento multimediale corrente è sospesa. Quando un elemento multimediale viene sospeso, la ripresa della riproduzione inizia dalla stessa posizione. |
| 3     | Playing       | L'elemento multimediale corrente sta eseguendo la riproduzione.                                                                                          |
| 4     | ScanForward   | L'elemento multimediale corrente è l'avanzamento rapido.                                                                                  |
| 5     | ScanReverse   | L'elemento multimediale corrente è un riavvolgimento rapido.                                                                                   |
| 6     | responseBuffering     | L'elemento multimediale corrente sta ottenendo dati aggiuntivi dal server.                                                          |
| 7     | Attesa       | Viene stabilita la connessione, ma il server non invia dati. In attesa dell'inizio della sessione.                                |
| 8     | MediaEnded    | La riproduzione dell'elemento multimediale è stata completata.                                                                                          |
| 9     | Transizione | Preparazione di un nuovo elemento multimediale.                                                                                                   |
| 10    | Ready         | Pronto per iniziare la riproduzione.                                                                                                     |
| 11    | Riconnessione  | Riconnessione al flusso.                                                                                                     |



 

## <a name="remarks"></a>Commenti

Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare. Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi. Non è necessario scrivere codice che si basa sull'ordine di stato.

## <a name="examples"></a>Esempio

Il codice JScript seguente illustra l'uso del *lettore*. proprietà **riproduzione** . Un elemento di testo HTML, denominato "testo", Visualizza lo stato corrente. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Evento Player. PlayStateChange**](player-player-playstatechange.md)
</dt> </dl>

 

 





