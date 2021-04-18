---
description: Il metodo attivo crea un thread di lavoro che estrae i dati dal pin di output. Questo metodo consente inoltre di eseguire il commit dell'allocatore.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Metodo CPullPin. Active (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333716"
---
# <a name="cpullpinactive-method"></a>Metodo CPullPin. Active

Il metodo **attivo** crea un thread di lavoro che estrae i dati dal pin di output. Questo metodo consente inoltre di eseguire il commit dell'allocatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>                                                   |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | La connessione del PIN non è stata stabilita correttamente.<br/>          |
| <dl> <dt>**E \_ non riescono**</dt> </dl>       | Non è stato possibile creare il thread oppure il thread esiste già.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo quando il filtro proprietario diventa attivo. Se il pin di input deriva da [**CBasePin**](cbasepin.md), eseguire l'override del metodo [**CBasePin:: Active**](cbasepin-active.md) .

Prima di chiamare questo metodo, chiamare il metodo [**CPullPin:: Connect**](cpullpin-connect.md) per stabilire la connessione con il pin di output.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




