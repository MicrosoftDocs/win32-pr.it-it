---
title: comando Load
description: Il comando Load carica un file in un formato specifico del dispositivo. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- comando carica Windows Multimedia
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742495"
---
# <a name="load-command"></a>comando Load

Il comando Load carica un file in un formato specifico del dispositivo. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*
</dt> <dd>

Percorso e nome del file da caricare. Per i dispositivi con sovrimpressione video, può includere anche un rettangolo di destinazione per i dati. Per specificare un rettangolo di destinazione, specificare "at" seguito da **x1 y1 x2 y2**, dove **X1 Y1** specificare l'angolo superiore sinistro del rettangolo e **X2 Y2** specificare la larghezza e l'altezza. Il rettangolo è relativo all'origine del buffer del video.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Il dispositivo "vidboard" Invia un messaggio di notifica al termine del caricamento.

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

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 

