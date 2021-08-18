---
description: Il metodo QueryStations fornisce un elenco di tutti i computer che stanno attualmente acquisendo dati usando Network Monitor.
ms.assetid: feebcb28-914b-450e-95d4-10a60cbf1438
title: Metodo IStats::QueryStations (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2d4ead22b3e7308aee3c44b3ff6dff407591cbe675b09a3300f3e7a8720726c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742641"
---
# <a name="istatsquerystations-method"></a>Metodo IStats::QueryStations

Il **metodo QueryStations** fornisce un elenco di tutti i computer che stanno attualmente acquisendo dati usando Network Monitor.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpQueryTable* \[ in, out\]
</dt> <dd>

Puntatore a una [struttura QUERYTABLE.](querytable.md) In input, questa struttura deve contenere il numero massimo di computer che Network Monitor restituire e una matrice di [strutture STATIONQUERY.](stationquery.md)

In caso di output, questa struttura restituisce il numero di computer che acquisisce dati e una [struttura STATIONQUERY](stationquery.md) per ogni computer trovato. Si noti che queste informazioni possono includere computer che usano versioni di Network Monitor precedenti alla versione 2.0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:



| Codice restituito                                                                                           | Descrizione                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**MEMORIA INSUFFICIENTE DI NMERR \_ \_ \_**</dt> </dl> | La memoria necessaria per elaborare la query non era disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato in qualsiasi momento dopo [la chiamata a CreateNPPInterface.](createnppinterface.md) Una chiamata a questo metodo è una chiamata sincrona, che può richiedere alcuni secondi per il completamento Network Monitor attesa che i computer remoti rispondano alla query. È possibile eseguire query solo sui computer nella subnet locale.

È responsabilità dell'utente allocare la memoria per la [struttura QUERYTABLE](querytable.md) e liberare tale memoria dopo che la tabella non è più necessaria. Questo requisito include la memoria necessaria per la [matrice STATIONQUERY](stationquery.md) usata in QUERYTABLE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStat](istats.md)
</dt> <dt>

[Querytable](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




