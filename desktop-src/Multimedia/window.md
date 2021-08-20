---
title: comando window
description: Il comando della finestra controlla la finestra di visualizzazione.
ms.assetid: 613dfedb-5ca8-45da-a4ba-ce465b933451
keywords:
- Comando window Windows Multimedia
topic_type:
- apiref
api_name:
- window
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c65fe13309d30a3aff94e6e78dc0ab1fbcfec26aa1634e8dae72130370cc8e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800705"
---
# <a name="window-command"></a>comando window

Il comando della finestra controlla la finestra di visualizzazione. È possibile usare questo comando per modificare le caratteristiche di visualizzazione della finestra o specificare una finestra di destinazione che il driver può usare al posto della finestra di visualizzazione predefinita. I dispositivi di sovrimpressione video e digitale riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("window %s %s %s"), 
  lpszDeviceID, 
  lpszWindowFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszWindowFlags"></span><span id="lpszwindowflags"></span><span id="LPSZWINDOWFLAGS"></span>*lpszWindowFlags*
</dt> <dd>

Flag per il controllo della finestra di visualizzazione. La tabella seguente elenca i tipi di dispositivo che riconoscono il comando della finestra e i flag usati da ogni tipo.



| Valore        | Significato                                                                                                                                        | Significato                                                                                                                                   |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | handle *hwnd* state hidestate minimizestate restorestate showshow maximized                                                                    | show minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normaltext *caption*                                             |
| overlay      | fixedhandle defaulthandle *hwnd* state hidestate invalidstate maximizedstate minimizestate minimizedstate no actionstate noactivatestate normal | state restorestate showshow maximizedshow minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normalstretchtext *caption* |



 

La tabella seguente elenca i flag che possono essere specificati nel **parametro lpszWindowFlags** e i relativi significati.



| Valore                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fixed                            | Disabilita l'estensione dell'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| handle default                   | Specifica che il dispositivo deve impostare nuovamente la finestra di visualizzazione sulla finestra predefinita creata durante [l'operazione di](open.md) apertura. Per i dispositivi con sovrimpressione video, specifica che il dispositivo deve creare e gestire la propria finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                  |
| handle *hwnd*                    | Specifica l'handle della finestra di destinazione da utilizzare al posto della finestra predefinita. Il *parametro hwnd* contiene l'equivalente numerico ASCII dell'handle di finestra restituito dalla [funzione CreateWindow.](/windows/win32/api/winuser/nf-winuser-createwindowa) Due istanze del dispositivo possono usare lo stesso handle di finestra a condizione che ogni istanza a aggiorna i pixel del video e dell'immagine nella finestra come se l'altra istanza non esistesse. Quando l'output video è disabilitato [con setvideo](setvideo.md) "off", un comando [di](update.md) aggiornamento rende il rettangolo di destinazione un colore a tinta unita. |
| mostra ingrandita                   | Ingrandisce la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| show [**min**](min.md) noactive | Visualizza la finestra di destinazione come icona.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| mostra ridotta a icona                   | Riduce a icona la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| show na                          | Visualizza la finestra di destinazione nello stato corrente. la finestra attualmente attiva rimane attiva.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| show noactivate                  | Visualizza la finestra di destinazione con le dimensioni e la posizione più recenti. la finestra attualmente attiva rimane attiva.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| show normal                      | Attiva e visualizza la finestra di destinazione con le dimensioni e la posizione originali. Corrisponde al flag "state restore".                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| state hide                       | Nasconde la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| state avare                     | Visualizza la finestra di destinazione come icona.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| stato ingrandito                  | Ingrandisce la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| riduzione a icona dello stato                   | Riduce a icona la finestra di destinazione e attiva la finestra di primo livello nell'elenco di gestione finestre.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stato ridotto a icona                  | Riduce a icona la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| state no action                  | Visualizza la finestra di destinazione nello stato corrente. La finestra attualmente attiva rimane attiva.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| state noactivate                 | Visualizza la finestra di destinazione con le dimensioni e lo stato più recenti. La finestra attiva rimane attiva.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| state normal                     | Attiva e visualizza la finestra di destinazione con le dimensioni e la posizione originali.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ripristino dello stato                    | Attiva e visualizza la finestra di destinazione con le dimensioni e la posizione originali.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| state show                       | Mostra la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| adattamento                          | Abilita l'estensione dell'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| didascalia *di testo*                   | Specifica la didascalia per la finestra di destinazione. Se questo testo contiene spazi vuoti incorporati, l'intera didascalia deve essere racchiusa tra virgolette. La didascalia predefinita per la finestra predefinita è vuota.                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I dispositivi con sovrimpressione video in genere creano e visualizzano una finestra all'apertura. Se l'applicazione fornisce una finestra al driver, l'applicazione è responsabile della gestione dei messaggi inviati alla finestra.

Poiché è possibile usare il comando [status](status.md) per recuperare l'handle per la finestra di visualizzazione del driver, è anche possibile usare le funzioni standard di gestione delle finestre ( ad esempio [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow)) per modificare la finestra.

## <a name="examples"></a>Esempio

Il comando seguente visualizza e imposta la didascalia per la finestra di riproduzione "movie".

``` syntax
window movie text "Welcome to the Movies" state show
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[open](open.md)
</dt> <dt>

[Giocare](play.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[update](update.md)
</dt> </dl>

 

