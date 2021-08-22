---
title: comando restore
description: Il comando restore copia un'immagine fissa da un file nel buffer dei frame. Questo è il contrario del comando capture. I dispositivi video digitali riconoscono questo comando.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- Comando restore Windows Multimedia
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e82fdec2480cfe2fc1b41901872aef7e41ee468d1adc3924df17a27e40031e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689191"
---
# <a name="restore-command"></a>comando restore

Il comando restore copia un'immagine fissa da un file nel buffer dei frame. Questo è il contrario del [comando capture.](capture.md) I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come segue.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*
</dt> <dd>

Uno o più dei flag seguenti.



| Valore           | Significato                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at *rectangle*  | Specifica un rettangolo relativo all'origine del buffer dei frame. Il *rettangolo* viene specificato *come X1 Y1 X2 Y2*. Le coordinate *X1 Y1* specificano l'angolo superiore sinistro e le coordinate *X2 Y2* specificano la larghezza e l'altezza. Se questo flag non viene usato, l'immagine viene copiata nell'angolo superiore sinistro del buffer dei frame.<br/> |
| da nome *file* | Specifica il nome file dell'immagine da richiamare. Questo flag è obbligatorio.                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I dispositivi possono riconoscere un'ampia gamma di formati di immagine. Una Windows bitmap indipendente dal dispositivo viene sempre riconosciuta.

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

[Catturare](capture.md)
</dt> </dl>

 

