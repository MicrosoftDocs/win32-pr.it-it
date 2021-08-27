---
title: comando cue
description: Il comando cue si prepara per la riproduzione o la registrazione. I dispositivi video digitale, VCR e audio waveform riconoscono questo comando.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- Comando cue Windows Multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6398d4773b6c92332e8a95996e4d81941a073fe
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467858"
---
# <a name="cue-command"></a>comando cue

Il comando cue si prepara per la riproduzione o la registrazione. I dispositivi video digitale, VCR e audio waveform riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*
</dt> <dd>

Flag che prepara un dispositivo per la riproduzione o la registrazione. La tabella seguente elenca i tipi di dispositivo che riconoscono il **comando cue** e i flag usati da ogni tipo.




| valore | Segnale | Segnale | 
|-------|-----|-----|
| digitalvideo | <ul><li>input</li><li>noshow</li></ul> | <ul><li>output</li><li>to <em>position</em></li></ul> | 
| Vcr | <ul><li>dalla <em>posizione</em></li><li>input</li><li>output</li></ul> | <ul><li>Preroll</li><li>reverse</li><li>to <em>position</em></li></ul> | 
| Waveaudio | input | output | 




 

La tabella seguente elenca i flag che possono essere specificati nel *parametro lpszInOutTo* e i relativi significati.



| valore           | Significato                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dalla *posizione* | Indica dove iniziare.                                                                                                                                                                                                                                                                                      |
| input           | Prepara la registrazione. Per i dispositivi video digitali, questo flag può essere omesso se l'origine di presentazione corrente è già l'input esterno.                                                                                                                                                                  |
| noshow          | Prepara la riproduzione di un frame senza visualizzarlo. Quando si specifica questo flag, la visualizzazione continua a mostrare l'immagine nel buffer dei frame anche se il frame corrispondente non è la posizione corrente. Un comando di segnale successivo senza questo flag e senza il flag "to" visualizza il frame corrente. |
| output          | Prepara per la riproduzione. Se non vengono specificati né "input" né "output", l'impostazione predefinita è "output".                                                                                                                                                                                                           |
| Preroll         | Sposta la distanza del preroll *dall'oggetto nel punto*. Il punto in è la posizione corrente o la posizione specificata dal flag "from".                                                                                                                                                                            |
| reverse         | Indica che la direzione di riproduzione è inversa (indietro).                                                                                                                                                                                                                                                             |
| to *position*   | Sposta l'area di lavoro nella posizione specificata. Per i dispositivi vcr, questo flag indica dove arrestarsi.                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Anche se non è necessario, l'esecuzione del comando di segnale prima della riproduzione o della registrazione in alcuni dispositivi potrebbe ridurre il ritardo prima che il dispositivo inizi l'azione.

Questo comando ha esito negativo se è in corso la riproduzione o la registrazione o se il dispositivo è in pausa.

Quando si esegue il segnale per la riproduzione (usando [](play.md) il segnale "output"), l'emissione del comando di riproduzione con il flag "from", "to" o "reverse" annulla il comando cue.

Quando si usa il segnale "input" per la registrazione, l'esecuzione del comando [di registrazione](record.md) con il flag "from", "to" o "initialize" annulla il comando cue.

## <a name="examples"></a>Esempio

Il comando seguente prepara il dispositivo "mysound" per la registrazione.

``` syntax
cue mysound input
```

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[Giocare](play.md)
</dt> <dt>

[Registrazione](record.md)
</dt> </dl>

 

