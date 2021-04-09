---
title: Put (comando)
description: Il comando put definisce l'area dell'immagine di origine e della finestra di destinazione utilizzata per la visualizzazione. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- inserire i contenuti multimediali di Windows
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121122"
---
# <a name="put-command"></a>Put (comando)

Il comando put definisce l'area dell'immagine di origine e della finestra di destinazione utilizzata per la visualizzazione. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*
</dt> <dd>

Flag per la definizione dell'area. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando put e i flag utilizzati da ogni tipo.



| Valore        | Significato                                                                                      | Significato                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| digitalvideo | destinazione destinazione al frame frame *rettangolo* all'origine di origine *rettangolo* al *rettangolo* | video video sulla finestra della finestra *rettangolare* nel client della finestra del client della finestra *rettangolare* al *rettangolo* |
| overlay      | destinazione destinazione al frame frame *rettangolo* al *rettangolo*                             | origine di origine in un video video *rettangolare* nel *rettangolo*                                           |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszRegions** e i relativi significati.



| Valore                        | Significato                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                  | Consente di selezionare l'intera area client della finestra di destinazione in cui visualizzare i dati.                                                                                                                                                                                                                                                                         |
| destinazione al *rettangolo*   | Seleziona una parte dell'area client della finestra di destinazione utilizzata per visualizzare l'immagine. Quando si specifica un'area della finestra di visualizzazione e il dispositivo supporta l'estensione, l'immagine di origine viene allungata all'offset e all'extent di destinazione.                                                                                                     |
| frame                        | Seleziona l'intero buffer di frame per ricevere le immagini video in arrivo.                                                                                                                                                                                                                                                                                 |
| cornice al *rettangolo*         | Seleziona una parte del buffer del frame per ricevere le immagini video in arrivo.                                                                                                                                                                                                                                                                           |
| source                       | Consente di selezionare l'intera immagine da visualizzare nella finestra di destinazione.                                                                                                                                                                                                                                                                                       |
| origine al *rettangolo*        | Seleziona una parte dell'immagine da visualizzare nella finestra di destinazione. Quando si specifica un'area dell'immagine di origine e il dispositivo supporta l'estensione, l'immagine di origine viene allungata all'offset e all'extent di destinazione.                                                                                                                           |
| Video                        | Seleziona l'intera immagine video in ingresso da acquisire nel buffer del frame.                                                                                                                                                                                                                                                                               |
| video al *rettangolo*         | Seleziona una parte dell'immagine video in ingresso da acquisire nel buffer del frame.                                                                                                                                                                                                                                                                         |
| Finestra                       | Ripristina le dimensioni iniziali della finestra sullo schermo. Questo comando Visualizza anche la finestra.                                                                                                                                                                                                                                                               |
| finestra al *rettangolo*        | Modifica le dimensioni e la posizione della finestra di visualizzazione. Il rettangolo specificato è relativo alla finestra padre della finestra di visualizzazione (in genere il desktop) se il flag "stile figlio" è stato usato per il comando [Apri](open.md) . Per modificare la posizione della finestra senza modificarne l'altezza o la larghezza, specificare zero per l'altezza e la larghezza. |
| client finestra                | Ripristina l'area client della finestra.                                                                                                                                                                                                                                                                                                               |
| client finestra al *rettangolo* | Modifica le dimensioni e la posizione dell'area client della finestra. Il rettangolo specificato è relativo alla finestra padre della finestra del client. Per modificare la posizione della finestra senza modificarne l'altezza o la larghezza, specificare zero per l'altezza e la larghezza.                                                                                      |



 

Quando un flag include un rettangolo, le coordinate del rettangolo sono relative all'origine della finestra o all'origine dell'immagine, a seconda delle esigenze, e sono specificate come **X1 Y1 2 x y2**. Le coordinate **X1Y1** specificano l'angolo superiore sinistro e le coordinate **X2Y2** specificano la larghezza e l'altezza del rettangolo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Il comando put definisce uno o più dei seguenti rettangoli quando si lavora con dispositivi con sovrimpressione video:

-   Il rettangolo video definisce l'area dell'immagine video in ingresso da acquisire.
-   Il rettangolo del frame definisce l'area del buffer del frame che riceve l'immagine video in arrivo.
-   Il rettangolo di origine definisce quale area del buffer dei frame viene copiata nel rettangolo di destinazione.
-   Il rettangolo di destinazione definisce l'area dell'area client della finestra di visualizzazione che riceve l'immagine del video.

Il rettangolo video è correlato al rettangolo frame nello stesso modo in cui il rettangolo di origine è correlato al rettangolo di destinazione. L'estensione può verificarsi dal rettangolo video al rettangolo del frame e dal rettangolo di origine al rettangolo di destinazione. Non tutti i dispositivi supportano l'estensione e l'allungamento deve essere abilitato (usando il comando [set](set.md) ).

Il comando che segue definisce tre aree per il video, il frame e l'origine.

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

Le aree in questo esempio sono definite come segue:

-   Un'area 200 per 200 pixel dei dati video in arrivo, a partire da un'origine 120 pixel dall'angolo superiore sinistro, verrà acquisita nel buffer del frame.
-   I dati video verranno posizionati in un'area 200 per 200 pixel nell'angolo superiore sinistro del buffer del frame.
-   I trasferimenti vengono effettuati dall'area 200-by 200-pixel nell'angolo superiore sinistro del buffer del frame alla finestra di destinazione.

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

[set](set.md)
</dt> </dl>

 

