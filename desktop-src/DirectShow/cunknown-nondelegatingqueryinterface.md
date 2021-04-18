---
description: 'Recupera un puntatore a interfaccia e incrementa il conteggio dei riferimenti. Questo metodo implementa il metodo INonDelegatingUnknown:: NonDelegatingQueryInterface.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Metodo CUnknown. NonDelegatingQueryInterface (ComBase. h)
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
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331446"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a>CUnknown. NonDelegatingQueryInterface, metodo

Recupera un puntatore a interfaccia e incrementa il conteggio dei riferimenti. Questo metodo implementa il metodo **INonDelegatingUnknown:: NonDelegatingQueryInterface** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* 
</dt> <dd>

Identificatore dell'interfaccia.

</dd> <dt>

*PPV* 
</dt> <dd>

Indirizzo di un puntatore per la ricezione dell'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                                |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | L'oggetto non supporta questa interfaccia.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null** .<br/>              |



 

## <a name="remarks"></a>Commenti

La classe **CUnknown** espone solo l'interfaccia **IUknown** . Eseguire l'override di questo metodo per esporre interfacce aggiuntive. Per informazioni su come eseguire l'override di questo metodo, vedere [How to implement IUnknown](how-to-implement-iunknown.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




