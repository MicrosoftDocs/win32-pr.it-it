---
description: Il metodo MakeIdentityPalette tenta di creare un &\# 0034; Identity palette, &\# 0034; definito come uno che esegue il mapping direttamente alla tavolozza selezionata nel dispositivo di visualizzazione.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Metodo CImagePalette. MakeIdentityPalette (Winutil. h)
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
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325067"
---
# <a name="cimagepalettemakeidentitypalette-method"></a>CImagePalette. MakeIdentityPalette, metodo

Il `MakeIdentityPalette` metodo tenta di creare una "tavolozza di identità", definita come uno che esegue il mapping direttamente alla tavolozza selezionata nel dispositivo di visualizzazione.

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

*Pente* 
</dt> <dd>

Puntatore a una matrice di voci della tavolozza.

</dd> <dt>

*iColours* 
</dt> <dd>

Numero di voci della tavolozza in *pente*.

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione **ENUMDISPLAYDEVICES** GDI. Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se l'operazione ha esito positivo o \_ false se non è riuscita.

## <a name="remarks"></a>Commenti

Questo metodo confronta le voci riservate nella tavolozza di sistema con le voci corrispondenti nell' *Array.* Se corrispondono esattamente, il metodo imposta il flag PC \_ nocollapse nelle voci della tavolozza rimanenti (non riservate) in *pente*. Questo flag impedisce a GDI di provare a eseguire il mapping delle voci della tavolozza logica alle voci della tavolozza.

Il metodo [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




