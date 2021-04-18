---
description: Il metodo SetStartStop imposta l'ora di inizio e di fine dell'oggetto, relativa all'elemento padre dell'oggetto.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'Metodo IAMTimelineObj:: SetStartStop (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330809"
---
# <a name="iamtimelineobjsetstartstop-method"></a>Metodo IAMTimelineObj:: SetStartStop

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetStartStop` metodo imposta l'ora di inizio e di fine dell'oggetto, relativa all'elemento padre dell'oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Inizia* 
</dt> <dd>

Nuova ora di inizio, in unità 100-nanosecondi, oppure-1 per la conservazione dell'ora di inizio esistente.

</dd> <dt>

*Stop* 
</dt> <dd>

Nuova ora di arresto, in unità 100-nanosecondi, oppure-1 per la conservazione dell'ora di arresto esistente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                  | Descrizione                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Non implementato.<br/>  |



 

## <a name="remarks"></a>Commenti

Tracce, composizioni e gruppi non implementano questo metodo. Per questi oggetti, l'ora di inizio è sempre zero e l'ora di arresto è l'ora di arresto massima degli oggetti in essi contenuti.

Non impostare orari sovrapposti negli oggetti di origine all'interno della stessa traccia. Questa operazione può causare comportamenti indefiniti.

Per gli oggetti di origine, le ore di inizio e di fine sono indipendenti dagli orari di inizio e di fine del supporto. La modifica di una coppia di valori non comporta la modifica dell'altro. Per impostare l'ora di inizio e di fine del supporto, chiamare il metodo [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . Per ulteriori informazioni, vedere [tempo in servizi di modifica DirectShow](time-in-directshow-editing-services.md).

Per ottenere le transizioni e i tagli accurati dei frame, impostare i parametri *Start* e *Stop* sui limiti del frame. È possibile usare il metodo [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) per convertire un valore di ora nel limite di frame più vicino oppure usare la funzione seguente per eseguire la conversione da un numero di frame all'ora di riferimento:


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




