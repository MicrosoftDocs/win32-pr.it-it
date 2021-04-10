---
title: comando realizza
description: Il comando realizza indica a un dispositivo di selezionare e realizzare la relativa tavolozza nel contesto di visualizzazione della finestra visualizzata. I dispositivi digitali video riconoscono questo comando.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- realizzare il comando Windows Multimedia
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33accaa9638210adf4385a1776fcd8d2bd2021e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964780"
---
# <a name="realize-command"></a>comando realizza

Il comando realizza indica a un dispositivo di selezionare e realizzare la relativa tavolozza nel contesto di visualizzazione della finestra visualizzata. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*
</dt> <dd>

Uno dei flag seguenti.



| Valore      | Significato                                                                   |
|------------|---------------------------------------------------------------------------|
| background | Realizza la tavolozza come tavolozza di sfondo.                             |
| normale     | Realizza la tavolozza per una finestra di primo livello. Si tratta dell'impostazione predefinita. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Usare questo comando solo se l'applicazione usa un handle di finestra e riceve un messaggio **WM \_ QUERYNEWPALLETTE** o **WM \_ PALETTECHANGED** .

## <a name="examples"></a>Esempio

Il comando seguente indica al dispositivo "video" di realizzare la propria tavolozza.

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

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 

