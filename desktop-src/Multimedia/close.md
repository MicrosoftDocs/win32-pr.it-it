---
title: comando Close (Corecrt \_ io. h)
description: Il comando Chiudi chiude il dispositivo o il file e tutte le risorse associate. MCI Scarica un dispositivo quando vengono chiuse tutte le istanze del dispositivo o tutti i file. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- Chiudi comando Windows Multimedia
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
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964100"
---
# <a name="close-command"></a>Chiudi comando

Il comando Chiudi chiude il dispositivo o il file e tutte le risorse associate. MCI Scarica un dispositivo quando vengono chiuse tutte le istanze del dispositivo o tutti i file. Tutti i dispositivi MCI riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Per chiudere tutti i dispositivi aperti dall'applicazione, specificare l'identificatore di dispositivo "All" per il parametro *lpszDeviceID* .

La chiusura del dispositivo **CDAudio** interrompe la riproduzione audio.

**Windows 2000/XP:** Se il dispositivo **CDAudio** è in esecuzione, la chiusura del dispositivo **CDAudio** non comporta l'interruzione della riproduzione dell'audio. Inviare prima il comando [Stop](stop.md) .

## <a name="examples"></a>Esempio

Il comando seguente chiude il dispositivo "audio".

``` syntax
close mysound
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>\_Io. h Corecrt</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 

