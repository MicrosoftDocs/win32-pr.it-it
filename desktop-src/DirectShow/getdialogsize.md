---
description: La funzione GetDialogSize recupera le dimensioni di una finestra di dialogo della risorsa.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: Funzione GetDialogSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330937"
---
# <a name="getdialogsize-function"></a>GetDialogSize (funzione)

La funzione **GetDialogSize** recupera le dimensioni di una finestra di dialogo della risorsa.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iResourceID* 
</dt> <dd>

Identificatore della risorsa della finestra di dialogo.

</dd> <dt>

*pDlgProc* 
</dt> <dd>

Puntatore alla routine della finestra di dialogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore passato al messaggio WM \_ INITDIALOG inviato alla finestra di dialogo temporanea subito dopo la creazione.

</dd> <dt>

*pResult* 
</dt> <dd>

Puntatore a una struttura di **dimensioni** che riceve le dimensioni della finestra di dialogo, in pixel dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se la risorsa della finestra di dialogo è stata trovata; in caso contrario, **false** .

## <a name="remarks"></a>Commenti

Le pagine delle proprietà possono usare questa funzione per restituire le dimensioni di visualizzazione effettive necessarie. La maggior parte delle pagine delle proprietà sono finestre di dialogo e, di conseguenza, i modelli di finestra di dialogo archiviati nei file di risorse. I modelli usano unità della finestra di dialogo che non eseguono il mapping direttamente sui pixel dello schermo. Tuttavia, la funzione [**GetPageInfo**](cbasepropertypage-getpageinfo.md) della pagina delle proprietà deve restituire le dimensioni di visualizzazione effettive in pixel. La pagina delle proprietà può chiamare `GetDialogSize` per calcolare le dimensioni di visualizzazione.

Questa funzione crea un'istanza temporanea della finestra di dialogo. Per evitare che la finestra di dialogo venga visualizzata sullo schermo, il modello della finestra di dialogo nel file di risorse non deve avere una \_ Proprietà WS Visible.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di supporto della pagina delle proprietà](property-page-helper-functions.md)
</dt> </dl>

 

 




