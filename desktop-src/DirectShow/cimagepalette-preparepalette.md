---
description: Il metodo PreparePalette configura una tavolozza in base a un tipo di supporto dal filtro proprietario.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Metodo CImagePalette. PreparePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325063"
---
# <a name="cimagepalettepreparepalette-method"></a>CImagePalette. PreparePalette, metodo

Il `PreparePalette` metodo configura una tavolozza in base a un tipo di supporto dal filtro proprietario.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pmtNew* 
</dt> <dd>

Puntatore al nuovo tipo di supporto. Il blocco di formato deve essere una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

</dd> <dt>

*pmtOld* 
</dt> <dd>

Puntatore al vecchio tipo di supporto. Se il tipo di supporto viene impostato per la prima volta, questo parametro può essere un tipo vuoto senza blocco di formato. In caso contrario, il blocco di formato deve essere una struttura **VIDEOINFOHEADER** .

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione **ENUMDISPLAYDEVICES** GDI. Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se la tavolozza è stata aggiornata oppure s \_ false se la tavolozza non è stata modificata.

## <a name="remarks"></a>Commenti

Se è necessario aggiornare la tavolozza, questo metodo esegue le azioni seguenti:

-   Chiama [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) per creare una nuova tavolozza logica.
-   Invia un evento di [**\_ \_ modifica della tavolozza EC**](ec-palette-changed.md) al gestore del grafico dei filtri.
-   Chiama [**CBaseWindow:: Setavolozza**](cbasewindow-setpalette.md) sull'oggetto **CBaseWindow** .
-   Chiama [**CDrawImage:: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) sull'oggetto **CDrawImage** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




