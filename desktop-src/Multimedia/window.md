---
title: comando finestra
description: Il comando finestra Controlla la finestra di visualizzazione.
ms.assetid: 613dfedb-5ca8-45da-a4ba-ce465b933451
keywords:
- Windows (comando finestra) Multimedia
topic_type:
- apiref
api_name:
- window
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21dde3304fa1445b0eaac68950cdfb91f48e5986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476582"
---
# <a name="window-command"></a>comando finestra

Il comando finestra Controlla la finestra di visualizzazione. È possibile utilizzare questo comando per modificare le caratteristiche di visualizzazione della finestra o specificare una finestra di destinazione che il driver utilizzerà al posto della finestra di visualizzazione predefinita. I dispositivi Digital-video e overlay video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszWindowFlags"></span><span id="lpszwindowflags"></span><span id="LPSZWINDOWFLAGS"></span>*lpszWindowFlags*
</dt> <dd>

Flag per il controllo della finestra di visualizzazione. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando della finestra e i flag utilizzati da ogni tipo.



| Valore        | Significato                                                                                                                                        | Significato                                                                                                                                   |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | Gestisci stato *HWND* hidestate minimizestate RestoreState showshow ingrandito                                                                    | Mostra minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normaltext *Caption*                                             |
| overlay      | fixedhandle defaulthandle *HWND* state hidestate iconicstate maximizedstate minimizestate minimizedstate no ActionState noactivatestate Normal | state RestoreState showshow maximizedshow minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normalstretchtext *Caption* |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszWindowFlags** e i relativi significati.



| Valore                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fixed                            | Disabilita l'allungamento dell'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Gestisci predefinito                   | Specifica che il dispositivo deve impostare nuovamente la finestra di visualizzazione sulla finestra predefinita creata durante l'operazione di [apertura](open.md) . Per i dispositivi con sovrimpressione video, specifica che il dispositivo deve creare e gestire la propria finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                  |
| Gestisci *HWND*                    | Specifica l'handle della finestra di destinazione da utilizzare al posto della finestra predefinita. Il parametro *HWND* contiene l'equivalente numerico ASCII dell'handle di finestra restituito dalla funzione [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Due istanze del dispositivo possono usare lo stesso handle di finestra purché ogni istanza aggiorni i pixel video e immagine nella finestra come se l'altra istanza non esistesse. Quando l'output video è disabilitato con [sevideo](setvideo.md) "off", un comando [Update](update.md) renderà il rettangolo di destinazione un colore a tinta unita. |
| Mostra ingrandita                   | Ingrandisce la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Mostra [**min**](min.md) noactive | Consente di visualizzare la finestra di destinazione come icona.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Mostra ridotta a icona                   | Riduce a icona la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Mostra na                          | Visualizza la finestra di destinazione nello stato corrente; la finestra attualmente attiva rimane attiva.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Mostra noactivate                  | Visualizza la finestra di destinazione nelle dimensioni e nella posizione più recenti; la finestra attualmente attiva rimane attiva.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Mostra normale                      | Attiva e visualizza la finestra di destinazione con le dimensioni e la posizione originali. (Corrisponde al flag "ripristino stato").                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Nascondi stato                       | Nasconde la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| icona stato                     | Consente di visualizzare la finestra di destinazione come icona.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| stato ingrandito                  | Ingrandisce la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stato ridotto a icona                   | Riduce a icona la finestra di destinazione e attiva la finestra di primo livello nell'elenco di Window-Manager.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stato ridotto a icona                  | Riduce a icona la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stato nessuna azione                  | Consente di visualizzare la finestra di destinazione nello stato corrente. La finestra attualmente attiva rimane attiva.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| stato noactivate                 | Consente di visualizzare la finestra di destinazione nelle dimensioni e nello stato più recenti. La finestra attiva rimane attiva.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| stato normale                     | Attiva e visualizza la finestra di destinazione con le dimensioni e la posizione originali.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ripristino dello stato                    | Attiva e visualizza la finestra di destinazione con le dimensioni e la posizione originali.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Mostra stato                       | Mostra la finestra di destinazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| adattamento                          | Abilita l'allungamento dell'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| *didascalia* testo                   | Specifica la didascalia per la finestra di destinazione. Se il testo contiene spazi vuoti incorporati, è necessario racchiudere l'intera didascalia tra virgolette. La didascalia predefinita per la finestra predefinita è vuota.                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I dispositivi overlay video in genere creano e visualizzano una finestra all'apertura. Se l'applicazione fornisce una finestra al driver, l'applicazione è responsabile della gestione dei messaggi inviati alla finestra di.

Poiché è possibile usare il comando [status](status.md) per recuperare l'handle per la finestra di visualizzazione del driver, è anche possibile usare le funzioni standard di Window Manager (ad esempio [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow)) per modificare la finestra.

## <a name="examples"></a>Esempio

Il comando seguente Visualizza e imposta la didascalia per la finestra di riproduzione "Movie".

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

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[open](open.md)
</dt> <dt>

[Play](play.md)
</dt> <dt>

[video](setvideo.md)
</dt> <dt>

[update](update.md)
</dt> </dl>

 

