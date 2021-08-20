---
title: Load (comando)
description: Il comando load carica un file in un formato specifico del dispositivo. I dispositivi di sovrimpressione video e digitale riconoscono questo comando.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- Comando load Windows Multimedia
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c66822de727ea45e93839c710dae19739cba8adaac8b571846c1fa23ef0083c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139356"
---
# <a name="load-command"></a>Load (comando)

Il comando load carica un file in un formato specifico del dispositivo. I dispositivi di sovrimpressione video e digitale riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*
</dt> <dd>

Percorso e nome file da caricare. Per i dispositivi con sovrimpressione video, può includere anche un rettangolo di destinazione per i dati. Per specificare un rettangolo di destinazione, specificare "at" seguito da **X1 Y1 X2 Y2**, dove **X1 Y1 specifica** l'angolo superiore sinistro del rettangolo e **X2 Y2** specificare la larghezza e l'altezza. Il rettangolo è relativo all'origine del buffer video.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il dispositivo "vidboard" invia un messaggio di notifica al termine del caricamento.

## <a name="examples"></a>Esempio

Il comando seguente carica un file nel dispositivo "vidboard".

``` syntax
load vidboard c:\vid\fish.vid notify
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

 

