---
description: Mappe una singola funzione membro e un set facoltativo di parametri a un set corrispondente di identificatori di invio integer, che possono essere usati nelle chiamate successive alla funzione membro CMediaEvent::Invoke.
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Metodo CMediaEvent.GetIDsOfNames (Ctlutil.h)
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
ms.openlocfilehash: a638861bc6a01a615355f0fad05cddc00f31d3e659fc60c0be0246eb108583f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401874"
---
# <a name="cmediaeventgetidsofnames-method"></a>Metodo CMediaEvent.GetIDsOfNames

Mappe una singola funzione membro e un set facoltativo di parametri a un set corrispondente di identificatori di invio integer, che possono essere usati nelle chiamate successive alla funzione membro [**CMediaEvent::Invoke.**](cmediaevent-invoke.md)

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

*Riid* 
</dt> <dd>

Identificatore di riferimento. Riservato per utilizzi futuri. Deve essere **NULL.**

</dd> <dt>

*rgszNames* 
</dt> <dd>

Indirizzo di un puntatore a una matrice passata di nomi di cui eseguire il mapping.

</dd> <dt>

*cNames* 
</dt> <dd>

Conteggio dei nomi di cui eseguire il mapping.

</dd> <dt>

*lcid* 
</dt> <dd>

Contesto delle impostazioni locali in cui interpretare i nomi.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntatore a una matrice allocata dal chiamante, ogni cui elemento contiene un ID corrispondente a uno dei nomi passati nella matrice *rgszNames.* Il primo elemento rappresenta il nome del membro. Gli elementi successivi rappresentano ognuno dei parametri del membro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DISP \_ E \_ UNKNOWN \_ CLSID**</dt> </dl> | Il CLSID non è stato riconosciuto.<br/>                                                                                                             |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl>    | Uno o più nomi non erano noti. I DISPID restituiti contengono DISPID \_ UNKNOWN per ogni voce che corrisponde a un nome sconosciuto.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Memoria insufficiente.<br/>                                                                                                                            |
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione completata.<br/>                                                                                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




