---
title: comando escape
description: Il comando escape invia informazioni specifiche del dispositivo a un dispositivo. I dispositivi videodisco riconoscono questo comando.
ms.assetid: 16e0e2b6-6d98-440a-86c1-eca8201ad61a
keywords:
- comando escape Windows Multimedia
topic_type:
- apiref
api_name:
- escape
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b04f7a2ef6c2e91adc9b24a044d0a7e941843f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300960"
---
# <a name="escape-command"></a>comando escape

Il comando escape invia informazioni specifiche del dispositivo a un dispositivo. I dispositivi videodisco riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("escape %s %s %s"), 
  lpszDeviceID, 
  lpszEscape, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*
</dt> <dd>

Informazioni personalizzate da inviare al dispositivo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="examples"></a>Esempio

Il comando seguente invia la stringa di escape "SA" al dispositivo videodisco.

``` syntax
escape videodisc SA
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

 

