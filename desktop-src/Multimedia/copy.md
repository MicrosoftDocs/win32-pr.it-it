---
title: Copy (comando)
description: Il comando copy copia i dati negli Appunti. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- Copia comando Windows Multimedia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740498"
---
# <a name="copy-command"></a>Copy (comando)

Il comando copy copia i dati negli Appunti. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Uno dei flag seguenti che identifica l'elemento da copiare.



| Valore                 | Significato                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| al *rettangolo*        | Specifica la parte di ogni frame che verrà copiato. Se omesso, l'impostazione predefinita è l'intero frame.                                                                                                                             |
| *flusso* del flusso audio | Specifica il flusso audio nell'area di lavoro interessata dal comando. Se si usa questo flag e si vuole anche copiare il video, è necessario usare anche il flag "flusso video". Se non viene specificato alcun flag, vengono copiati tutti i flussi audio e video. |
| dalla *posizione*       | Specifica l'inizio dell'intervallo copiato. Se omesso, l'impostazione predefinita è la posizione corrente.                                                                                                                                         |
| *posizione*         | Specifica la fine dell'intervallo copiato. I dati audio e video copiati sono esclusivi di questa posizione. Se omesso, l'impostazione predefinita è la fine dell'area di lavoro.                                                                       |
| *flusso* del flusso video | Specifica il flusso video nell'area di lavoro interessata dal comando. Se si usa questo flag e si vuole anche copiare l'audio, è necessario usare anche il flag "flusso audio". Se non viene specificato alcun flag, vengono copiati tutti i flussi audio e video. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify", "test" o una combinazione di questi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

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

 

