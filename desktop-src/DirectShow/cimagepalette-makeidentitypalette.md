---
description: Il metodo MakeIdentityPalette tenta di creare una tavolozza delle identità \# &0034;&0034; definita come mappata direttamente alla tavolozza selezionata nel dispositivo di \# visualizzazione.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Metodo CImagePalette.MakeIdentityPalette (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb6e9a4e2c6adc411b7b043e35dc6dacf45dbb6a6ee4cf326a1c1953c559c16f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916131"
---
# <a name="cimagepalettemakeidentitypalette-method"></a>Metodo CImagePalette.MakeIdentityPalette

Il metodo tenta di creare una "tavolozza delle identità", definita come una tavolozza mappata direttamente alla `MakeIdentityPalette` tavolozza selezionata nel dispositivo di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pEntry* 
</dt> <dd>

Puntatore a una matrice di voci della tavolozza.

</dd> <dt>

*iColours* 
</dt> <dd>

Numero di voci della tavolozza in *pEntry.*

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione GDI **EnumDisplayDevices.** Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo o S FALSE in caso di esito \_ negativo.

## <a name="remarks"></a>Commenti

Questo metodo confronta le voci riservate nella tavolozza di sistema con le voci corrispondenti nella *matrice pEntry.* Se corrispondono esattamente, il metodo imposta il flag PC NOCOLLAPSE nelle voci della \_ tavolozza rimanenti (non riservate) in *pEntry*. Questo flag impedisce a GDI di eseguire il mapping delle voci della tavolozza logica alle voci della tavolozza di sistema.

Il [**metodo CImagePalette::MakePalette**](cimagepalette-makepalette.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




