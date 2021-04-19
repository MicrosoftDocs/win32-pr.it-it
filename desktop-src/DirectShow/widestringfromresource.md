---
description: La funzione WideStringFromResource carica una stringa di caratteri wide da un file di risorse con l'identificatore di risorsa specificato.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Funzione WideStringFromResource (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329357"
---
# <a name="widestringfromresource-function"></a>WideStringFromResource (funzione)

La `WideStringFromResource` funzione carica una stringa di caratteri wide da un file di risorse con l'identificatore di risorsa specificato.

## <a name="syntax"></a>Sintassi


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBuffer* 
</dt> <dd>

Puntatore alla stringa corrispondente a *iResourceID*.

</dd> <dt>

*iResourceID* 
</dt> <dd>

Identificatore di risorsa della stringa da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la stessa stringa di *pbuffer*. Se la funzione ha esito negativo, restituisce una stringa null.

## <a name="remarks"></a>Commenti

Le pagine delle proprietà vengono in genere chiamate tramite le interfacce COM, che usano stringhe a caratteri wide indipendentemente dalla modalità di compilazione del file binario. Questa funzione consente di convertire una stringa di risorsa in una stringa di caratteri wide. La funzione converte la risorsa in una stringa di caratteri wide (se non è già una) dopo il caricamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di supporto della pagina delle proprietà](property-page-helper-functions.md)
</dt> </dl>

 

 




