---
description: Recupera un puntatore a interfaccia e incrementa il conteggio dei riferimenti. Questo metodo implementa il metodo INonDelegatingUnknown::NonDelegatingQueryInterface.
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Metodo CUnknown.NonDelegatingQueryInterface (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26e13d9d30c3da208bb702427ee99a9648a7f538ba0d5a6a1b359db41e2cd155
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076011"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a>Metodo CUnknown.NonDelegatingQueryInterface

Recupera un puntatore a interfaccia e incrementa il conteggio dei riferimenti. Questo metodo implementa il **metodo INonDelegatingUnknown::NonDelegatingQueryInterface.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Riid* 
</dt> <dd>

Identificatore dell'interfaccia.

</dd> <dt>

*Ppv* 
</dt> <dd>

Indirizzo di un puntatore per ricevere l'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                                |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | L'oggetto non supporta questa interfaccia.<br/> |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Argomento del puntatore **NULL.**<br/>              |



 

## <a name="remarks"></a>Commenti

La **classe CUnknown** espone solo l'interfaccia **IUknown.** Eseguire l'override di questo metodo per esporre interfacce aggiuntive. Per informazioni su come eseguire l'override di questo metodo, [vedere Come implementare IUnknown.](how-to-implement-iunknown.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




