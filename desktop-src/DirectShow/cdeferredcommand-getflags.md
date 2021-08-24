---
description: Il metodo GetFlags recupera i flag di contesto associati al comando posticipato.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: Metodo CDeferredCommand.GetFlags (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c3ee5826c1b4ff81f90c86a6db4517aafc41313e53672486c41ab4847e82674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910191"
---
# <a name="cdeferredcommandgetflags-method"></a>Metodo CDeferredCommand.GetFlags

Il `GetFlags` metodo recupera i flag di contesto associati al comando posticipato.

## <a name="syntax"></a>Sintassi


```C++
short GetFlags();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce una delle operazioni seguenti:



| Codice restituito                                                                                             | Descrizione                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**METODO \_ DISPATCH**</dt> </dl>         | Eseguire il membro come metodo . Se una proprietà ha lo stesso nome, è possibile impostare sia questo che il \_ flag PROPERTYGET DISPATCH.<br/>                                               |
| <dl> <dt>**DISPATCH \_ PROPERTYGET**</dt> </dl>    | Il membro viene recuperato come proprietà o membro dati.<br/>                                                                                                         |
| <dl> <dt>**PROPRIETÀ \_ DISPATCHPUT**</dt> </dl>    | Il membro viene modificato come proprietà o membro dati.<br/>                                                                                                           |
| <dl> <dt>**DISPATCH \_ PROPERTYPUTREF**</dt> </dl> | Il membro viene modificato tramite un'assegnazione di riferimento, anziché un'assegnazione di valore. Questo flag è valido solo quando la proprietà accetta un riferimento a un oggetto .<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




