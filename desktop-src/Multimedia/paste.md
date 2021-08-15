---
title: Comando Incolla
description: Il comando Incolla copia il contenuto degli Appunti nell'area di lavoro. I dispositivi video digitali riconoscono questo comando.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- Comando Incolla Windows Multimediali
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b93f042193c50a810ac23285224ddd234a23b2070f8db2d56d216fee037c37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373216"
---
# <a name="paste-command"></a>Comando Incolla

Il comando Incolla copia il contenuto degli Appunti nell'area di lavoro. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come segue.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Uno o più dei flag seguenti.



| Valore                 | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at *rectangle*        | Specifica la posizione all'interno del frame in cui vengono incollati i dati. L'angolo superiore sinistro del *rettangolo* corrisponde all'angolo superiore sinistro dei dati aggiunti. Se le dimensioni del rettangolo sono diverse da zero in X o Y, il contenuto degli Appunti viene ridimensionato in tali dimensioni quando vengono incollati nel frame. Se omesso, il *rettangolo viene* utilizzato per impostazione predefinita per l'intero frame. Se questo flag viene specificato in modalità di inserimento (impostazione predefinita), qualsiasi area esterna al rettangolo viene disegnata con un colore a tinta unita.                       |
| flusso  audio | Specifica il flusso audio nell'area di lavoro interessata dal comando . Se negli Appunti è presente un solo flusso audio, i dati audio vengono incollati nel flusso *designato.* Se negli Appunti sono presenti più flussi audio, il *flusso* indica il numero iniziale per le sequenze di flusso. Se si usa questo flag e si vuole anche incollare video, è necessario usare anche il flag "flusso video". Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati e conservano i numeri di flusso originali. |
| insert                | Specifica che i dati vengono inseriti nell'area di lavoro. Tutti i dati dopo il punto di inserimento vengono spostati in avanti nell'area di lavoro per fare spazio. Si tratta del valore predefinito.                                                                                                                                                                                                                                                                                                                                                    |
| overwrite             | Specifica che i dati vengono copiati nell'area di lavoro scrivendo su tutti i dati esistenti dopo il punto di inserimento. I flag "insert" e "overwrite" influiscono sull'eliminazione o lo spostamento dei frame durante l'operazione Incolla, non sulla modalità di incolla dei dati all'interno di ogni frame.                                                                                                                                                                                                                                              |
| to *position*         | Specifica la posizione nell'area di lavoro in cui vengono incollati i dati. Se omesso, il valore predefinito è la posizione corrente.                                                                                                                                                                                                                                                                                                                                                                                                    |
| flusso  video | Specifica il flusso video nell'area di lavoro interessata dal comando . Se negli Appunti è presente un solo flusso video, i dati video vengono incollati nel flusso *designato.* Se negli Appunti è presente più di un flusso video, il *flusso* indica il numero iniziale per le sequenze di flusso. Se si usa questo flag e si vuole anche incollare l'audio, è necessario usare anche il flag "flusso audio". Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati e conservano i numeri di flusso originali. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Non sono presenti segnali nei dati copiati dagli Appunti. La modifica diventa permanente solo quando i dati vengono salvati in modo esplicito. Tuttavia, la riproduzione funziona come se i dati siano stati aggiunti.

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

 

