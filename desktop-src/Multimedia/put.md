---
title: Comando put
description: Il comando put definisce l'area dell'immagine di origine e della finestra di destinazione usata per la visualizzazione. I dispositivi di sovrimpressione video e digitale riconoscono questo comando.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- Comando put Windows Multimedia
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08732b0ed55464fa1a288cc13a9ac19609b480644ffa4c9dfbeb140cedbbd3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372380"
---
# <a name="put-command"></a>Comando put

Il comando put definisce l'area dell'immagine di origine e della finestra di destinazione usata per la visualizzazione. I dispositivi di sovrimpressione video e digitale riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*
</dt> <dd>

Flag per la definizione dell'area. La tabella seguente elenca i tipi di dispositivo che riconoscono il comando put e i flag usati da ogni tipo.



| Valore        | Significato                                                                                      | Significato                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| digitalvideo | destinazione nel frame del *rettangolo* all'origine *del rettangolo* in corrispondenza del rettangolo di *origine* | video nella finestra *rettangolare* in corrispondenza del client *della* finestra client della finestra rettangolare in corrispondenza del *rettangolo* |
| overlay      | destinazione nel frame *del rettangolo* in corrispondenza del *rettangolo*                             | source source at *rectangle* video at *rectangle*                                           |



 

La tabella seguente elenca i flag che possono essere specificati nel **parametro lpszRegions** e i relativi significati.



| Valore                        | Significato                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                  | Seleziona l'intera area client della finestra di destinazione per visualizzare i dati.                                                                                                                                                                                                                                                                         |
| destinazione in corrispondenza del *rettangolo*   | Seleziona una parte dell'area client della finestra di destinazione utilizzata per visualizzare l'immagine. Quando viene specificata un'area della finestra di visualizzazione e il dispositivo supporta l'estensione, l'immagine di origine viene adattata all'offset e all'extent di destinazione.                                                                                                     |
| frame                        | Seleziona l'intero buffer dei fotogrammi per ricevere le immagini video in ingresso.                                                                                                                                                                                                                                                                                 |
| frame in corrispondenza del *rettangolo*         | Seleziona una parte del buffer dei fotogrammi per ricevere le immagini video in ingresso.                                                                                                                                                                                                                                                                           |
| source                       | Seleziona l'intera immagine da visualizzare nella finestra di destinazione.                                                                                                                                                                                                                                                                                       |
| origine in corrispondenza del *rettangolo*        | Seleziona una parte dell'immagine da visualizzare nella finestra di destinazione. Quando viene specificata un'area dell'immagine di origine e il dispositivo supporta l'estensione, l'immagine di origine viene adattata all'offset e all'extent di destinazione.                                                                                                                           |
| Video                        | Seleziona l'intera immagine video in ingresso da acquisire nel buffer dei fotogrammi.                                                                                                                                                                                                                                                                               |
| video at *rectangle*         | Seleziona una parte dell'immagine video in ingresso da acquisire nel buffer dei fotogrammi.                                                                                                                                                                                                                                                                         |
| Finestra                       | Ripristina le dimensioni iniziali della finestra sullo schermo. Questo comando visualizza anche la finestra.                                                                                                                                                                                                                                                               |
| finestra in corrispondenza del *rettangolo*        | Modifica le dimensioni e la posizione della finestra di visualizzazione. Il rettangolo specificato è relativo alla finestra padre della finestra di visualizzazione (in genere il desktop) se per il comando [open](open.md) è stato usato il flag "style child". Per modificare la posizione della finestra senza modificarne l'altezza o la larghezza, specificare zero per l'altezza e la larghezza. |
| client finestra                | Ripristina l'area client della finestra.                                                                                                                                                                                                                                                                                                               |
| client finestra in corrispondenza del *rettangolo* | Modifica le dimensioni e la posizione dell'area client della finestra. Il rettangolo specificato è relativo alla finestra padre della finestra client. Per modificare la posizione della finestra senza modificarne l'altezza o la larghezza, specificare zero per l'altezza e la larghezza.                                                                                      |



 

Quando un flag include un rettangolo, le coordinate del rettangolo sono relative all'origine della finestra o all'origine dell'immagine, in base alle esigenze, e vengono specificate come **X1 Y1 X2 Y2.** Le coordinate **X1Y1** specificano l'angolo superiore sinistro e le coordinate **X2Y2** specificano la larghezza e l'altezza del rettangolo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il comando put definisce uno o più rettangoli seguenti quando si lavora con dispositivi di sovrimpressione video:

-   Il rettangolo video definisce l'area dell'immagine video in ingresso da acquisire.
-   Il rettangolo dei fotogrammi definisce l'area del buffer dei fotogrammi che riceve l'immagine video in ingresso.
-   Il rettangolo di origine definisce quale area del buffer dei frame viene copiata nel rettangolo di destinazione.
-   Il rettangolo di destinazione definisce l'area client della finestra di visualizzazione che riceve l'immagine video.

Il rettangolo video è correlato al rettangolo del frame nello stesso modo in cui il rettangolo di origine è correlato al rettangolo di destinazione. L'estensione può avvenire dal rettangolo video al rettangolo del frame e dal rettangolo di origine al rettangolo di destinazione. Non tutti i dispositivi supportano l'estensione e l'estensione deve essere abilitata (usando il [comando set).](set.md)

Il comando seguente definisce tre aree per il video, il frame e l'origine.

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

Le aree in questo esempio sono definite come segue:

-   Un'area di 200x200 pixel dei dati video in ingresso, a partire da un'origine a 120 pixel dall'angolo superiore sinistro, verrà acquisita nel buffer dei fotogrammi.
-   I dati video verranno inseriti in un'area di 200x200 pixel nell'angolo superiore sinistro del buffer dei fotogrammi.
-   I trasferimenti vengono effettuati dall'area da 200 a 200 pixel nell'angolo superiore sinistro del buffer frame alla finestra di destinazione.

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

[set](set.md)
</dt> </dl>

 

