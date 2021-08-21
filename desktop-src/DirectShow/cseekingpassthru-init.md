---
description: Il metodo Init inizializza l'oggetto .
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: CSeekingPassThru.Init (Seekpt.h)
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
ms.openlocfilehash: 91d20477f83ec79c6ae6095e81810c98454f9c26521eda995c919867b3e3ac12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953816"
---
# <a name="cseekingpassthruinit-method"></a>CSeekingPassThru.Init

Il `Init` metodo inizializza l'oggetto .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bSupportRendering* \[ Pollici\]
</dt> <dd>

Valore booleano che specifica se il filtro è un renderer. Usare il valore **TRUE se** il filtro è un renderer oppure FALSE **in caso** contrario.

</dd> <dt>

*pPin* 
</dt> <dd>

Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) sul pin di input del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                                |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | L'oggetto è già stato inizializzato.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per creare l'oggetto.<br/> |



 

## <a name="remarks"></a>Commenti

Se il valore di *bSupportRendering* è **TRUE,** questo metodo crea un'istanza della [**classe CRendererPosPassThru.**](crendererpospassthru.md) In caso contrario, viene creata un'istanza [**della classe CPosPassThru.**](cpospassthru.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Seekpt.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSeekingPassThru**](cseekingpassthru.md)
</dt> </dl>

 

 




