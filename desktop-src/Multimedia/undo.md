---
title: comando undo
description: Il comando di annullamento inverte l'azione eseguita dal comando di copia, taglia, eliminazione, annullamento o incolla riuscito più recente. I dispositivi video digitali riconoscono questo comando.
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- comando undo Windows Multimedia
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec088f893b221a80cb3fe84c191a52874a8c29f5163ad3bcdaa8e68a9a4d4d2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804731"
---
# <a name="undo-command"></a>comando undo

Il comando di annullamento inverte l'azione eseguita dal comando di [copia,](copy.md) [taglia,](cut.md) [eliminazione,](delete.md)annullamento o incolla riuscito [più](paste.md) recente. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
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

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

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

[copy](copy.md)
</dt> <dt>

[Tagliare](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[Incollare](paste.md)
</dt> </dl>

 

