---
description: La funzione WideStringFromResource carica una stringa di caratteri wide da un file di risorse con l'identificatore di risorsa specificato.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Funzione WideStringFromResource (Wxutil.h)
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
ms.openlocfilehash: 798f915536c491d32ccab7e7dbdc9b506d8b5df22b4459818472307e62356b71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071815"
---
# <a name="widestringfromresource-function"></a>Funzione WideStringFromResource

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

Puntatore alla stringa corrispondente a *iResourceID.*

</dd> <dt>

*iResourceID* 
</dt> <dd>

Identificatore di risorsa della stringa da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la stessa stringa di *pBuffer.* Se la funzione non ha esito positivo, restituisce una stringa Null.

## <a name="remarks"></a>Commenti

Le pagine delle proprietà vengono in genere chiamate tramite le relative interfacce COM, che usano stringhe di caratteri wide indipendentemente dalla modalità di creazione del file binario. Questa funzione consente di convertire una stringa di risorsa in una stringa di caratteri wide. La funzione converte la risorsa in una stringa di caratteri wide (se non è già presente) dopo il caricamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper della pagina delle proprietà](property-page-helper-functions.md)
</dt> </dl>

 

 




