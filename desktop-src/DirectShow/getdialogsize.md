---
description: La funzione GetDialogSize recupera le dimensioni di una finestra di dialogo della risorsa.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: Funzione GetDialogSize (Wxutil.h)
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
ms.openlocfilehash: 7f1f2631e169549895a1f74ce571b2abfeeee8cd77ac7cb3c4dfc5aa6913a6d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564951"
---
# <a name="getdialogsize-function"></a>Funzione GetDialogSize

La **funzione GetDialogSize** recupera le dimensioni di una finestra di dialogo della risorsa.

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

Identificatore di risorsa della finestra di dialogo.

</dd> <dt>

*pDlgProc* 
</dt> <dd>

Puntatore alla routine della finestra di dialogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore passato nel messaggio WM \_ INITDIALOG inviato alla finestra di dialogo temporanea subito dopo la creazione.

</dd> <dt>

*pResult* 
</dt> <dd>

Puntatore a **una struttura SIZE** che riceve le dimensioni della finestra di dialogo, in pixel dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** la risorsa della finestra di dialogo è stata trovata oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Le pagine delle proprietà possono usare questa funzione per restituire le dimensioni di visualizzazione effettive richieste. La maggior parte delle pagine delle proprietà sono finestre di dialogo e, di conseguenza, dispongono di modelli di finestra di dialogo archiviati nei file di risorse. I modelli usano unità di finestra di dialogo che non vengono mappate direttamente sui pixel dello schermo. Tuttavia, la funzione [**GetPageInfo**](cbasepropertypage-getpageinfo.md) di una pagina delle proprietà deve restituire le dimensioni di visualizzazione effettive in pixel. La pagina delle proprietà può chiamare `GetDialogSize` per calcolare le dimensioni di visualizzazione.

Questa funzione crea un'istanza temporanea della finestra di dialogo. Per evitare che la finestra di dialogo venga visualizzata sullo schermo, il modello di finestra di dialogo nel file di risorse non deve avere una proprietà \_ WS VISIBLE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper pagina delle proprietà](property-page-helper-functions.md)
</dt> </dl>

 

 




