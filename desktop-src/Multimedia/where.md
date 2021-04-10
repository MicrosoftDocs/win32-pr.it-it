---
title: comando Where
description: Il comando WHERE recupera il rettangolo che specifica l'area di origine o di destinazione. Questo rettangolo è stato specificato utilizzando il comando put. I dispositivi Digital-video e overlay video riconoscono questo comando.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- comando Where Windows Multimedia
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964778"
---
# <a name="where-command"></a>comando Where

Il comando WHERE recupera il rettangolo che specifica l'area di origine o di destinazione. Questo rettangolo è stato specificato utilizzando il comando [put](put.md) . I dispositivi Digital-video e overlay video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*
</dt> <dd>

Flag che identifica il rettangolo le cui dimensioni vengono recuperate. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **where** e i flag utilizzati da ogni tipo.



| Valore        | Significato                                                       | Significato                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| digitalvideo | destinationdestination [**Max**](max.md)frameFrame maxsource | maxvideovideo di origine maxwindowwindow max |
| overlay      | destinationframe                                              | sourcevideo                              |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszRequestRect** e i relativi significati.



| Valore                          | Significato                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                    | Recupera l'offset e l'extent di destinazione. Per i dispositivi con sovrimpressione video, il rettangolo di destinazione definisce l'area dell'area client della finestra di visualizzazione che consente di visualizzare i dati dell'immagine dal buffer del frame.                                                                                             |
| [ **massimo** destinazione](max.md) | Recupera le dimensioni correnti del rettangolo client.                                                                                                                                                                                                                                                  |
| frame                          | Recupera l'offset e l'extent del rettangolo del buffer del frame. Il rettangolo del buffer del frame definisce l'area del buffer del frame che riceve i dati video in arrivo. Le immagini del rettangolo "video" vengono ridimensionate in questa area.                                                                     |
| [ **massimo** frame](max.md)       | Restituisce la dimensione massima del buffer del frame.                                                                                                                                                                                                                                                        |
| source                         | Recupera l'offset di origine e l'extent. Per i dispositivi con sovrimpressione video, il rettangolo di origine definisce l'area del buffer del frame visualizzato nella finestra di destinazione. Il dispositivo utilizza questo rettangolo per ritagliare l'immagine prima che sia adattata al rettangolo di destinazione sullo schermo. |
| [ **numero massimo** di origine](max.md)      | Recupera la dimensione massima del buffer del frame.                                                                                                                                                                                                                                                      |
| Video                          | Recupera l'offset e l'extent del rettangolo video. Il rettangolo video definisce l'area dei dati video in arrivo trasferiti al buffer del frame.                                                                                                                                   |
| [ **massimo** video](max.md)       | Restituisce la dimensione massima dell'input.                                                                                                                                                                                                                                                               |
| Finestra                         | Recupera le dimensioni e la posizione correnti della cornice della finestra di visualizzazione.                                                                                                                                                                                                                                 |
| [ **massimo** finestra](max.md)      | Recupera le dimensioni dell'intero schermo.                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un rettangolo nel parametro *lpszReturnString* della funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . Il rettangolo descrive l'area specificata nel parametro *lpszRequestRect* di questo comando. Il rettangolo viene specificato come *X1 Y1 Y1 2*. Le coordinate *X1 Y1* specificano l'angolo superiore sinistro del rettangolo e le coordinate *X2 Y2* specificano la larghezza e l'altezza.

## <a name="examples"></a>Esempio

Il comando seguente restituisce il rettangolo di visualizzazione del dispositivo "Movie".

``` syntax
where movie destination
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

[mettere](put.md)
</dt> </dl>

 

