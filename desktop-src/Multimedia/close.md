---
title: Comando close (Corecrt \_ io.h)
description: Il comando close chiude il dispositivo o il file e tutte le risorse associate. MCI scarica un dispositivo quando tutte le istanze del dispositivo o tutti i file vengono chiusi. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- Comando close Windows Multimedia
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02acd3ebe3d45a402ae565c6fcac121f712df4374924bcb0e02c3dcadf9ceeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807960"
---
# <a name="close-command"></a>comando close

Il comando close chiude il dispositivo o il file e tutte le risorse associate. MCI scarica un dispositivo quando tutte le istanze del dispositivo o tutti i file vengono chiusi. Tutti i dispositivi MCI riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Per chiudere tutti i dispositivi aperti dall'applicazione, specificare l'identificatore di dispositivo "all" per il *parametro lpszDeviceID.*

La chiusura del **dispositivo cdaudio** interrompe la riproduzione audio.

**Windows 2000/XP:** Se il **dispositivo cdaudio** è in riproduzione, la chiusura del **dispositivo cdaudio** non causa l'interruzione della riproduzione dell'audio. Inviare prima [il comando stop.](stop.md)

## <a name="examples"></a>Esempio

Il comando seguente chiude il dispositivo "mysound".

``` syntax
close mysound
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Corecrt \_ io.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 

