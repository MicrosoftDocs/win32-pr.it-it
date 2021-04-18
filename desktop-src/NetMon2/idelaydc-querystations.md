---
description: Il metodo QueryStations fornisce un elenco di tutti i computer che attualmente utilizzano Network Monitor per acquisire i dati.
ms.assetid: 8e578f50-685e-4799-90ca-5da8810ec2a3
title: 'Metodo IDelaydC:: QueryStations (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5a45f5046dbd2e5714424baf42621e0c1d5539ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305884"
---
# <a name="idelaydcquerystations-method"></a>Metodo IDelaydC:: QueryStations

Il metodo **QueryStations** fornisce un elenco di tutti i computer che attualmente utilizzano Network Monitor per acquisire i dati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpQueryTable* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [QUERYTABLE](querytable.md) . In input questa struttura deve contenere il numero massimo di computer che si desidera vengano restituiti Network Monitor e una matrice di strutture [STATIONQUERY](stationquery.md) .

Nell'output, questa struttura restituisce il numero di computer che acquisiscono i dati e una struttura [STATIONQUERY](stationquery.md) per ogni computer rilevato. Si noti che questo elenco potrebbe includere computer che usano versioni di Network Monitor la versione data di 2,0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:



| Codice restituito                                                                                           | Descrizione                                               |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_ \_ \_ memoria insufficiente NMERR**</dt> </dl> | Memoria non disponibile per l'elaborazione della query.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato in qualsiasi momento dopo la chiamata a [CreateNPPInterface](createnppinterface.md) . Una chiamata a questo metodo è una chiamata sincrona, che può richiedere alcuni secondi per il completamento come Network Monitor attende che i computer remoti rispondano alla query. È possibile eseguire query solo sui computer della subnet locale.

È responsabilità dell'utente allocare la memoria per la struttura [QUERYTABLE](querytable.md) e liberarla dopo che la tabella non è più necessaria. Questo requisito include la memoria necessaria per la matrice [STATIONQUERY](stationquery.md) usata in QUERYTABLE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[QUERYTABLE](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




