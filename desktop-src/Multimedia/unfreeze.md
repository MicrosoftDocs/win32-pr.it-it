---
title: comando unfreeze
description: Il comando unfreeze riabilita l'acquisizione video nel buffer dei fotogrammi dopo che è stato disabilitato dal comando freeze. I dispositivi di video digitale, videoregistratore e sovrimpressione video riconoscono questo comando.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- Comando unfreeze Windows Multimedia
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fe45b1346872483a4012c5f5d161dcd61020c64349fee254ae4bf337b4be8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370811"
---
# <a name="unfreeze-command"></a>comando unfreeze

Il comando unfreeze riabilita l'acquisizione video nel buffer dei fotogrammi dopo che è stato disabilitato dal [comando freeze.](freeze.md) I dispositivi di video digitale, videoregistratore e sovrimpressione video riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*
</dt> <dd>

Flag per la riasserzione dell'acquisizione video nel buffer dei fotogrammi. La tabella seguente elenca i tipi di dispositivo che riconoscono il comando **unfreeze** e i flag usati da ogni tipo.



| Valore        | Significato        |
|--------------|----------------|
| digitalvideo | at *rectangle* |
| overlay      | at *rectangle* |
| Vcr          | output di input   |



 

La tabella seguente elenca i flag che possono essere specificati nel **parametro lpszUnfreeze** e i relativi significati.



| Valore          | Significato                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at *rectangle* | Specifica l'area in cui verrà ri abilitata l'acquisizione del video. Il rettangolo è relativo all'origine del buffer video e viene specificato come *X1 Y1 X2 Y2*. Le coordinate *X1 Y1* specificano l'angolo superiore sinistro del rettangolo e le coordinate *X2 Y2* specificano la larghezza e l'altezza. |
| input          | Sbloccare l'immagine di input.                                                                                                                                                                                                                                                                  |
| output         | Sbloccare l'immagine di output. Se non viene specificato né "input" né "output", viene utilizzato "output".                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="examples"></a>Esempio

Il comando seguente sblocca un'area del buffer video.

``` syntax
unfreeze vboard at 10 20 90 165
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

[Congelare](freeze.md)
</dt> </dl>

 

