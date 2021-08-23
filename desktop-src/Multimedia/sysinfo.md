---
title: Comando sysinfo
description: Il comando sysinfo recupera le informazioni di sistema MCI. Il comando sysinfo è un comando di sistema MCI. viene interpretato direttamente da MCI.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- Comando sysinfo Windows Multimedia
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0af11370fd3968a2f5a6cf296ea04507f18d517665071674cfa8a4573e1a4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688331"
---
# <a name="sysinfo-command"></a>Comando sysinfo

Il comando sysinfo recupera le informazioni di sistema MCI. Il comando sysinfo è un comando di sistema MCI. viene interpretato direttamente da MCI.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come segue.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszDeviceID* 
</dt> <dd>

Identificatore di un dispositivo o di un tipo di dispositivo MCI. Se viene specificato un tipo di dispositivo, deve essere un nome di tipo di dispositivo MCI standard, come elencato nel materiale di riferimento per il [**comando capability.**](capability.md) È possibile specificare "all" quando il flag specificato in *lpszRequest* consente tale possibilità.

</dd> <dt>

*lpszRequest* 
</dt> <dd>

Uno dei flag seguenti.



| Valore                                                                                                                                                                | Significato                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <dt>**installname**</dt> </dl>               | Restituisce il nome elencato nel Registro di sistema o il file SYSTEM.INI usato per installare il dispositivo aperto con l'identificatore di dispositivo specificato.<br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <dt>**Quantità**</dt> </dl>                        | Restituisce il numero di dispositivi MCI elencati nel Registro di sistema o nel file SYSTEM.INI del tipo specificato nel *parametro lpszDeviceID.* Questo identificatore di dispositivo deve essere un nome di tipo di dispositivo MCI standard. Tutte le cifre dopo il tipo di dispositivo vengono ignorate. Se si specifica "all" per *lpszDeviceID,* viene restituito il numero totale di dispositivi MCI nel sistema.<br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <dt>**quantity open**</dt> </dl>         | Restituisce il numero di dispositivi MCI aperti del tipo specificato in *lpszDeviceID*. Questo identificatore di dispositivo deve essere un nome di tipo di dispositivo MCI standard. Se si specifica "all" per *lpszDeviceID,* viene restituito il numero totale di dispositivi MCI aperti nel sistema.<br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <dt>**name *index***</dt> </dl>                | Restituisce il nome di un dispositivo MCI. L'identificatore del dispositivo deve essere un nome di tipo di dispositivo MCI standard. *L'indice* è compreso tra 1 e il numero di dispositivi di quel tipo. Se per *lpszDeviceID* viene specificato  "all", l'indice è compreso tra 1 e il numero totale di dispositivi nel sistema.<br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <dt>**name *index* open**</dt> </dl> | Restituisce il nome di un dispositivo MCI aperto. L'identificatore del dispositivo deve essere un nome di tipo di dispositivo MCI standard. *L'indice* è compreso tra 1 e il numero di dispositivi aperti di quel tipo di dispositivo. Se per *lpszDeviceID* viene specificato  "all", l'indice è compreso tra 1 e il numero totale di dispositivi aperti nel sistema.<br/>                                          |



 

</dd> <dt>

*lpszFlags* 
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="examples"></a>Esempio

Il comando seguente restituisce il numero di dispositivi audio waveform aperti.

``` syntax
sysinfo waveaudio quantity open
```

Il comando seguente restituisce il nome (alias del dispositivo) del primo dispositivo audio waveform aperto.

``` syntax
sysinfo waveaudio name 1 open
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

[**Capacità**](capability.md)
</dt> </dl>

 

