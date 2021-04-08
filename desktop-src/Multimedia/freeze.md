---
title: blocca comando
description: Il comando Freeze consente di bloccare l'input video o l'output video in un VCR o di disabilitare l'acquisizione di video nel buffer del frame. I dispositivi Digital-video, video-overlay e VCR riconoscono questo comando.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- blocca il comando Windows Multimedia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047836"
---
# <a name="freeze-command"></a>blocca comando

Il comando Freeze consente di bloccare l'input video o l'output video in un VCR o di disabilitare l'acquisizione di video nel buffer del frame. I dispositivi Digital-video, video-overlay e VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*
</dt> <dd>

Flag che identifica gli elementi da bloccare. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Freeze** e i flag utilizzati da ogni tipo.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>digitalvideo</td>
<td>al <em>rettangolo</em></td>
<td>fuori</td>
</tr>
<tr class="even">
<td>overlay</td>
<td>al <em>rettangolo</em></td>

</tr>
<tr class="odd">
<td>VCR</td>
<td><ul>
<li>campo</li>
<li>frame</li>
</ul></td>
<td><ul>
<li>input</li>
<li>output</li>
</ul></td>
</tr>
</tbody>
</table>



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro *lpszFreezeFlags* e i relativi significati.



| Valore          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| al *rettangolo* | Specifica l'area che verrà bloccata. Per i dispositivi con sovrimpressione video, in questa area l'acquisizione video è disabilitata. Per i dispositivi video digitali, i pixel all'interno del rettangolo avranno il relativo bit di maschera di blocco acceso (a meno che non sia specificato il flag "esterno"). Il rettangolo è relativo all'origine del buffer video ed è specificato come *X1 Y1 Y1 2*. Le coordinate *X1 Y1* specificano l'angolo superiore sinistro del rettangolo e le coordinate *X2 Y2* specificano la larghezza e l'altezza. |
| campo          | Blocca il primo campo. Per impostazione predefinita, viene utilizzato il campo (se non viene specificato né frame né campo).                                                                                                                                                                                                                                                                                                                                                                                               |
| frame          | Blocca l'intero frame, visualizzando entrambi i campi.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| input          | Blocca il frame corrente dell'immagine di input, se è in pausa o in esecuzione.                                                                                                                                                                                                                                                                                                                                                                                                                |
| output         | Blocca il frame corrente dell'output dal VCR. Se il videoregistratore viene riprodotto quando viene eseguito il blocco, il frame corrente viene bloccato e il videoregistratore viene sospeso. Se il videoregistratore viene sospeso quando viene emesso questo comando, il frame corrente è bloccato. L'immagine bloccata rimane sul dispositivo di output fino a quando non viene emesso un comando di [Unfreeze](unfreeze.md) . Se non viene specificato né "input" né "output", viene utilizzato "output".                                                                                    |
| fuori        | Indica che l'area esterna all'area specificata utilizzando il flag "at" è bloccata.                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Se usato con i dispositivi VCR, questo comando è destinato alle schede di acquisizione dei frame.

Per specificare le aree di acquisizione irregolari con il flag "at", usare una serie di comandi Freeze e [Unfreeze](unfreeze.md) . Alcuni dispositivi con sovrimpressione video limitano la complessità dell'area di acquisizione.

Questo comando è supportato solo se una chiamata al comando [Capability](capability.md) con il flag "Can Freeze" restituisce **true**.

## <a name="examples"></a>Esempio

Il comando che segue Disabilita l'acquisizione di video in un quadrato di 100 pixel nell'angolo superiore sinistro del buffer video.

``` syntax
freeze vboard at 0 0 100 100
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
</dt> <dt>

[capability](capability.md)
</dt> <dt>

[Sblocca](unfreeze.md)
</dt> </dl>

 

