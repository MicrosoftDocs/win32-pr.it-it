---
description: Il metodo CheckStreamState determina se un campione multimediale deve essere recapitato o rimosso.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Metodo CBaseStreamControl. CheckStreamState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326565"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a>CBaseStreamControl. CheckStreamState, metodo

Il `CheckStreamState` metodo determina se un campione multimediale deve essere recapitato o rimosso.

## <a name="syntax"></a>Sintassi


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                                       | Descrizione                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**ELIMINAZIONE di flussi \_**</dt> </dl> | Rimuovere l'esempio.<br/> |
| <dl> <dt>**flusso di flusso \_**</dt> </dl>    | Fornire questo esempio.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo quando il pin riceve un campione. Recapitare l'esempio solo se il valore restituito è flusso di flusso \_ . Se il valore restituito è il flusso che viene \_ ignorato, eliminare l'esempio.

Se il pin Elimina tutti gli esempi, deve contrassegnare l'esempio successivo che recapita come discontinuità, chiamando il metodo [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

Se il filtro implementa l'interfaccia [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) per contare il numero di frame eliminati, non contare un frame scartato come frame eliminato.

Quando il valore restituito è il flusso che viene \_ ignorato, il metodo si blocca fino a quando non viene raggiunta l'ora di inizio del campione. In questo modo si impedisce al pin di ignorare troppo rapidamente i campioni. Se il filtro è sospeso, il tempo di attesa è infinito, fino a quando il filtro non viene eseguito, interrompe o Scarica i dati. (Le modifiche allo stato del filtro e lo streaming avvengono su thread separati, quindi non viene generato alcun deadlock).

L'enumerazione **CBaseStreamControl:: StreamControlState** viene definita nel modo seguente:


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a>Esempio

Nell'esempio seguente si presuppone che il pin usi una variabile membro denominata m \_ fLastSampleDiscarded per tenere traccia delle discontinuità.


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




