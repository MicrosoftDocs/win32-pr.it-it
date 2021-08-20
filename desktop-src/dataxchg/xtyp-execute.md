---
title: XTYP_EXECUTE transazione (Ddeml.h)
description: Un client utilizza la transazione EXECUTE XTYP \_ per inviare una stringa di comando al server. Una funzione di callback del server Dynamic Data Exchange (DDE) DdeCallback riceve questa transazione quando un client specifica XTYP EXECUTE nella \_ funzione DdeClientTransaction.
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- XTYP_EXECUTE dati della transazione Exchange
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
ms.openlocfilehash: 6dd6d23b485de31693fc5ad3a648414e3cc18251f741f69885de0fda714d8f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118102122"
---
# <a name="xtyp_execute-transaction"></a>Transazione EXECUTE XTYP \_

Un client utilizza la **transazione \_ EXECUTE XTYP** per inviare una stringa di comando al server. Una funzione di callback del server Dynamic Data Exchange [*(DDE) DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)riceve questa transazione quando un client specifica **XTYP \_ EXECUTE** nella [**funzione DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


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

Una funzione di callback del server deve restituire **DDE \_ FACK** se elabora questa **transazione, DDE \_ FBUSY** se è troppo occupato per elaborare la transazione o **DDE \_ FNOTPROCESSED** se rifiuta questa transazione.

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ FAIL \_ EXECUTES** nella [**funzione DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

Un'applicazione deve liberare l'handle di dati ottenuto durante questa transazione. Un'applicazione deve tuttavia copiare la stringa di comando associata all'handle di dati se l'applicazione deve elaborare la stringa dopo la fine della funzione di callback. Un'applicazione può usare [**la funzione DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) per copiare i dati.

Poiché la maggior parte delle applicazioni client prevede che un'applicazione server eserciti una transazione **\_ EXECUTE XTYP** in modo sincrono, un server deve tentare di eseguire tutte le elaborazioni della transazione **\_ EXECUTE XTYP** dall'interno della funzione di callback DDE o tramite la restituzione del codice **restituito CBR \_ BLOCK.** Se il *parametro hdata* è un comando che indica al server di terminare, il server deve eseguire questa operazione dopo l'elaborazione della **transazione \_ EXECUTE XTYP.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Ddeml.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Dynamic Data Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

