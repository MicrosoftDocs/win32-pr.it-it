---
description: Fornisce un elenco di tutti i computer che utilizzano attualmente Network Monitor per acquisire i dati di rete.
ms.assetid: 57e7b8e1-99b8-4194-b6dc-401235be4ef4
title: 'Metodo IRTC:: QueryStations (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a0cebd789284dd41c293424a70686f30eb4601d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967137"
---
# <a name="irtcquerystations-method"></a>Metodo IRTC:: QueryStations

Il metodo **QueryStations** fornisce un elenco di tutti i computer che utilizzano attualmente Network Monitor per acquisire i dati di rete.

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

Puntatore a una struttura [**QUERYTABLE**](querytable.md) . In input questa struttura deve contenere il numero massimo di computer che si desidera vengano restituiti Network Monitor e una matrice di strutture [**STATIONQUERY**](stationquery.md) .

Nell'output questa struttura restituisce il numero di computer che acquisiscono i dati e una struttura [**STATIONQUERY**](stationquery.md) per ogni computer trovato. Tenere presente che potrebbero essere inclusi computer che usano versioni di Network Monitor la versione preesistente 2,0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è **NMERR \_ Success**.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                           | Descrizione                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_ \_ \_ memoria insufficiente NMERR**</dt> </dl> | La memoria necessaria per elaborare la query non è disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato in qualsiasi momento dopo la chiamata del metodo [**CreateNPPInterface**](createnppinterface.md) . Una chiamata a questo metodo è una chiamata sincrona, che può richiedere alcuni secondi per il completamento mentre Network Monitor attende che i computer remoti rispondano alla query. È possibile eseguire query solo sui computer della subnet locale.

L'utente deve allocare la memoria per la struttura [**QUERYTABLE**](querytable.md) e liberare tale memoria dopo che la tabella non è più necessaria. Questo requisito include la memoria necessaria per la matrice [**STATIONQUERY**](stationquery.md) usata in **QUERYTABLE**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**QUERYTABLE**](querytable.md)
</dt> <dt>

[**STATIONQUERY**](stationquery.md)
</dt> </dl>

 

 




