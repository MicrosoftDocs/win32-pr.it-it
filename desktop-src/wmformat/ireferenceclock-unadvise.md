---
title: IReferenceClock Unadvise (metodo)
description: Il metodo Unadvise Annulla una richiesta di notifica.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Metodo Unadvise Windows Media Format
- Unadvise metodo Windows Media Format, interfaccia IReferenceClock
- Interfaccia IReferenceClock-formato Windows Media, metodo Unadvise
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117124"
---
# <a name="ireferenceclockunadvise-method"></a>Metodo IReferenceClock:: Unadvise

Il metodo **Unadvise** Annulla una richiesta di notifica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

Identificatore della richiesta da rimuovere. Usare il valore restituito da AdviseTime nel parametro pdwAdviseCookie.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Il metodo è riuscito.<br/>                    |
| <dl> <dt>**S \_ false**</dt> </dl> | L'identificatore passato non esiste.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





