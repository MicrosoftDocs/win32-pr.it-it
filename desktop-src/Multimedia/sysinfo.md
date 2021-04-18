---
title: comando sysinfo
description: Il comando sysinfo recupera le informazioni sul sistema MCI. Il comando sysinfo è un comando di sistema MCI; viene interpretato direttamente da MCI.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- comando di sysinfo Windows Multimedia
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302584"
---
# <a name="sysinfo-command"></a>comando sysinfo

Il comando sysinfo recupera le informazioni sul sistema MCI. Il comando sysinfo è un comando di sistema MCI; viene interpretato direttamente da MCI.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI o di un tipo di dispositivo. Se viene specificato un tipo di dispositivo, deve trattarsi di un nome di tipo dispositivo MCI standard, come elencato nel materiale di riferimento per il comando [**Capability**](capability.md) . È possibile specificare "All" quando il flag specificato in *lpszRequest* consente tale possibilità.

</dd> <dt>

*lpszRequest* 
</dt> <dd>

Uno dei flag seguenti.



| Valore                                                                                                                                                                | Significato                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <dt>**installname**</dt> </dl>               | Restituisce il nome elencato nel registro di sistema o il file di SYSTEM.INI usato per installare il dispositivo aperto con l'identificatore di dispositivo specificato.<br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <dt>**quantità**</dt> </dl>                        | Restituisce il numero di dispositivi MCI elencati nel registro di sistema o il file di SYSTEM.INI del tipo specificato nel parametro *lpszDeviceID* . Questo identificatore di dispositivo deve essere un nome di tipo dispositivo MCI standard. Eventuali cifre dopo il tipo di dispositivo verranno ignorate. Se si specifica "All" per *lpszDeviceID* , viene restituito il numero totale di dispositivi MCI nel sistema.<br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <dt>**quantità aperta**</dt> </dl>         | Restituisce il numero di dispositivi Open MCI del tipo specificato in *lpszDeviceID*. Questo identificatore di dispositivo deve essere un nome di tipo dispositivo MCI standard. Se si specifica "All" per *lpszDeviceID* , viene restituito il numero totale di dispositivi Open MCI presenti nel sistema.<br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <dt>* * name * index * * *</dt> </dl>                | Restituisce il nome di un dispositivo MCI. L'identificatore del dispositivo deve essere un nome di tipo dispositivo MCI standard. L' *Indice* è compreso tra 1 e il numero di dispositivi di quel tipo. Se per *lpszDeviceID* è specificato "All", *index* è compreso tra 1 e il numero totale di dispositivi nel sistema.<br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <dt>***Indice* nome aperto**</dt> </dl> | Restituisce il nome di un dispositivo MCI aperto. L'identificatore del dispositivo deve essere un nome di tipo dispositivo MCI standard. L' *Indice* è compreso tra 1 e il numero di dispositivi aperti del tipo di dispositivo. Se per *lpszDeviceID* è specificato "All", *index* è compreso tra 1 e il numero totale di dispositivi aperti nel sistema.<br/>                                          |



 

</dd> <dt>

*lpszFlags* 
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="examples"></a>Esempio

Il comando seguente restituisce il numero di dispositivi audio e di forma d'onda aperti.

``` syntax
sysinfo waveaudio quantity open
```

Il comando che segue restituisce il nome (alias del dispositivo) del primo dispositivo Open Waveform-Audio.

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

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[**funzionalità**](capability.md)
</dt> </dl>

 

