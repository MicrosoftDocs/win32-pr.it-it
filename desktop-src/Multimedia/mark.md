---
title: comando Mark
description: Il comando Mark controlla la registrazione e l'eliminazione dei contrassegni sul nastro. I dispositivi VCR riconoscono questo comando.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- contrassegna il comando Windows Multimedia
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570968af05424597a7fe2b59e86e0364694e0e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301468"
---
# <a name="mark-command"></a>comando Mark

Il comando Mark controlla la registrazione e l'eliminazione dei contrassegni sul nastro. I dispositivi VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*
</dt> <dd>

Uno dei flag seguenti.



| Valore | Significato                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| erase | Cancella un contrassegno in corrispondenza della posizione corrente, se presente. Per cancellare un contrassegno, cercare innanzitutto il contrassegno e quindi eseguire il comando "Erase" del contrassegno. |
| scrittura | Scrive un contrassegno nella posizione corrente. È possibile che il VCR debba essere in modalità riproduzione o registrazione affinché il comando abbia esito positivo.                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I contrassegni sono segnali speciali scritti nel contenuto che possono essere rilevati dal VCR durante le ricerche ad alta velocità. I contrassegni sono specifici del VCR.

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

 

