---
description: Il metodo SetFormat inizializza il blocco di formato.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Metodo CMediaType.SetFormat (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99726a466b6bf273b654a5d459fa2391a75882f1adee64b981d91a514a988b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108451"
---
# <a name="cmediatypesetformat-method"></a>Metodo CMediaType.SetFormat

Il `SetFormat` metodo inizializza il blocco di formato.

## <a name="syntax"></a>Sintassi


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntatore a un blocco di memoria che contiene il blocco di formato.

</dd> <dt>

*length* 
</dt> <dd>

Lunghezza del blocco di formato, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **se** si è verificato un errore.

## <a name="remarks"></a>Commenti

Questo metodo alloca memoria per il blocco di formato e copia il buffer specificato da *pFormat* nel nuovo blocco di formato. Se il tipo di supporto contiene già un blocco di formato, viene rilasciato quello precedente. Il metodo imposta anche il **membro cbFormat** della struttura **AM MEDIA \_ \_ TYPE.**

Per impostare il tipo di formato, chiamare il [**metodo CMediaType::SetFormatType.**](cmediatype-setformattype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




