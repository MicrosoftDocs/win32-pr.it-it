---
description: Il metodo UpdateColourTable aggiorna la tabella dei colori con una nuova tavolozza.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: Metodo CDrawImage.UpdateColourTable (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a53413cd1aaf60c17031f126f0a158629f5c41f8ca94981d293f003afadda8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384031"
---
# <a name="cdrawimageupdatecolourtable-method"></a>Metodo CDrawImage.UpdateColourTable

Il `UpdateColourTable` metodo aggiorna la tabella dei colori con una nuova tavolozza.

## <a name="syntax"></a>Sintassi


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hdc* 
</dt> <dd>

Contesto di dispositivo contenente l'immagine.

</dd> <dt>

*pbmi* 
</dt> <dd>

Puntatore a una [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) contenente la nuova tavolozza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




