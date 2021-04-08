---
title: Sblocca comando
description: Il comando Unfreeze riabilita l'acquisizione video nel buffer del frame dopo che è stata disabilitata tramite il comando Freeze. I dispositivi Digital-video, VCR e overlay video riconoscono questo comando.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- sbloccare il comando Windows Multimedia
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743559"
---
# <a name="unfreeze-command"></a>Sblocca comando

Il comando Unfreeze riabilita l'acquisizione video nel buffer del frame dopo che è stata disabilitata tramite il comando [Freeze](freeze.md) . I dispositivi Digital-video, VCR e overlay video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*
</dt> <dd>

Flag per la riabilitazione dell'acquisizione video nel buffer del frame. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Unfreeze** e i flag utilizzati da ogni tipo.



| Valore        | Significato        |
|--------------|----------------|
| digitalvideo | al *rettangolo* |
| overlay      | al *rettangolo* |
| VCR          | input output   |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszUnfreeze** e i relativi significati.



| Valore          | Significato                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| al *rettangolo* | Specifica l'area in cui sarà riabilitata l'acquisizione dei video. Il rettangolo è relativo all'origine del buffer video ed è specificato come *X1 Y1 Y1 2*. Le coordinate *X1 Y1* specificano l'angolo superiore sinistro del rettangolo e le coordinate *X2 Y2* specificano la larghezza e l'altezza. |
| input          | Sbloccare l'immagine di input.                                                                                                                                                                                                                                                                  |
| output         | Sbloccare l'immagine di output. Se non viene specificato né "input" né "output", viene utilizzato "output".                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="examples"></a>Esempio

Il comando seguente Sblocca un'area del buffer video.

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

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[congelare](freeze.md)
</dt> </dl>

 

