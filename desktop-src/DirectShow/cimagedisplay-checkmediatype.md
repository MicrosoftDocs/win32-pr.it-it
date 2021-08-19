---
description: Il metodo CheckMediaType determina se un tipo di supporto proposto è compatibile con il formato di visualizzazione.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Metodo CImageDisplay.CheckMediaType (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad6a7242ba110ad3916d08070eef40a8fa1d5d658ea366732e14a1cd107d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087391"
---
# <a name="cimagedisplaycheckmediatype-method"></a>Metodo CImageDisplay.CheckMediaType

Il `CheckMediaType` metodo determina se un tipo di supporto proposto è compatibile con il formato di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pmtIn* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che contiene il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Tipo di supporto non valido.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Tipo di supporto non valido.<br/>           |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il tipo di supporto è compatibile.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




