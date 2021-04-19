---
description: 'Esegue il mapping di una singola funzione membro e di un set facoltativo di parametri a un set corrispondente di identificatori di invio di numeri interi, che possono essere usati durante le chiamate successive alla funzione membro CMediaEvent:: Invoke.'
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Metodo CMediaEvent. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 191fa85264e4e7e22aa67f409db20cebd68f4319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332336"
---
# <a name="cmediaeventgetidsofnames-method"></a>CMediaEvent. GetIDsOfNames, metodo

Esegue il mapping di una singola funzione membro e di un set facoltativo di parametri a un set corrispondente di identificatori di invio di numeri interi, che possono essere usati durante le chiamate successive alla funzione membro [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* 
</dt> <dd>

Identificatore di riferimento. Riservato per utilizzi futuri. Deve essere **null**.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Indirizzo di un puntatore a una matrice di nomi passata di cui eseguire il mapping.

</dd> <dt>

*CNAME* 
</dt> <dd>

Conteggio dei nomi di cui eseguire il mapping.

</dd> <dt>

*lcid* 
</dt> <dd>

Contesto delle impostazioni locali in cui interpretare i nomi.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntatore a una matrice allocata dal chiamante, ogni elemento contenente un ID corrispondente a uno dei nomi passati nella matrice *rgszNames* . Il primo elemento rappresenta il nome del membro; gli elementi successivi rappresentano ognuno dei parametri del membro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ CLSID sconosciuto disp \_ E**</dt> </dl> | Il CLSID non è stato riconosciuto.<br/>                                                                                                             |
| <dl> <dt>**DISP \_ E \_ unknowname**</dt> </dl>    | Uno o più nomi non sono noti. I DISPID restituiti contengono DISPID \_ sconosciuto per ogni voce che corrisponde a un nome sconosciuto.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>          | Memoria insufficiente.<br/>                                                                                                                            |
| <dl> <dt>**\_OK**</dt> </dl>                   | Esito positivo.<br/>                                                                                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




