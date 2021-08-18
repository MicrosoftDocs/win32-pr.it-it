---
title: comando copy
description: Il comando copy copia i dati negli Appunti. I dispositivi video digitali riconoscono questo comando.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- Comando copy Windows Multimedia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3d103aae14b9dc13bb0d7d210d0412db993210bc788fa7fedd1a48a7216d59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144784"
---
# <a name="copy-command"></a>comando copy

Il comando copy copia i dati negli Appunti. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Uno dei flag seguenti che identifica l'elemento da copiare.



| Valore                 | Significato                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at *rectangle*        | Specifica la parte di ogni frame che verrà copiato. Se omesso, l'impostazione predefinita è l'intero frame.                                                                                                                             |
| flusso  audio | Specifica il flusso audio nell'area di lavoro interessata dal comando . Se si usa questo flag e si vuole anche copiare il video, è necessario usare anche il flag "flusso video". Se non viene specificato alcun flag, vengono copiati tutti i flussi audio e video. |
| dalla *posizione*       | Specifica l'inizio dell'intervallo copiato. Se omesso, l'impostazione predefinita è la posizione corrente.                                                                                                                                         |
| to *position*         | Specifica la fine dell'intervallo copiato. I dati audio e video copiati sono esclusivi di questa posizione. Se omesso, l'impostazione predefinita è la fine dell'area di lavoro.                                                                       |
| flusso  video | Specifica il flusso video nell'area di lavoro interessata dal comando . Se si usa questo flag e si vuole anche copiare l'audio, è necessario usare anche il flag "flusso audio". Se non viene specificato alcun flag, vengono copiati tutti i flussi audio e video. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

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
</dt> </dl>

 

