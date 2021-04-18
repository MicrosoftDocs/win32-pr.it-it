---
description: Il metodo ShouldUpdate determina se è necessario creare una nuova tavolozza.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Metodo CImagePalette. ShouldUpdate (Winutil. h)
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
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325059"
---
# <a name="cimagepaletteshouldupdate-method"></a>CImagePalette. ShouldUpdate, metodo

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

Puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contenente la nuova tabella dei colori.

</dd> <dt>

*pOldInfo* 
</dt> <dd>

Puntatore a una struttura **VIDEOINFOHEADER** contenente la tabella dei colori obsoleta. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se è necessario aggiornare la tavolozza; in caso contrario, **false** .

## <a name="remarks"></a>Commenti

-   Se nessuna delle due strutture **VIDEOINFOHEADER** contiene una tabella dei colori, il metodo restituisce **false**.
-   Se una sola struttura contiene una tabella dei colori o se *pOldInfo* è **null**, il metodo restituisce **true**.
-   Se entrambe le strutture contengono tabelle dei colori e le voci di colore corrispondono, il metodo restituisce **false**.
-   Se entrambe le strutture contengono tabelle dei colori, ma le voci di colore non corrispondono, il metodo restituisce **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




