---
description: Il metodo GetVideoPaletteEntries recupera un intervallo di voci della tavolozza per il video.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Metodo CBaseControlVideo.GetVideoPaletteEntries (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5eb1c017353ed3e5095f5ee5d24870773c11211c14eaa44a673b4f12913c56c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057041"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a>Metodo CBaseControlVideo.GetVideoPaletteEntries

Il `GetVideoPaletteEntries` metodo recupera un intervallo di voci della tavolozza per il video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Startindex* 
</dt> <dd>

Voce della tavolozza iniziale in base zero.

</dd> <dt>

*Voci* 
</dt> <dd>

Numero di voci necessarie.

</dd> <dt>

*pRetrieved* 
</dt> <dd>

Puntatore al numero di colori ottenuti.

</dd> <dt>

*pPalette* 
</dt> <dd>

Puntatore al buffer di output per i colori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR in caso di esito positivo, VFW E NO PALETTE AVAILABLE se i campioni video non hanno una tavolozza dei colori, E OUTOFMEMORY se la memoria disponibile non è \_ \_ \_ \_ \_ sufficiente, E \_ INVALIDARG se *StartIndex* \_ non è valido o S FALSE se non sono presenti colori nella tavolozza.

## <a name="remarks"></a>Commenti

Questa funzione membro restituisce la tavolozza corrente del video come matrice allocata dall'utente. Per mantenere la coerenza, usare i membri nella struttura WIN32 **PALETTEENTRY** per restituire i colori, anziché i membri nella struttura **RGBQUAD** (anche se il parametro è **long).** La memoria viene allocata dal chiamante, quindi è sufficiente copiare ogni elemento a turno. Determinare che il numero di voci richieste e l'offset della posizione iniziale sono entrambi validi. Se il numero di voci restituisce zero, restituisce un codice S \_ FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




