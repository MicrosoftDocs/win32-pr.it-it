---
title: Transazione XTYP_EXECUTE (DDEML. h)
description: Un client utilizza XTYP \_ Execute Transaction per inviare una stringa di comando al server. Una funzione di callback del server Dynamic Data Exchange (DDE), DdeCallback, riceve questa transazione quando un client specifica XTYP \_ Execute nella funzione DdeClientTransaction.
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- Scambio di dati delle transazioni XTYP_EXECUTE
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048619"
---
# <a name="xtyp_execute-transaction"></a>XTYP \_ Execute Transaction

Un client utilizza **XTYP \_ Execute** Transaction per inviare una stringa di comando al server. Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica **XTYP \_ Execute** nella funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uType* 
</dt> <dd>

Tipo di transazione.

</dd> <dt>

*uFmt* 
</dt> <dd>

Non usato.

</dd> <dt>

*hconv* 
</dt> <dd>

Handle per la conversazione.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle per il nome dell'argomento.

</dd> <dt>

*hsz2* 
</dt> <dd>

Non usato.

</dd> <dt>

*hdata* 
</dt> <dd>

Handle per la stringa di comando.

</dd> <dt>

*dwData1* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData2* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una funzione di callback del server deve restituire **\_ fack DDE** se elabora questa transazione, **DDE \_ FBUSY** se è troppo occupato per elaborare la transazione o **\_ FNOTPROCESSED DDE** se rifiuta questa transazione.

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione server specificata il flag **CBF \_ Fail \_ executes** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un'applicazione deve liberare l'handle di dati ottenuto durante la transazione. Un'applicazione, tuttavia, deve copiare la stringa di comando associata all'handle di dati se l'applicazione deve elaborare la stringa dopo che la funzione di callback restituisce. Un'applicazione può usare la funzione [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) per copiare i dati.

Poiché la maggior parte delle applicazioni client prevede che un'applicazione server esegua in modo sincrono un' **\_ esecuzione XTYP** , un server deve tentare di eseguire tutte le elaborazioni di **XTYP \_ Execute** Transaction dall'interno della funzione di callback DDE oppure restituendo il codice restituito del **\_ blocco CBR** . Se il parametro *hData* è un comando che indica al server di terminare, il server deve eseguire tale operazione dopo l'elaborazione di **XTYP \_ Execute** Transaction.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>DDEML. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

