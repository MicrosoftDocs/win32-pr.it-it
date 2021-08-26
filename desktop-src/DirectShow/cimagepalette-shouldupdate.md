---
description: Il metodo ShouldUpdate determina se è necessario creare una nuova tavolozza.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Metodo CImagePalette.ShouldUpdate (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c7897e14aec690ec67451fe868b5352e99c9bd513c8c182a47556fe075cffb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916031"
---
# <a name="cimagepaletteshouldupdate-method"></a>Metodo CImagePalette.ShouldUpdate

Il `ShouldUpdate` metodo determina se è necessario creare una nuova tavolozza.

## <a name="syntax"></a>Sintassi


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNewInfo* 
</dt> <dd>

Puntatore a una [**struttura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contenente la nuova tabella dei colori.

</dd> <dt>

*pOldInfo* 
</dt> <dd>

Puntatore a una **struttura VIDEOINFOHEADER** contenente la tabella dei colori precedente. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** è necessario aggiornare la tavolozza oppure FALSE in **caso** contrario.

## <a name="remarks"></a>Commenti

-   Se nessuna **delle due strutture VIDEOINFOHEADER** contiene una tabella dei colori, il metodo restituisce **FALSE.**
-   Se una sola struttura contiene una tabella dei colori o *se pOldInfo* è **NULL,** il metodo restituisce **TRUE.**
-   Se entrambe le strutture contengono tabelle dei colori e le voci di colore corrispondono, il metodo restituisce **FALSE.**
-   Se entrambe le strutture contengono tabelle dei colori, ma le voci di colore non corrispondono, il metodo restituisce **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




