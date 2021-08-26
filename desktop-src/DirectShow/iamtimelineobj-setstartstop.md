---
description: Il metodo SetStartStop imposta le ore di inizio e arresto dell'oggetto rispetto all'elemento padre dell'oggetto.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: Metodo IAMTimelineObj::SetStartStop (Qedit.h)
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
ms.openlocfilehash: e2806d926c9842f5900f46f923f4cbdf8caa47f112e1832077ab7d2b80a9341c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052451"
---
# <a name="iamtimelineobjsetstartstop-method"></a>Metodo IAMTimelineObj::SetStartStop

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo imposta le ore di inizio e arresto `SetStartStop` dell'oggetto rispetto all'elemento padre dell'oggetto.

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

Nuova ora di inizio, in unità da 100 nanosecondi o -1 per mantenere l'ora di inizio esistente.

</dd> <dt>

*Stop* 
</dt> <dd>

Nuovo tempo di arresto, in unità da 100 nanosecondi o -1 per mantenere l'ora di arresto esistente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                  | Descrizione                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Non implementato.<br/>  |



 

## <a name="remarks"></a>Commenti

Le tracce, le composizioni e i gruppi non implementano questo metodo. Per questi oggetti, l'ora di inizio è sempre zero e l'ora di arresto è il tempo massimo di arresto degli oggetti che contengono.

Non impostare orari sovrapposti sugli oggetti di origine all'interno della stessa traccia. Questa operazione può causare comportamenti non definiti.

Per gli oggetti di origine, i tempi di avvio e arresto sono indipendenti dai tempi di avvio e arresto dei supporti. La modifica di una coppia di valori non modifica l'altra. Per impostare le ore di avvio e arresto dei supporti, chiamare il [**metodo IAMTimelineSrc::SetMediaTimes.**](iamtimelinesrc-setmediatimes.md) Per altre informazioni, vedere [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Per ottenere le transizioni e i tagli accurati del frame, impostare i *parametri Start* e *Stop* sui limiti del frame. È possibile usare il metodo [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) per convertire un valore temporale nel limite del frame più vicino oppure usare la funzione seguente per eseguire la conversione dal numero di fotogramma all'ora di riferimento:


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
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




