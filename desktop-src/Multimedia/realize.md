---
title: Comando realize
description: Il comando realize indica a un dispositivo di selezionare e realizzare la tavolozza nel contesto di visualizzazione della finestra visualizzata. I dispositivi video digitali riconoscono questo comando.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- Comando realize Windows Multimedia
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0aba1e610f4636c7dbfb71fbc959d9b4b8496cc23e91a97100ef6edce133b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371436"
---
# <a name="realize-command"></a>Comando realize

Il comando realize indica a un dispositivo di selezionare e realizzare la tavolozza nel contesto di visualizzazione della finestra visualizzata. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*
</dt> <dd>

Uno dei flag seguenti.



| Valore      | Significato                                                                   |
|------------|---------------------------------------------------------------------------|
| background | Rende la tavolozza come tavolozza di sfondo.                             |
| normale     | Rende possibile la tavolozza per una finestra di primo livello. Si tratta dell'impostazione predefinita. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Usare questo comando solo se l'applicazione usa un handle di finestra e riceve un messaggio **WM \_ QUERYNEWPALLETTE** o **WM \_ PALETTECHANGED.**

## <a name="examples"></a>Esempio

Il comando seguente indica al dispositivo "myvideo" di realizzare la tavolozza.

``` syntax
realize myvideo normal
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
</dt> </dl>

 

