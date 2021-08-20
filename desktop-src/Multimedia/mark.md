---
title: comando mark
description: Il comando mark controlla la registrazione e la cancellazione dei contrassegni nella videotape. I dispositivi vcr riconoscono questo comando.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- Comando mark Windows Multimedia
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f59f56a6d542120d088d764d1b301329a7f0b167f25952587a9e743878643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138752"
---
# <a name="mark-command"></a>comando mark

Il comando mark controlla la registrazione e la cancellazione dei contrassegni nella videotape. I dispositivi vcr riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*
</dt> <dd>

Uno dei flag seguenti.



| Valore | Significato                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| erase | Cancella un segno nella posizione corrente, se presente. Per cancellare un contrassegno, cercare prima di tutto il contrassegno e quindi eseguire il comando mark "erase". |
| scrivere | Scrive un segno nella posizione corrente. Potrebbe essere necessario che il videoregistratore sia in modalità di riproduzione o registrazione per il successo del comando.                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o "test". Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I contrassegni sono segnali speciali scritti nel contenuto che possono essere rilevati dal videoregistratore durante ricerche ad alta velocità. I contrassegni sono specifici del videoregistratore.

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

 

