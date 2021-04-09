---
title: comando Capture
description: Il comando Capture copia il contenuto del buffer del frame e lo archivia nel file specificato. I dispositivi digitali video riconoscono questo comando.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- comando Acquisisci Windows Multimedia
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121263"
---
# <a name="capture-command"></a>comando Capture

Il comando Capture copia il contenuto del buffer del frame e lo archivia nel file specificato. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*
</dt> <dd>

Uno o più dei flag seguenti:



| Valore          | Significato                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *nome percorso*  | Specifica il percorso e il nome file di destinazione per l'immagine acquisita. Questo flag è obbligatorio.                                                                                                                                                                |
| al *rettangolo* | Specifica l'area rettangolare all'interno del buffer di frame che il dispositivo Ritaglia e Salva su disco. Se omesso, l'area ritagliata viene impostata per impostazione predefinita sul rettangolo specificato o impostato come predefinito in un comando [put](put.md) "Source" precedente per questa istanza del dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify", "test" o una combinazione di questi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Questo comando può avere esito negativo se il dispositivo sta attualmente eseguendo il video di movimento o se è in esecuzione un'altra operazione a elevato utilizzo di risorse. Se il buffer del frame viene aggiornato in tempo reale, l'aggiornamento viene momentaneamente sospeso in modo che venga acquisita un'immagine completa. Se il dispositivo sospende l'aggiornamento, è possibile che si verifichi un effetto visivo o acustico. Se il formato di file, l'algoritmo di compressione e i livelli di qualità non sono stati impostati, vengono usate le impostazioni predefinite.

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

 

