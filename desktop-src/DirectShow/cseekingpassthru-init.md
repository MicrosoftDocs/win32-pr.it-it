---
description: Il metodo init Inizializza l'oggetto.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Metodo CSeekingPassThru.Init (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324665"
---
# <a name="cseekingpassthruinit-method"></a>Metodo CSeekingPassThru.Init

Il `Init` metodo inizializza l'oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bSupportRendering* \[ in\]
</dt> <dd>

Valore booleano che specifica se il filtro è un renderer. Usare il valore **true** se il filtro è un renderer oppure **false** in caso contrario.

</dd> <dt>

*pPin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) sul pin di input del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                                |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Oggetto già inizializzato.<br/>         |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente per creare l'oggetto.<br/> |



 

## <a name="remarks"></a>Commenti

Se il valore di *bSupportRendering* è **true**, questo metodo crea un'istanza della classe [**CRendererPosPassThru**](crendererpospassthru.md) . In caso contrario, viene creata un'istanza della classe [**CPosPassThru**](cpospassthru.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Seekpt. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSeekingPassThru**](cseekingpassthru.md)
</dt> </dl>

 

 




