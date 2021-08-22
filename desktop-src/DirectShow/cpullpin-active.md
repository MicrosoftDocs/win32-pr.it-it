---
description: Il metodo Active crea un thread di lavoro che esegue il pull dei dati dal pin di output. Questo metodo esegue anche il commit dell'allocatore.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Metodo CPullPin.Active (Pullpin.h)
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
ms.openlocfilehash: a6572ad0b415f4c1a51133d080e84a2e869787dea0c23614478b09c7b86296b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073525"
---
# <a name="cpullpinactive-method"></a>Metodo CPullPin.Active

Il **metodo Active** crea un thread di lavoro che esegue il pull dei dati dal pin di output. Questo metodo esegue anche il commit dell'allocatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata.<br/>                                                   |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | La connessione pin non è stata stabilita correttamente.<br/>          |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Impossibile creare il thread oppure il thread esiste già.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo quando il filtro proprietario diventa attivo. Se il pin di input deriva da [**CBasePin,**](cbasepin.md)eseguire l'override del [**metodo CBasePin::Active.**](cbasepin-active.md)

Prima di chiamare questo metodo, chiamare il [**metodo CPullPin::Connessione**](cpullpin-connect.md) per stabilire la connessione con il pin di output.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




