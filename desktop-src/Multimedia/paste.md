---
title: comando Incolla
description: Il comando Incolla copia il contenuto degli Appunti nell'area di lavoro. I dispositivi digitali video riconoscono questo comando.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- comando Incolla Windows Multimedia
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048050"
---
# <a name="paste-command"></a>comando Incolla

Il comando Incolla copia il contenuto degli Appunti nell'area di lavoro. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
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

Uno o più dei flag seguenti.



| Valore                 | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| al *rettangolo*        | Specifica la posizione all'interno del frame in cui vengono incollati i dati. L'angolo superiore sinistro del *rettangolo* corrisponde all'angolo superiore sinistro dei dati aggiunti. Se il rettangolo ha una dimensione diversa da zero in X o Y, il contenuto degli Appunti viene ridimensionato in tali dimensioni quando vengono incollate nel frame. Se omesso, il *rettangolo* viene impostato per impostazione predefinita sull'intero frame. Se questo flag viene specificato in modalità "Insert" (impostazione predefinita), qualsiasi area esterna al rettangolo viene disegnata con un colore a tinta unita.                       |
| *flusso* del flusso audio | Specifica il flusso audio nell'area di lavoro interessata dal comando. Se negli Appunti è presente un solo flusso audio, i dati audio vengono incollati nel *flusso* designato. Se negli Appunti è presente più di un flusso audio, il *flusso* indica il numero iniziale per le sequenze di flusso. Se si usa questo flag e si vuole anche incollare il video, è necessario usare anche il flag "flusso video". Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati e mantengono i numeri di flusso originali. |
| insert                | Specifica che i dati vengono inseriti nell'area di lavoro. Tutti i dati successivi al punto di inserimento vengono spostati nell'area di lavoro per fare spazio. Si tratta del valore predefinito.                                                                                                                                                                                                                                                                                                                                                    |
| overwrite             | Specifica che i dati vengono copiati nell'area di lavoro scrivendo su tutti i dati esistenti dopo il punto di inserimento. I flag "Insert" e "overwrite" influiscono sul fatto che i frame vengano eliminati o spostati durante l'operazione Incolla, non su come i dati vengono incollati all'interno di ogni frame.                                                                                                                                                                                                                                              |
| *posizione*         | Specifica la posizione nell'area di lavoro in cui vengono incollati i dati. Se omesso, il valore predefinito è la posizione corrente.                                                                                                                                                                                                                                                                                                                                                                                                    |
| *flusso* del flusso video | Specifica il flusso video nell'area di lavoro interessata dal comando. Se negli Appunti è presente un solo flusso video, i dati video vengono incollati nel *flusso* designato. Se negli Appunti è presente più di un flusso video, il *flusso* indica il numero iniziale per le sequenze di flusso. Se si usa questo flag e si vuole anche incollare audio, è necessario usare anche il flag "flusso audio". Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati e mantengono i numeri di flusso originali. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify", "test" o una combinazione di questi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Nessun segnale presente nei dati copiati dagli Appunti. La modifica diventa permanente solo quando i dati vengono salvati in modo esplicito; Tuttavia, la riproduzione funge da se i dati sono stati aggiunti.

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

 

