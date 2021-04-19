---
description: Metodo del costruttore.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Costruttore CImagePalette. CImagePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38b5766617e1d17fa3917048c2fb845b5194cc42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332273"
---
# <a name="cimagepalettecimagepalette-constructor"></a>Costruttore CImagePalette. CImagePalette

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBaseFilter* 
</dt> <dd>

Puntatore al filtro proprietario.

</dd> <dt>

*pBaseWindow* 
</dt> <dd>

Puntatore a un oggetto **CBaseWindow** , che gestisce la finestra in cui viene realizzata la tavolozza. Questo parametro può essere **NULL**.

</dd> <dt>

*pDrawImage* 
</dt> <dd>

Puntatore a un oggetto **CDrawImage** , che consente di disegnare l'immagine del video. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




