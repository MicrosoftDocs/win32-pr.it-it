---
title: Comando capture
description: Il comando capture copia il contenuto del buffer dei frame e lo archivia nel file specificato. I dispositivi video digitali riconoscono questo comando.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- Comando capture Windows Multimedia
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68bc32fd247cbe3519fbffad778b33679e3b71c652b476f557db5a910e87721c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941519"
---
# <a name="capture-command"></a>Comando capture

Il comando capture copia il contenuto del buffer dei frame e lo archivia nel file specificato. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*
</dt> <dd>

Uno o più dei flag seguenti:



| Valore          | Significato                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| as *pathname*  | Specifica il percorso e il nome file di destinazione per l'immagine acquisita. Questo flag è obbligatorio.                                                                                                                                                                |
| at *rectangle* | Specifica l'area rettangolare all'interno del buffer dei frame che il dispositivo ritaglia e salva su disco. Se omesso, per impostazione predefinita l'area ritagliata viene impostata sul rettangolo specificato o sul valore predefinito di un comando [put](put.md) "source" precedente per questa istanza del dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo comando potrebbe non riuscire se il dispositivo sta riproducendo video in movimento o sta eseguendo altre operazioni a elevato utilizzo di risorse. Se il buffer dei frame viene aggiornato in tempo reale, l'aggiornamento viene temporaneamente sospeso in modo che venga acquisita un'immagine completa. Se il dispositivo sospende l'aggiornamento, potrebbe esserci un effetto visivo o acustico. Se il formato di file, l'algoritmo di compressione e i livelli di qualità non sono stati impostati, vengono usati i relativi valori predefiniti.

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

[Mettere](put.md)
</dt> </dl>

 

