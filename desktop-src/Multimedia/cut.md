---
title: Taglia comando
description: Il comando taglia rimuove i dati dall'area di lavoro e li copia negli Appunti. I dispositivi digitali video riconoscono questo comando.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- taglia il comando Windows Multimedia
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964727"
---
# <a name="cut-command"></a>Taglia comando

Il comando taglia rimuove i dati dall'area di lavoro e li copia negli Appunti. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Uno dei flag seguenti che identifica l'elemento da tagliare.



| Valore                 | Significato                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| al *rettangolo*        | Specifica la parte di ogni taglia del fotogramma. Se omesso, il valore predefinito è l'intero frame. Quando si specifica questo elemento, i frame non vengono eliminati. L'area all'interno del rettangolo diventa invece nero.                                       |
| *flusso* del flusso audio | Specifica il flusso audio nell'area di lavoro interessata dal comando. Se si usa questo flag e si vuole anche tagliare video, è necessario usare anche il flag "flusso video". Se non viene specificato alcun flag, vengono tagliati tutti i flussi audio e video. |
| dalla *posizione*       | Specifica l'inizio del taglio dell'intervallo. Se omesso, il valore predefinito è la posizione corrente.                                                                                                                                                |
| *posizione*         | Specifica la fine del taglio dell'intervallo. Il taglio di dati audio e video è escluso da questa posizione. Se omesso, il valore predefinito è la fine dell'area di lavoro.                                                                                  |
| *flusso* del flusso video | Specifica il flusso video nell'area di lavoro interessata dal comando. Se si usa questo flag e si vuole anche tagliare audio, è necessario usare anche il flag "flusso audio". Se non viene specificato alcun flag, vengono tagliati tutti i flussi audio e video. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify", "test" o una combinazione di questi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

La modifica diventa permanente solo quando i dati vengono salvati in modo esplicito; Tuttavia, la riproduzione funziona come se i dati fossero stati rimossi.

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

 

