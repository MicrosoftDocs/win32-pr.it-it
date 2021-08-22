---
title: Comando taglia
description: Il comando taglia rimuove i dati dall'area di lavoro e li copia negli Appunti. I dispositivi video digitali riconoscono questo comando.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- Comando taglia Windows Multimediali
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a39010ad7dd07ccff38291441bb0aa05a54ee65da1b865d7ac82ed77fbfdd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144564"
---
# <a name="cut-command"></a>Comando taglia

Il comando taglia rimuove i dati dall'area di lavoro e li copia negli Appunti. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
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

Uno dei flag seguenti che identifica l'elemento da tagliare.



| Valore                 | Significato                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at *rectangle*        | Specifica la parte di ogni taglio del frame. Se omesso, per impostazione predefinita viene utilizzato l'intero frame. Quando questo elemento viene specificato, i frame non vengono eliminati. L'area all'interno del rettangolo diventa invece nera.                                       |
| flusso  audio | Specifica il flusso audio nell'area di lavoro interessata dal comando . Se si usa questo flag e si vuole anche tagliare il video, è necessario usare anche il flag "flusso video". Se non viene specificato alcun flag, vengono tagliati tutti i flussi audio e video. |
| dalla *posizione*       | Specifica l'inizio del taglio dell'intervallo. Se omesso, il valore predefinito è la posizione corrente.                                                                                                                                                |
| to *position*         | Specifica la fine del taglio dell'intervallo. I dati audio e video tagliati sono esclusivi di questa posizione. Se omesso, il valore predefinito è la fine dell'area di lavoro.                                                                                  |
| flusso  video | Specifica il flusso video nell'area di lavoro interessata dal comando . Se si usa questo flag e si vuole anche tagliare l'audio, è necessario usare anche il flag "flusso audio". Se non viene specificato alcun flag, vengono tagliati tutti i flussi audio e video. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

La modifica diventa permanente solo quando i dati vengono salvati in modo esplicito. Tuttavia, la riproduzione funziona come se i dati siano stati rimossi.

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

 

