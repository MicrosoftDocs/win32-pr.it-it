---
description: Il Metodo GetFlags recupera i flag di contesto associati al comando posticipato.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: Metodo CDeferredCommand. GetFlags (Ctlutil. h)
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
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333477"
---
# <a name="cdeferredcommandgetflags-method"></a>Metodo CDeferredCommand. GetFlags

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
| <dl> <dt>**\_metodo Dispatch**</dt> </dl>         | Eseguire il membro come metodo. Se una proprietà ha lo stesso nome, è possibile impostare sia questo che il \_ flag PropertyGet (di invio.<br/>                                               |
| <dl> <dt>**\_PROPERTYGET (dispatch**</dt> </dl>    | Il membro viene recuperato come una proprietà o un membro dati.<br/>                                                                                                         |
| <dl> <dt>**\_PROPERTYPUT dispatch**</dt> </dl>    | Il membro viene modificato come una proprietà o un membro dati.<br/>                                                                                                           |
| <dl> <dt>**\_PROPERTYPUTREF dispatch**</dt> </dl> | Il membro viene modificato tramite un'assegnazione di riferimento, anziché un'assegnazione di valore. Questo flag è valido solo quando la proprietà accetta un riferimento a un oggetto.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




