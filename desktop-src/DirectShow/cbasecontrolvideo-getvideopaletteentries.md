---
description: Il metodo GetVideoPaletteEntries recupera un intervallo di voci della tavolozza per il video.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Metodo CBaseControlVideo. GetVideoPaletteEntries (Ctlutil. h)
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
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332083"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a>CBaseControlVideo. GetVideoPaletteEntries, metodo

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

*StartIndex* 
</dt> <dd>

Voce della tavolozza iniziale in base zero.

</dd> <dt>

*Voci* 
</dt> <dd>

Numero di voci richieste.

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

Restituisce NOERROR se ha esito positivo, VFW \_ E \_ Nessuna \_ tavolozza \_ disponibile se gli esempi video non hanno tavolozza colori, e \_ OutOfMemory se la memoria disponibile non è sufficiente, e \_ INVALIDARG se *startIndex* non è valido oppure S \_ false se non sono presenti colori nella tavolozza.

## <a name="remarks"></a>Commenti

Questa funzione membro restituisce la tavolozza corrente del video come matrice allocata dall'utente. Per rimanere coerenti, usare i membri della struttura Win32 **PaletteEntry** per restituire i colori, anziché i membri nella struttura **RGBQUAD** (anche se il parametro è **Long**). La memoria viene allocata dal chiamante, quindi è sufficiente copiarla a turno. Determinare se il numero di voci richieste e l'offset della posizione iniziale sono entrambi validi. Se il numero di voci restituisce zero, restituire un \_ codice S false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




